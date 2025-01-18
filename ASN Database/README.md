# ASN Database

## An Autonomous System Number (ASN) is a unique identifier given to a collection of IP networks by an organization. Get range, range type, and organization information from the ASN database.

![ASN Explained](../assets/ASN.png)

# Database Schema & Description

*[data updated as of January, 2025]*

| Field Name  | Example          | Data Type | Description                                                               |
|-------------|------------------|-----------|---------------------------------------------------------------------------|
| **network** | `115.76.56.0/23` | TEXT      | CIDR or IP network of the ASN IP address block                            |
| **asn**     | `AS7552`         | TEXT      | Autonomous System Number (ASN)                                            |
| **domain**  | `viettel.com.vn` | TEXT      | Organization domain name of the ASN                                       |
| **name**    | `Viettel Group`  | TEXT      | Name of the ASN organization                                              |
| **type**    | `isp`            | TEXT      | ASN Type: ISP, Hosting, Education, Government or Business                 |
| **country** | `VN`             | TEXT      | ISO 3166 two letter country code of the ASN declared in the WHOIS records |


<details>

<summary><h3>Alternate Database Schema: <code>standard_asn</code></h3></summary>

The `standard_asn` data download is structured based on IP ranges (`start_ip` and `end_ip`) and includes the `join_key` column. Our default data downloads has been updated (January, 2025) to use the `network`-based schema which also does not include the `join_key` column. However, we will continue supporting the original IP range-based schema for existing customers, with no plans for deprecation. While the underlying data remains the same, the difference lies only in the schema.


| Field Name | Example             | Data Type | Description                                              |
|------------|---------------------|-----------|----------------------------------------------------------|
| `start_ip` | 125.113.0.0         | TEXT      | Starting IP address of the ASN IP address block          |
| `end_ip`   | 125.113.255.255     | TEXT      | Ending IP address of the ASN IP address block            |
| `join_key` | 125.113.0.0         | TEXT      | Special variable to facilitate database `join` operation |
| `asn`      | AS4134              | TEXT      | Autonomous System Number (ASN)                           |
| `domain`   | chinatelecom.com.cn | TEXT      | Domain name of the AS                                    |
| `name`     | CHINANET-BACKBONE   | TEXT      | Name of the ASN                                          |
| `type`     | isp                 | TEXT      | ASN Type: ISP, Hosting, Education, Government or Business|
| `country`  | CN                  | TEXT      | ISO 3166 country code of the ASN from the WHOIS records  |


> Includes IP range columns (`start_ip` and `end_ip`) instead of a network or CIDR based column (`network`).
> `join_key` represents the Class C network each IP address is part of, allowing you to filter the result set significantly before `join`ing. Learn more about `join_key` [here](https://community.ipinfo.io/t/ipinfos-join-key-column-explained/5526).

#### Samples

- [CSV Database] [ASN Database Sample](/ASN%20Database/asn_sample.csv)
- [JSON Database] [ASN Database Sample](/ASN%20Database/asn_sample.json)
- [MMDB Database] [ASN Database Sample](/ASN%20Database/asn_sample.mmdb)


</details>


## Downloadable File Formats

- CSV: Plain text file format where data is organized into rows, with individual values separated by commas.
- JSON: More specifically, NDJSON (Newline Delimited JSON), a text file format where each line is a separated in valid JSON object.
- MMDB: Specialized binary database for efficient and fast IP lookups.
- Parquet: A columnar storage file format optimized for efficient data querying.

> Please refer to "[How to choose the best file format for your IPinfo database?](https://ipinfo.io/blog/ipinfo-database-formats/)" article to select the best format possible for your use case.
>
> The usage of the IP data downloads relies on the software or application of the data. Check out our [documentation](https://ipinfo.io/developers/database-download), [community](https://community.ipinfo.io/c/docs/8), and our [integrations](https://ipinfo.io/integrations) pages to find the best path forward.

## Filename references:


| File Format | Filename / Slug    | Terminal Command                                                                            |
|-------------|--------------------|---------------------------------------------------------------------------------------------|
| CSV         | ipinfo_asn.csv.gz  | `curl -L https://ipinfo.io/data/ipinfo_asn.csv.gz?token=$YOUR_TOKEN -o ipinfo_asn.csv.gz`   |
| MMDB        | ipinfo_asn.mmdb    | `curl -L https://ipinfo.io/data/ipinfo_asn.mmdb?token=$YOUR_TOKEN -o ipinfo_asn.mmdb`       |
| JSON        | ipinfo_asn.json.gz | `curl -L https://ipinfo.io/data/ipinfo_asn.json.gz?token=$YOUR_TOKEN -o ipinfo_asn.json.gz` |
| Parquet     | ipinfo_asn.parquet | `curl -L https://ipinfo.io/data/ipinfo_asn.parquet?token=$YOUR_TOKEN -o ipinfo_asn.parquet` |


## Difference among the ASN Database, the free IP to ASN Database and the free IP to Country ASN Database

Compared to the [IP to ASN (Free) Database](https://ipinfo.io/developers/ip-to-asn-database) or the [free IP to Country ASN database](https://ipinfo.io/developers/ip-to-country-asn-database), the [ASN database (Premium)](https://ipinfo.io/products/asn-database) is different because of certain factors. The [free IP to ASN database](https://ipinfo.io/developers/ip-to-asn-database) is a subset of the [ASN database (Premium)](https://ipinfo.io/products/asn-database) and does not contain the following information.

- **AS range type:** The `type` column in the ASN database is not available in the free ASN database. The `type` column provides insights into what type of organization is running a certain range of IP addresses. It could be one of four types: Education, Hosting, Business, or ISP. The range type is assigned based on a range classifier algorithm. Learn about the IPinfo range classifier algorithm [here](https://community.ipinfo.io/t/how-do-we-classify-asn-types/2236).
- **AS country type:** The `country` column in the ASN database is different from the `country` column in the free IP to Country ASN database. The `country` column is not present in the free IP to ASN database. The `country` column in the ASN database represents the country of the AS organization as represented in the WHOIS records. Meanwhile, the `country` column in the free IP to Country ASN database represents the geolocated country of ranges as per our IP to Geolocation data. It does not provide information regarding the organization's country, but rather the country of the ranges in general.

# ASN API

Along with our ASN database product, IPinfo also provides a robust API service. ASN data is available in two ways:
- [ASN information for an IP address](https://ipinfo.io/developers/data-types#asn-data)
- [ASN lookup](https://ipinfo.io/developers/asn)

The ASN API service is available as part of our [Basic Tier](https://ipinfo.io/developers/responses#basic-plan) plan.

## **ASN data from IP Address lookup**

You can get ASN level information of an IP address by looking up the IP address through [our API](https://ipinfo.io/developers/data-types#asn-data).

API Query:

```bash
$ curl ipinfo.io/$IP_ADDRESS/ASN?token=$TOKEN
```

Response:

```json
{
    "asn": "AS1221",
    "name": "Telstra Limited",
    "domain": "telstra.com.au",
    "route": "58.160.0.0/12",
    "type": "isp"
}
```

![ASN Data from IP Lookup.png](../assets/ASN_Data_from_IP_Lookup.png)

> We will also provide basic ASN information on our free and publicly accessible API service through the `org` field.

## **ASN data API**

You can get information on the ASNs themselves by looking up an ASN. Just prefix the `AS` keyword in front of the ASN (e.g. `AS12345`) and look it up on our [API endpoint](https://ipinfo.io/developers/asn).

```bash
$ curl ipinfo.io/$ASN?token=$TOKEN
```

Response:

```json
{
    "asn": "AS2828",
    "name": "Verizon Business",
    "country": "US",
    "allocated": "2001-12-19",
    "registry": "arin",
    "domain": "verizonbusiness.com",
    "num_ips": 6654976,
    "type": "isp",
    "prefixes": [
        {
            "netblock": "104.237.24.0/22",
            "id": "VOICECARRIER",
            "name": "Voice Carrier, LLC",
            "country": "US",
            "size": "1024",
            "status": "ALLOCATION",
            "domain": "voicecarrier.com"
        },
        // ...
    ],
        "prefixes6": [
        {
            "netblock": "2610:18::/32",
            "id": "XOXO-IPV6-A",
            "name": "Verizon Business",
            "country": "US",
            "size": "79228162514264337593543950336",
            "status": "ALLOCATION",
            "domain": "verizonbusiness.com"
        },
        // ...
    ],
    "peers": [
        "17216",
        // ...
    ],
    "upstreams": [
        "1299",
        // ...
    ]
    "downstreams": [
        "9",
        // ...
    ]
}
```

![ASN Data API (1).png](../assets/ASN_Data_API.png)

# Samples

- [CSV Database] [ASN Database Sample](/ASN%20Database/asn_sample.csv)
- [JSON Database] [ASN Database Sample](/ASN%20Database/asn_sample.json)
- [MMDB Database] [ASN Database Sample](/ASN%20Database/asn_sample.mmdb)
- [API] [ASN Lookup API Response Sample](/ASN%20Database/asn_lookup_api_sample.json)
- [API][IP Address to ASN API Response Sample](/ASN%20Database/ip_address_to_asn_api_sample.json)

# Guides, Resources & Links

## Links

🔗 [ASN Database Page](https://ipinfo.io/products/asn-database)

🔗 [ASN Data Downloads Documentation](https://ipinfo.io/developers/asn-database)

🔗 [ASN API Page](https://ipinfo.io/products/asn-api)

🔗 [ASN API Documentation](https://ipinfo.io/developers/asn)

🔗 [ASN Data Type Documentation](https://ipinfo.io/developers/data-types#asn-data)

If you have any questions about using our data, feel free to ask us about it in the [IPinfo Community](https://community.ipinfo.io/).

## FAQs (Frequently Asked Questions)

- [IPinfo Community posts tagged as `ASN`](https://community.ipinfo.io/tag/asn)
- [Choosing between the ASN, IP to ASN and IP to Company database](https://community.ipinfo.io/t/choosing-between-the-asn-ip-to-asn-and-ip-to-company-database/731)
- [Differences in data for the ASN and the IP to Company database](https://community.ipinfo.io/t/differences-in-data-for-the-asn-and-the-ip-to-company-database/730)
- [What is an autonomous system (ASN)?](https://ipinfo.io/faq/article/40-what-is-an-autonomous-system-asn)

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)