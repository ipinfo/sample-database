# IP to Device Count Database

## Track how many devices share an IP and whether sharing is concurrent or rotating over time.

The [IP to Device Count dataset](/data/device-count) provides network-level intelligence on how many devices share an IP address and whether that sharing is concurrent or rotating over time. This goes far beyond simple "[residential](/data/ip-asn)" or "[mobile](/data/ip-carrier)" labels. The IP to Device Count database reveals whether an IP is used by 1 device, 10, or 10,000+, and whether that sharing happens all at once (concurrent CGNAT) or one device at a time with ISP rotation (dynamic residential).

The database covers currently (as of April 10, 2026) 7.7 million networks globally, with 1.3 million networks exhibiting daily device sharing patterns, and includes validated coverage for major carriers worldwide.

> **Status:** Alpha (Early Access)

# Database Schema & Description

| Field Name            | Example             | Data Type | Descrption                                                                                                                                               |
| --------------------- | ------------------- | --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **network**           | `103.89.82.50/32`   | TEXT      | IP network range (CIDR notation) associated with the device count observation.                                                                          |
| **asn**               | `AS10214`           | TEXT      | Autonomous System Number identifying the network owner/operator.                                                                                        |
| **shared**            | `daily`             | TEXT      | Shortest time window where significant sharing (>=10 devices) is observed: `daily`, `weekly`, or `monthly`. Indicates whether sharing is concurrent or rotating. |
| **devices_daily**     | `10`                | INTEGER   | Observed unique devices per day (logarithmic bucket: 1, 10, 100, 1000, 10000, 100000). Represents order-of-magnitude device count.                   |
| **devices_weekly**    | `10`                | INTEGER   | Observed devices over 7 days (logarithmic bucket: 1, 10, 100, 1000, 10000, 100000). Used for campaign-duration measurement.                           |
| **devices_monthly**   | `100`               | INTEGER   | Observed devices over 30 days (logarithmic bucket: 1, 10, 100, 1000, 10000, 100000). Used for list validation and long-term attribution.              |

## Logarithmic Device Count Buckets

| Devices  | Category       | Description                                                        | Example                              |
| -------- | -------------- | ------------------------------------------------------------------ | ------------------------------------ |
| 1        | Single device  | Individual connection, typically one household device              | Home broadband, personal hotspot     |
| 10       | Small shared   | Small shared network, household, small office, or dynamic rotation | Family router, small business        |
| 100      | Medium shared  | Medium shared network, business, apartment building, or MDU        | Enterprise office, apartment complex |
| 1,000    | Large shared   | Large shared network, enterprise, university, or cellular CGNAT    | University campus, carrier CGNAT     |
| 10,000   | Carrier-scale  | Regional CGNAT pools, large carrier infrastructure                 | Spark NZ, NTT Docomo                 |
| 100,000  | Hyper-scale    | Massive concurrent sharing, the largest CGNAT pools globally       | TPG Telecom (AU), Bell Canada        |

**Why logarithmic?** The difference between 8,500 and 9,200 devices sharing an IP is less meaningful than the difference between 10 and 100. Order-of-magnitude buckets capture the signal that matters.

## Time Windows

| Window       | Interpretation                   | Primary Use Case                                 |
| ------------ | -------------------------------- | ------------------------------------------------ |
| **Daily**    | Devices observed in 24 hours     | Security blast radius, real-time blocking        |
| **Weekly**   | Devices observed over 7 days     | Campaign-duration measurement, short-term use    |
| **Monthly**  | Devices observed over 30 days    | List validation, attribution, long-term patterns |

### How to Read Across Windows

| Pattern                      | Daily  | Weekly | Monthly | Interpretation                                                                                                               |
| ---------------------------- | ------ | ------ | ------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Dynamic IP with rotation     | 1      | 1      | 10      | Dynamic residential IP. One device at a time, but ISP rotates assignments over the month.                                  |
| Concurrent CGNAT sharing     | 100+   | 100+   | 100+    | Concurrently shared infrastructure (CGNAT, VPN, university). High blast radius for blocking.                               |
| Growing rotation             | 1      | 10     | 100     | ISP-managed dynamic pool with increasing rotation velocity.                                                                  |

The **shared** field indicates the shortest window where >=10 devices are observed:

- `daily` = concurrent sharing (high coverage radius)
- `weekly` = moderate rotation
- `monthly` = slow rotation (likely sequential)

## Samples

- [CSV Database] [IP to Device Count Sample](/IP%20to%20Device%20Count/device_count_v2_sample.csv)
- [JSON Database] [IP to Device Count Sample](/IP%20to%20Device%20Count/device_count_v2_sample.json)
- [MMDB Database] [IP to Device Count Sample](/IP%20to%20Device%20Count/device_count_v2_sample.mmdb)
- [Parquet Database] [IP to Device Count Sample](/IP%20to%20Device%20Count/device_count_v2_sample.parquet)

## Downloadable File Formats

- CSV: Plain text file format where data is organized into rows, with individual values separated by commas.
- JSON: More specifically, NDJSON (Newline Delimited JSON), a text file format where each line is a separated in valid JSON object.
- MMDB: Specialized binary database for efficient and fast IP lookups.
- Parquet: A columnar storage file format optimized for efficient data querying.

> Please refer to "[How to choose the best file format for your IPinfo database?](https://ipinfo.io/blog/ipinfo-database-formats/)" article to select the best format possible for your use case.
>
> The usage of the IP data downloads relies on the software or application of the data. Check out our [documentation](https://ipinfo.io/developers/database-download), [community](https://community.ipinfo.io/c/docs/8), and our [integrations](https://ipinfo.io/integrations) pages to find the best path forward.

## Filename references:

| File Format | Filename / Slug             | Terminal Command                                                                                                  |
| ----------- | --------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| CSV         | device_count_v2.csv.gz      | `curl -L https://ipinfo.io/data/device_count_v2.csv.gz?token=$YOUR_TOKEN -o device_count.csv.gz`                  |
| MMDB        | device_count_v2.mmdb        | `curl -L https://ipinfo.io/data/device_count_v2.mmdb?token=$YOUR_TOKEN -o device_count.mmdb`                      |
| JSON        | device_count_v2.json.gz     | `curl -L https://ipinfo.io/data/device_count_v2.json.gz?token=$YOUR_TOKEN -o device_count.json.gz`                |
| Parquet     | device_count_v2.parquet     | `curl -L https://ipinfo.io/data/device_count_v2.parquet?token=$YOUR_TOKEN -o device_count.parquet`                |

## Request Early Access

Device Count is currently in alpha with limited availability. To request access:

1. Visit [https://ipinfo.io/data/device-count](https://ipinfo.io/data/device-count#form)
2. Fill out the early access request form
3. Specify your primary use case and expected usage volume

Priority is given to companies with active use cases in security, ad tech, data quality, or network operations who can commit to testing and feedback.

### Alpha Status

- Schema field names are exploratory and may change
- Data refresh cadence is weekly (faster updates planned)
- Coverage is global but may be incomplete in some regions
- Early access is limited to selected customers

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it's fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)