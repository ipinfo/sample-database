# IPinfo Standard Database

## IPinfo's Standard is a robust IP database that combines our location, ASN, network flags data in a single database.

# Database Schema & Description

| Field Name         | Example                         | Data Type | Descrption                                                                  |
|--------------------|---------------------------------|-----------|-----------------------------------------------------------------------------|
| **network**        | `66.202.64.131`                 | TEXT      | CIDR/IP range or single IP address                                          |
| **city**           | `Chicago`                       | TEXT      | City of the IP address                                                      |
| **region**         | `Illinois`                      | TEXT      | Region/State of the IP address                                              |
| **region_code**    | `IL`                            | TEXT      | Region code in two-letter format in ISO 3166                                |
| **country**        | `United States`                 | TEXT      | Name of the country of the IP address                                       |
| **country_code**   | `US`                            | TEXT      | ISO 3166 country code of the IP address                                     |
| **continent**      | `North America`                 | TEXT      | Name of the continent                                                       |
| **continent_code** | `NA`                            | TEXT      | Continent name code in two-letter format                                    |
| **latitude**       | `41.85003`                      | FLOAT     | Latitude value of the IP address                                            |
| **longitude**      | `-87.65005`                     | FLOAT     | Longitude value of the IP address                                           |
| **timezone**       | `America/Chicago`               | TEXT      | Local timezone of the IP address location                                   |
| **postal_code**    | `60666`                         | TEXT      | Postal code or zip code of the IP address                                   |
| **asn**            | `AS7029`                        | TEXT      | Autonomous System Number (ASN)                                              |
| **as_name**        | `Windstream Communications LLC` | TEXT      | Organization domain name of the ASN                                         |
| **as_domain**      | `windstream.com`                | TEXT      | Name of the ASN organization                                                |
| **as_type**        | `isp`                           | TEXT      | ASN Type: ISP, Hosting, Education, Government or Business                   |
| **is_anonymous**        | `false`                         | BOOLEAN   | Indicates whether the IP address is anonymous.                              |
| **is_anycast**     | `false`                         | BOOLEAN   | dicates whether the IP address is an internet service hosting IP address    |
| **is_hosting**     | `false`                         | BOOLEAN   | Indicates whether the IP address is an hosting/cloud/data center IP address |
| **is_mobile**      | `false`                         | BOOLEAN   | Indicates whether the IP address belongs to a mobile network                |
| **is_satellite**   | `false`                         | BOOLEAN   | Indicates whether the IP address is part of a satellite internet connection |



## Samples

- [CSV Database] [IPinfo Standard Sample](/IPinfo%20Standard/ipinfo_standard_sample.csv)
- [JSON Database] [IPinfo Standard Sample](/IPinfo%20Standard/ipinfo_standard_sample.json)
- [MMDB Database] [IPinfo Standard Sample](/IPinfo%20Standard/ipinfo_standard_sample.mmdb)

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
| CSV         | ipinfo_standard.csv.gz  | `curl -L https://ipinfo.io/data/ipinfo_standard.csv.gz?token=$YOUR_TOKEN -o ipinfo_standard.csv.gz`   |
| MMDB        | ipinfo_standard.mmdb    | `curl -L https://ipinfo.io/data/ipinfo_standard.mmdb?token=$YOUR_TOKEN -o ipinfo_standard.mmdb`       |
| JSON        | ipinfo_standard.json.gz | `curl -L https://ipinfo.io/data/ipinfo_standard.json.gz?token=$YOUR_TOKEN -o ipinfo_standard.json.gz` |
| Parquet     | ipinfo_standard.parquet | `curl -L https://ipinfo.io/data/ipinfo_standard.parquet?token=$YOUR_TOKEN -o ipinfo_standard.parquet` |

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)