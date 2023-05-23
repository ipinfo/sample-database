# Privacy Detection

## IP Address to privacy detection database with detection method

IPinfo's IP Address to Privacy Detection (Extended) database includes IP addresses that have been used by VPNs, proxies, relays, TOR and hosting services that can be used to hide a user's location. The database showcases how detect the privacy service associated with an IP address.

# Database Schema & Description

*[data updated as of May, 2023]*

The following database schema represents the CSV database. We also provide JSON and MMDB format data.

| Fields          | Example        | Description                                                                              |
|-----------------|----------------|------------------------------------------------------------------------------------------|
| start_ip        | 185.164.34.246 | First IP address of the range                                                            |
| end_ip          | 185.164.34.246 | Last IP address of the range                                                             |
| hosting         | True           | Indicates hosting service IP address (Bots, scrapers, data center, cloud service etc.)   |
| proxy           | False          | IP address associated with a proxy service                                               |
| tor             | False          | Tor exit node IP address                                                                 |
| vpn             | False          | IP address associated with a VPN service                                                 |
| relay           | Zenmate        | Private relay service IP address (Apple relay, android, firefox etc.)                    |
| service         | False          | Name of the privacy service provider                                                     |
| census          | True           | True: if we've detected this via our VPN scans (successful openvpn or ipsec handshake)   |
| device_activity | False          | True: if we've seen VPN-like activity (multiple devices, multiple locations etc)         |
| whois           | False          | True: if we've seen vpn provider attributes in the IP whois data (eg. provider name)     |
| vpn_config      | True           |                                                                                          |
| census_port     | 443,500        | True: if we've seen this IP in a VPN provider config or their API                        |
| vpn_name        | False          | Name of the provider, if available (eg. inferred from whois, hostname, or source config) |

> `join_key` → This key represents the Class C network each IP address is part of, allowing you to filter the result set significantly before filtering to the exact IP address you want. [[*Source*](https://ipinfo.io/blog/ingesting-ipinfo-geolocation-data-with-postgresql-13/)]


# Samples

- [CSV Database] [Privacy Detection (Extended) Database Sample](/Privacy%20Detection%20Extendedprivacy_detection_extended_sample.csv)
- [JSON Database] [Privacy Detection (Extended) Database Sample](/Privacy%20Detection%20Extended/privacy_detection_extended_sample.json)
- [MMDB Database] [Privacy Detection (Extended) Database Sample](/Privacy%20Detection%20Extended/privacy_detection_extended_sample.mmdb)

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfoio) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)