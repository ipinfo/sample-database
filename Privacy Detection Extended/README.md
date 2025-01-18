# Privacy Detection Extended Database

## IP Address to privacy detection database with detection method

IPinfo's IP Address to Privacy Detection (Extended) database includes IP addresses that have been used by VPNs, proxies, relays, TOR and hosting services that can be used to hide a user's location. The database showcases how detect the privacy service associated with an IP address.

# Database Schema & Description

*[data updated as of January, 2025]*

| Field Name          | Example         | Data Type | Descrption                                                                                                                                                                                                                                                                                                                            |
| ------------------- | --------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **network**         | `45.129.35.234` | TEXT      | CIDR/IP Range or single IP address block                                                                                                                                                                                                                                                                                              |
| **hosting**         | `true`          | BOOLEAN   | Indicates a hosting/cloud service/data center IP address                                                                                                                                                                                                                                                                              |
| **proxy**           | `false`         | BOOLEAN   | Indicates a open web proxy IP address                                                                                                                                                                                                                                                                                                 |
| **relay**           | `false`         | BOOLEAN   | Indicates location preserving anonymous relay service                                                                                                                                                                                                                                                                                 |
| **tor**             | `false`         | BOOLEAN   | Indicates a TOR (The Onion Router) exit node IP address                                                                                                                                                                                                                                                                               |
| **vpn**             | `true`          | BOOLEAN   | Indicates Virtual Private Network (VPN) service exit node IP address                                                                                                                                                                                                                                                                  |
| **service**         | `NordVPN`       | TEXT      | Name of the privacy service provider includes VPN, Proxy and Relay service providers names                                                                                                                                                                                                                                            |
| **first_seen**      | `2024-10-31`    | DATE      | Date when the activity on an anonymous IP address was first observed: Date in YYYY-MM-DD format, ISO-8601. Within the 3-month lookback period.                                                                                                                                                                                        |
| **last_seen**       | `2025-01-03`    | DATE      | Date when the activity on an anonymous IP address was last/recently observed: Date in YYYY-MM-DD format, ISO-8601.                                                                                                                                                                                                                    |
| **confidence**      | `3`             | INTEGER   | The level (from 1 to 3) of confidence attributed to the best source associated with this range                                                                                                                                                                                                                                        |
| **coverage**        | `1.0`             | FLOAT   | For inferred ranges (see `inferred` flag), represents the proportion of the range (in IP count) that we saw direct evidence of VPN activity on; the remaining percentage of the range (1 - coverage) is composed of IPs we did not directly observe. For IPs/ranges we've fully directly observed VPN evidence on, this value is 1.0. |
| **census**          | `false`         | BOOLEAN   | Ranges where we've observed VPN software/ports on; we run scans on ports and protocols commonly associated with VPN software. Ranges with the census flag are those where these scans obtained positive results                                                                                                                       |
| **census_ports**    | ``              | INTEGER   | The ports we've gotten positive results for when running our VPN detection census                                                                                                                                                                                                                                                     |
| **device_activity** | `false`         | BOOLEAN   | Ranges on which we've observed device activity compatible with VPN usage (outside of known infrastructure area; simultaneous use around a large area; pingable and/or associated with hosting providers)                                                                                                                              |
| **inferred**        | `false`         | BOOLEAN   | Whether the range associated with the record is the result of direct observation or inference based on neighboring IPs                                                                                                                                                                                                                |
| **vpn_config**      | `true`          | BOOLEAN   | Ranges where we confirmed VPN activity by directly running VPN software from almost 200 different providers and collecting exit IPs                                                                                                                                                                                                   |
| **whois**           | `false`         | BOOLEAN   | Ranges where we've observed VPN software/ports on AND have a WHOIS association with either VPNs in general or specific VPN providers. e.g. if our ipsec scan returned a positive result for an IP and its WHOIS record indicates that it is owned by a VPN provider, this flag will be true.                                          |

> Note that the `network` field can contain either CIDR-noted ranges or individual IP addresses.

Confidence intervals defined:

| Confidence Level | Description                                                                                                                                                                                                                                                                                                            |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **3**            | Direct observation of commercial use (vpn_config)                                                                                                                                                                                                                                                                      |
| **2**            | Direct observation of VPN software running on the range (census) + registrar information associated with VPNs or specific providers OR highly convincing device activity (large spread of devices on pingable networks that are not associated with carrier traffic and known to be associated with hosting providers) |
| **1**            | Direct observation of VPN software running on the range (census) without known association to specific providers or VPNs in general OR device data that is suspicious but not associated with hosting ranges                                                                                                           |

## Samples

- [CSV Database] [Privacy Extended Detection Database Sample](/Privacy%20Detection/ipinfo_privacy_extended_sample.csv)
- [JSON Database] [Privacy Extended Detection Database Sample](/Privacy%20Detection/ipinfo_privacy_extended_sample.json)
- [MMDB Database] [Privacy Extended Detection Database Sample](/Privacy%20Detection/ipinfo_privacy_extended_sample.mmdb)
- [CSV Database] [Privacy Extended Detection Database (Older Version) Sample](/Privacy%20Detection/privacy_detection_extended_sample.csv)
- [JSON Database] [Privacy Extended Detection Database (Older Version) Sample](/Privacy%20Detection/privacy_detection_extended_sample.json)
- [MMDB Database] [Privacy Extended Detection Database (Older Version) Sample](/Privacy%20Detection/privacy_detection_extended_sample.mmdb)

## Downloadable File Formats

- CSV: Plain text file format where data is organized into rows, with individual values separated by commas.
- JSON: More specifically, NDJSON (Newline Delimited JSON), a text file format where each line is a separated in valid JSON object.
- MMDB: Specialized binary database for efficient and fast IP lookups.
- Parquet: A columnar storage file format optimized for efficient data querying.

> Please refer to "[How to choose the best file format for your IPinfo database?](https://ipinfo.io/blog/ipinfo-database-formats/)" article to select the best format possible for your use case.
>
> The usage of the IP data downloads relies on the software or application of the data. Check out our [documentation](https://ipinfo.io/developers/database-download), [community](https://community.ipinfo.io/c/docs/8), and our [integrations](https://ipinfo.io/integrations) pages to find the best path forward.

## Filename references:


| File Format | Filename / Slug                 | Terminal Command                                                                                                      |
| ----------- | ------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| CSV         | ipinfo_privacy_extended.csv.gz  | `curl -L https://ipinfo.io/data/ipinfo_privacy_extended.csv.gz?token=$YOUR_TOKEN -o ipinfo_privacy_extended.csv.gz`   |
| MMDB        | ipinfo_privacy_extended.mmdb    | `curl -L https://ipinfo.io/data/ipinfo_privacy_extended.mmdb?token=$YOUR_TOKEN -o ipinfo_privacy_extended.mmdb`       |
| JSON        | ipinfo_privacy_extended.json.gz | `curl -L https://ipinfo.io/data/ipinfo_privacy_extended.json.gz?token=$YOUR_TOKEN -o ipinfo_privacy_extended.json.gz` |
| Parquet     | ipinfo_privacy_extended.parquet | `curl -L https://ipinfo.io/data/ipinfo_privacy_extended.parquet?token=$YOUR_TOKEN -o ipinfo_privacy_extended.parquet` |

## Links

🔗 [IP to Privacy Detection Extended Data Downloads Documentation](https://ipinfo.io/developers/privacy-detection-extended)

The IP to Privacy Detectio Extended Dataset is a customized product available only through request. [Reach out to our sales team to get started](https://ipinfo.io/contact).

## Articles & Guides

- [Deep dive into privacy detection data and masked IPs](https://ipinfo.io/blog/deep-dive-into-privacy-detection-data-and-masked-ips/)
- [How to privacy-proof your online targeting](https://ipinfo.io/blog/privacy-adtech-online-targeting/)
- [5 businesses who use privacy detection data well](https://ipinfo.io/blog/using-privacy-detection-data/)
- [What to expect from our Privacy Detection API](https://ipinfo.io/blog/what-to-expect-from-our-privacy-detection-api/)

## FAQ (Frequently Asked Questions)

- [IPinfo Community posts tagged as `ip-privacy-detection`](https://community.ipinfo.io/tag/ip-privacy-detection)
- [Why the provider’s name is sometimes is missing from our IP to privacy detection data?](https://community.ipinfo.io/t/why-the-provider-s-name-is-sometimes-is-missing-from-our-ip-to-privacy-detection-data/1719)
- [Do we provide a confidence score for our IP to Privacy data?](https://community.ipinfo.io/t/do-we-provide-a-confidence-score-for-our-ip-to-privacy-data/1723)
- [How we classify IP addresses in the IP to Privacy Detection Dataset](https://community.ipinfo.io/t/how-we-classify-ip-addresses-in-the-ip-to-privacy-detection-dataset/5573)
- [Preventing bot activity with IPinfo’s IP to Privacy Data](https://community.ipinfo.io/t/preventing-bot-activity-with-ipinfos-ip-to-privacy-data/1811)
- [Difference between proxy and VPN according to our privacy detection](https://community.ipinfo.io/t/difference-between-proxy-and-vpn-according-to-our-privacy-detection/5604)
- [Why are some IP addresses not always flagged in the privacy detection data?](https://community.ipinfo.io/t/why-are-some-ip-addresses-not-always-flagged-in-the-privacy-detection-data/5626)
- [Getting IP data from anonymous IP addresses](https://community.ipinfo.io/t/getting-ip-data-from-anonymous-ip-addresses/1743)
- [Preventing Ad Fraud using IPinfo’s data](https://community.ipinfo.io/t/preventing-ad-fraud-using-ipinfo-s-data/5591)
- [Anonymous or masked IP address](https://ipinfo.io/faq/article/83-anonymous-or-masked-ip-address)
- [What is Tor?](https://ipinfo.io/faq/article/81-what-is-tor)
- [What is a proxy?](https://ipinfo.io/faq/article/82-what-is-proxy)
- [What is a VPN?](https://ipinfo.io/faq/article/80-what-is-vpn)

If you have any questions about using our data, feel free to ask us about it in the [IPinfo Community](https://community.ipinfo.io/).

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)
