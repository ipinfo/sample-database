CIDR/IP range or single IP address

# IPinfo Plus Database

## IPinfo's Plus is an enterprise-grade IP database that combines our location, insights, and confidence with ASN, privacy, carrier, and network flags in a single database.

# Database Schema & Description

| Field Name         | Example                        | Data Type | Descrption                                                                                                 |
| ------------------ | ------------------------------ | --------- | ---------------------------------------------------------------------------------------------------------- |
| network            | 86.179.219.192/29              | TEXT      | CIDR/IP range or single IP address                                                                         |
| city               | Weymouth                       | TEXT      | City of the IP address                                                                                     |
| region             | England                        | TEXT      | Region/State of the IP address                                                                             |
| region_code        | ENG                            | TEXT      | Region code in two-letter format in ISO 3166                                                               |
| country            | United Kingdom                 | TEXT      | Name of the country of the IP address                                                                      |
| country_code       | GB                             | TEXT      | ISO 3166 country code of the IP address                                                                    |
| continent          | Europe                         | TEXT      | Name of the continent                                                                                      |
| continent_code     | EU                             | TEXT      | Continent name code in two-letter format                                                                   |
| latitude           | 50.61448                       | FLOAT     | Latitude value of the IP address                                                                           |
| longitude          | -2.45991                       | FLOAT     | Longitude value of the IP address                                                                          |
| timezone           | Europe/London                  | TEXT      | Local timezone of the IP address location                                                                  |
| postal_code        | DT3                            | TEXT      | Postal code or zip code of the IP address                                                                  |
| dma_code           | 13w                            | TEXT      | Direct Marketing Area (DMA) is a unique regional identifier for marketing.                                 |
| geoname_id         | 2634202                        | INTEGER   | geonames.org's unique numercial identifier for geographic locations.                                       |
| radius             | 20                             | INTEGER   | Location accuracy radius in terms of kilometers                                                            |
| city_confidence    | high                           | TEXT      | Indicates the accuracy of city-level geolocation data.                                                     |
| region_confidence  | high                           | TEXT      | Indicates the accuracy of region or state level geolocation data.                                          |
| country_confidence | high                           | TEXT      | Indicates the accuracy of country level geolocation data.                                                  |
| asn                | AS2856                         | TEXT      | Autonomous System Number (ASN)                                                                             |
| as_name            | British Telecommunications PLC | TEXT      | Organization domain name of the ASN                                                                        |
| as_domain          | bt.com                         | TEXT      | Name of the ASN organization                                                                               |
| as_type            | isp                            | TEXT      | ASN Type: ISP, Hosting, Education, Government or Business                                                  |
| carrier_name       |                                | TEXT      | Name of the mobile carrier organization                                                                    |
| mcc                |                                | INTEGER   | Mobile Country Code (MCC) of the carrier                                                                   |
| mnc                |                                | INTEGER   | Mobile Network Code (MNC) of the carrier                                                                   |
| as_changed         | 2025-01-10                     | DATE      | Date when the IP address's ASN last changed: Date in YYYY-MM-DD format, ISO-8601                           |
| geo_changed        | 2024-11-10                     | DATE      | Date when the IP address's location last changed: Date in YYYY-MM-DD format, ISO-8601                      |
| as_stability       | 1.0                            | FLOAT     | The stability/change of ASN data for the IP address within a recent period of time. 1.0 means very stable. |
| geo_stability      | 1.0                            | FLOAT     | The stability/change of locaion for the IP address within a recent period of time. 1.0 means very stable.  |
| is_anon            | false                          | BOOLEAN   | Indicates whether the IP address is anonymous.                                                             |
| is_anycast         | false                          | BOOLEAN   | dicates whether the IP address is an internet service hosting IP address                                   |
| is_hosting         | false                          | BOOLEAN   | Indicates whether the IP address is an hosting/cloud/data center IP address                                |
| is_mobile          | false                          | BOOLEAN   | Indicates whether the IP address belongs to a mobile network                                               |
| is_satellite       | false                          | BOOLEAN   | Indicates whether the IP address is part of a satellite internet connection                                |
| is_proxy           | false                          | BOOLEAN   | Indicates a open web proxy IP address                                                                      |
| is_relay           | false                          | BOOLEAN   | Indicates location preserving anonymous relay service like iCloud private relay.                           |
| is_tor             | false                          | BOOLEAN   | Indicates a TOR (The Onion Router) exit node IP address                                                    |
| is_vpn             | false                          | BOOLEAN   | Indicates Virtual Private Network (VPN) service exit node IP address                                       |
| privacy_name       |                                | TEXT      | The name of the privacy service provider includes VPN, Proxy, or Relay service provider name               |
| cdn_name           |                                | TEXT      | Name of the CDN provider, if it is CDN IP address                                                          |


## Samples

- [CSV Database] [IPinfo Plus Sample](/Privacy%20Detection/ipinfo_plus_sample.csv)
- [JSON Database] [IPinfo Plus Sample](/Privacy%20Detection/ipinfo_plus_sample.json)
- [MMDB Database] [IPinfo Plus Sample](/Privacy%20Detection/ipinfo_plus_sample.mmdb)

## Downloadable File Formats

- CSV: Plain text file format where data is organized into rows, with individual values separated by commas.
- JSON: More specifically, NDJSON (Newline Delimited JSON), a text file format where each line is a separated in valid JSON object.
- MMDB: Specialized binary database for efficient and fast IP lookups.
- Parquet: A columnar storage file format optimized for efficient data querying.

> Please refer to "[How to choose the best file format for your IPinfo database?](https://ipinfo.io/blog/ipinfo-database-formats/)" article to select the best format possible for your use case.
>
> The usage of the IP data downloads relies on the software or application of the data. Check out our [documentation](https://ipinfo.io/developers/database-download), [community](https://community.ipinfo.io/c/docs/8), and our [integrations](https://ipinfo.io/integrations) pages to find the best path forward.

## Filename references:

| File Format | Filename / Slug     | Terminal Command                                                                              |
| ----------- | ------------------- | --------------------------------------------------------------------------------------------- |
| CSV         | ipinfo_plus.csv.gz  | `curl -L https://ipinfo.io/data/ipinfo_plus.csv.gz?token=$YOUR_TOKEN -o ipinfo_plus.csv.gz`   |
| MMDB        | ipinfo_plus.mmdb    | `curl -L https://ipinfo.io/data/ipinfo_plus.mmdb?token=$YOUR_TOKEN -o ipinfo_plus.mmdb`       |
| JSON        | ipinfo_plus.json.gz | `curl -L https://ipinfo.io/data/ipinfo_plus.json.gz?token=$YOUR_TOKEN -o ipinfo_plus.json.gz` |
| Parquet     | ipinfo_plus.parquet | `curl -L https://ipinfo.io/data/ipinfo_plus.parquet?token=$YOUR_TOKEN -o ipinfo_plus.parquet` |

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)