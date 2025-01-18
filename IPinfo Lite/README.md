# IPinfo Lite Database

## IPinfo's free IP datbaase that provides location (country + continent) and ASN information in a single database

The IPinfo Lite database is part of our [free IP data downloads offering](https://ipinfo.io/products/free-ip-database). The IPinfo Lite database is our ultimate free IP database combining both country and ASN information in a single database. Features of the IPinfo Lite database includes:

- Full accuracy with zero compromise. The dataset is updated daily to ensure the highest accuracy possible.
- The dataset is a merged subset of our premium [IP to Geolocation Database](https://ipinfo.io/products/ip-geolocation-database) and [ASN database](https://ipinfo.io/products/asn-database).
- It includes both IPv4 and IPv6 data in a single dataset.
- It includes both country and ASN information, which means that for each IP address query, you will receive both of these pieces of information.
- The data is tabular and unnested, making it extremely easy to use.
- Our free databases are licensed under CC-BY-SA 4.0.
- Comes in MMDB, CSV, and JSON formats.

# Database Schema & Description

*[data updated as of January, 2025]*

| Field Name         | Example                 | Data Type | Descrption                                                             |
|--------------------|-------------------------|-----------|------------------------------------------------------------------------|
| **network**        | `154.24.39.204/30`      | TEXT      | CIDR/IP range or single IP address                                              |
| **country**        | `Canada`                | TEXT      | Country name                                                           |
| **country_code**   | `CA`                    | TEXT      | Two-letter ISO 3166 country code of the IP addresses                   |
| **continent**      | `North America`         | TEXT      | Continent name of the IP location                                      |
| **continent_code** | `NA`                    | TEXT      | Two-letter continent code of the IP location                           |
| **asn**            | `AS174`                 | TEXT      | Autonomous System Number, an organization that owns the IP range block |
| **as_name**        | `Cogent Communications` | TEXT      | Name of the AS (Autonomous System Number) organization                 |
| **as_domain**      | `cogentco.com`          | TEXT      | Official domain or website of the ASN organization                     |

## Samples

- [CSV Database] [IPinfo Lite Sample](/IPinfo%20Lite/ipinfo_lite_sample.csv)
- [JSON Database] [IPinfo Lite Sample](/IPinfo%20Lite/ipinfo_lite_sample.json)
- [MMDB Database] [IPinfo Lite Sample](/IPinfo%20Lite/ipinfo_lite_sample.mmdb)

<details>

<summary><h3>Alternate Database Schema: <code>country_asn</code></h3></summary>

The `country_asn` data download is structured based on IP ranges (`start_ip` and `end_ip`). Our default data downloads has been updated (January, 2025) to use the `network`-based schema and also changes the name of the columns. However, we will continue supporting the original IP range-based schema for existing customers, with no plans for deprecation. While the underlying data remains the same, the difference lies only in the schema.

| Field Name       | Example                      | Data Type | Description                                       |
|------------------|------------------------------|-----------|---------------------------------------------------|
| `start_ip`       | 1.0.16.0                     | TEXT      | Starting IP address of an IP address range        |
| `end_ip`         | 1.0.31.255                   | TEXT      | Ending IP address of an IP address range          |
| `country`        | JP                           | TEXT      | ISO 3166 country code of the IP addresses         |
| `country_name`   | Japan                        | TEXT      | Name of the country                               |
| `continent`      | AS                           | TEXT      | Continent code of the country                     |
| `continent_name` | Asia                         | TEXT      | Name of the continent                             |
| `asn`            | AS2519                       | TEXT      | Autonomous System Number                          |
| `as_name`        | ARTERIA Networks Corporation | TEXT      | Name of the AS (Autonomous System) organization   |
| `as_domain`      | arteria-net.com              | TEXT      | Official domain or website of the AS organization |

> Includes IP range columns (`start_ip` and `end_ip`) instead of a network or CIDR based column (`network`).

#### Samples

- [CSV Database] [IP to Country + ASN Database Sample](/IP%20to%20Country%20ASN/ip_country_asn_sample.csv)
- [JSON Database] [IP to Country + ASN Database Sample](/IP%20to%20Country%20ASN/ip_country_asn_sample.json)
- [MMDB Database] [IP to Database + ASN Sample](/IP%20to%20Country%20ASN/ip_country_asn_sample.mmdb)

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

| File Format | Filename / Slug        | Terminal Command                                                                                    |
|-------------|------------------------|-----------------------------------------------------------------------------------------------------|
| CSV         | ipinfo_lite.csv.gz  | `curl -L https://ipinfo.io/data/ipinfo_lite.csv.gz?token=$YOUR_TOKEN -o ipinfo_lite.csv.gz`   |
| MMDB        | ipinfo_lite.mmdb    | `curl -L https://ipinfo.io/data/ipinfo_lite.mmdb?token=$YOUR_TOKEN -o ipinfo_lite.mmdb`       |
| JSON        | ipinfo_lite.json.gz | `curl -L https://ipinfo.io/data/ipinfo_lite.json.gz?token=$YOUR_TOKEN -o ipinfo_lite.json.gz` |
| Parquet     | ipinfo_lite.parquet | `curl -L https://ipinfo.io/data/ipinfo_lite.parquet?token=$YOUR_TOKEN -o ipinfo_lite.parquet` |

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)