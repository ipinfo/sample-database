# Privacy Detection

## IP Address to privacy detection database with detection method

IPinfo's IP Address to Privacy Detection (Extended) database includes IP addresses that have been used by VPNs, proxies, relays, TOR and hosting services that can be used to hide a user's location. The database showcases how detect the privacy service associated with an IP address.

# Database Schema & Description

*[data updated as of May, 2023]*

The following database schema represents the CSV database. We also provide JSON and MMDB format data.

| Fields            | Example       | Description                                                                                                                          |
|-------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `start_ip`        | 62.182.99.0   | First IP address of the range                                                                                                        |
| `end_ip`          | 62.182.99.255 | Last IP address of the range                                                                                                         |
| `join_key`        | 62.182.0.0    | Specialized variable to facilitate join operation                                                                                    |
| `hosting`         | False         | Indicates hosting service IP address (data center, cloud service, bots, scrapers,  etc.)                                             |
| `proxy`           | False         | IP address associated with a proxy service                                                                                           |
| `tor`             | False         | Tor exit node IP address                                                                                                             |
| `vpn`             | True          | IP address associated with a VPN service                                                                                             |
| `relay`           | False         | Private relay service IP address (Apple relay, Cloudflare, Akamai etc.)                                                              |
| `vpn_name`        | NordVPN       | Name of the privacy service provider includes VPN, Proxy and Relay service providers names                                           |
| `anycast`         | False         | True: if IP is indentified as being any anycast IP, that could map to multiple physical servers in different locations               |
| `census`          | True          | True: if we've indentified VPN software running on this IP as part of our internet wide scan (successful openvpn or ipsec handshake) |
| `device_activity` | True          | True: if we've seen VPN-like behavior (multiple devices, multiple locations etc)                                                     |
| `whois`           | False         | True: if we've seen vpn provider attributes in the IP whois data (eg. provider name)                                                 |
| `vpn_config`      | True          | True: if we've identified this IP in a VPN config file                                                                               |
| `census_port`     | 500           | Port number we've identified VPN software running on                                                                                 |


> `join_key` → This key represents the Class C network each IP address is part of, allowing you to filter the result set significantly before filtering to the exact IP address you want.


# Samples

- [CSV Database] [Privacy Detection (Extended) Database Sample](/Privacy%20Detection%20Extended/privacy_detection_extended_sample.csv)
- [JSON Database] [Privacy Detection (Extended) Database Sample](/Privacy%20Detection%20Extended/privacy_detection_extended_sample.json)
- [MMDB Database] [Privacy Detection (Extended) Database Sample](/Privacy%20Detection%20Extended/privacy_detection_extended_sample.mmdb)

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfoio) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)