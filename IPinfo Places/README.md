# IPinfo Places Database

## IPinfo Places maps IP addresses to real-world venues and buildings where they are observed.

The [IPinfo Places](/data/places) database maps IP addresses to the real-world venues and buildings they are observed on, including hotels, airports, museums, stadiums, transit stations, and 30+ other location categories. Each record links an IP to a verified physical place, the Wi-Fi SSID observed at that venue, and the building-level coordinates of the matched place.

The database is built on top of active measurements and curated GIS data, allowing customers to enrich IP data with venue context for security, ad tech, fraud prevention, and audience analytics use cases.

> **Status:** Enterprise Beta
>
> **Available formats/slugs:** `poi_all` and `poi_all_extended`

# Database Schema & Description

## IPinfo Places (`poi_all`)

| Field Name     | Example                               | Data Type | Descrption                                                                                            |
| -------------- | ------------------------------------- | --------- | ----------------------------------------------------------------------------------------------------- |
| **ip**         | `65.144.40.106`                       | TEXT      | The IP address associated with the venue observation.                                                 |
| **ssid**       | `MOHAI-Guest`                         | TEXT      | The Wi-Fi network name (SSID) observed at the venue.                                                  |
| **category**   | `museum`                              | TEXT      | The location category tag for the venue. See the Places documentation for supported categories.       |
| **name**       | `Museum of History and Industry`      | TEXT      | The name of the venue or building associated with the IP address. Can identify the brand or operator. |
| **brand**      | `null`                                | TEXT      | The brand associated with the venue when available.                                                    |
| **latitude**   | `47.6275`                             | FLOAT     | The latitude coordinate of the matched place at building level.                                       |
| **longitude**  | `-122.3367`                           | FLOAT     | The longitude coordinate of the matched place at building level.                                      |

## IPinfo Places (Extended) (`poi_all_extended`)

| Field Name       | Example                                 | Data Type | Descrption                                                                                            |
| ---------------- | --------------------------------------- | --------- | ----------------------------------------------------------------------------------------------------- |
| **ip**           | `1.0.140.55`                            | TEXT      | The IP address associated with the venue observation.                                                 |
| **bssid**        | `14:4d:67:a1:45:bc,30:16:9d:75:3b:82`   | TEXT      | Comma-separated Wi-Fi BSSID values observed at the venue.                                             |
| **ssid**         | `Rimnan4`                               | TEXT      | The Wi-Fi network name (SSID) observed at the venue.                                                  |
| **category**     | `hotel`                                 | TEXT      | The location category tag for the venue. See the Places documentation for supported categories.       |
| **name**         | `Ruean Rim Nan เรือนริมน่าน`          | TEXT      | The name of the venue or building associated with the IP address. Can identify the brand or operator. |
| **brand**        | `null`                                  | TEXT      | The brand associated with the venue when available.                                                    |
| **city**         | `Taphan Hin`                            | TEXT      | City of the matched place.                                                                            |
| **region**       | `Phichit`                               | TEXT      | Region or state of the matched place.                                                                 |
| **country_code** | `TH`                                    | TEXT      | ISO 3166 two-letter country code of the matched place.                                                |
| **latitude**     | `16.225`                                | FLOAT     | The latitude coordinate of the matched place at building level.                                       |
| **longitude**    | `100.4188`                              | FLOAT     | The longitude coordinate of the matched place at building level.                                      |

## Samples

### IPinfo Places (`poi_all`)

- [CSV Database] [IPinfo Places Sample](/IPinfo%20Places/poi_all_sample.csv)
- [JSON Database] [IPinfo Places Sample](/IPinfo%20Places/poi_all_sample.json)
- [MMDB Database] [IPinfo Places Sample](/IPinfo%20Places/poi_all_sample.mmdb)
- [Parquet Database] [IPinfo Places Sample](/IPinfo%20Places/poi_all_sample.parquet)

### IPinfo Places (Extended) (`poi_all_extended`)

- [CSV Database] [IPinfo Places Extended Sample](/IPinfo%20Places/poi_all_extended_sample.csv)
- [JSON Database] [IPinfo Places Extended Sample](/IPinfo%20Places/poi_all_extended_sample.json)
- [MMDB Database] [IPinfo Places Extended Sample](/IPinfo%20Places/poi_all_extended_sample.mmdb)
- [Parquet Database] [IPinfo Places Extended Sample](/IPinfo%20Places/poi_all_extended_sample.parquet)

## Downloadable File Formats

- CSV: Plain text file format where data is organized into rows, with individual values separated by commas.
- JSON: More specifically, NDJSON (Newline Delimited JSON), a text file format where each line is a separated in valid JSON object.
- MMDB: Specialized binary database for efficient and fast IP lookups.
- Parquet: A columnar storage file format optimized for efficient data querying.

> Please refer to "[How to choose the best file format for your IPinfo database?](https://ipinfo.io/blog/ipinfo-database-formats/)" article to select the best format possible for your use case.
>
> The usage of the IP data downloads relies on the software or application of the data. Check out our [documentation](https://ipinfo.io/developers/database-download), [community](https://community.ipinfo.io/c/docs/8), and our [integrations](https://ipinfo.io/integrations) pages to find the best path forward.

## Filename references:

### IPinfo Places (`poi_all`)

| File Format | Filename / Slug   | Terminal Command                                                                                |
| ----------- | ----------------- | ----------------------------------------------------------------------------------------------- |
| CSV         | poi_all.csv.gz    | `curl -L https://ipinfo.io/data/poi_all.csv.gz?token=$YOUR_TOKEN -o poi_all.csv.gz`             |
| MMDB        | poi_all.mmdb      | `curl -L https://ipinfo.io/data/poi_all.mmdb?token=$YOUR_TOKEN -o poi_all.mmdb`                 |
| JSON        | poi_all.json.gz   | `curl -L https://ipinfo.io/data/poi_all.json.gz?token=$YOUR_TOKEN -o poi_all.json.gz`           |
| Parquet     | poi_all.parquet   | `curl -L https://ipinfo.io/data/poi_all.parquet?token=$YOUR_TOKEN -o poi_all.parquet`           |

### IPinfo Places (Extended) (`poi_all_extended`)

| File Format | Filename / Slug             | Terminal Command                                                                                                  |
| ----------- | --------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| CSV         | poi_all_extended.csv.gz     | `curl -L https://ipinfo.io/data/poi_all_extended.csv.gz?token=$YOUR_TOKEN -o poi_all_extended.csv.gz`             |
| MMDB        | poi_all_extended.mmdb       | `curl -L https://ipinfo.io/data/poi_all_extended.mmdb?token=$YOUR_TOKEN -o poi_all_extended.mmdb`                 |
| JSON        | poi_all_extended.json.gz    | `curl -L https://ipinfo.io/data/poi_all_extended.json.gz?token=$YOUR_TOKEN -o poi_all_extended.json.gz`           |
| Parquet     | poi_all_extended.parquet    | `curl -L https://ipinfo.io/data/poi_all_extended.parquet?token=$YOUR_TOKEN -o poi_all_extended.parquet`           |

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it's fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)