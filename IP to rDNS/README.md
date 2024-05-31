# IP to rDNS (Reverse DNS) resolution

## A comprehensive dataset of IP address and rDNS resolution, mapping between IP addresses and corresponding hostnames and domains.

# Database Schema & Description

*[data updated as of March, 2024]*

The IP to rDNS dataset contain two datasets.

## IP to rDNS - Domains dataset

| Field Name | Example         | Data Type | Notes                                            |
|------------|-----------------|-----------|--------------------------------------------------|
| `start_ip` | 38.80.229.1     | TEXT      | Starting IP address of an IP address range       |
| `end_ip`   | 38.80.229.255   | TEXT      | Ending IP address of an IP address range         |
| `join_key` | 38.80.0.0       | TEXT      | Special variable to facilitate IP join operation |
| `size`     | 255             | INTEGER   | Size of the IP range                             |
| `domain`   | digitalpath.net | TEXT      | Associated rDNS domain                           |


##  IP to rDNS - Hostname dataset

| Field Name | Example        | Data Type | Notes               |
|------------|----------------|-----------|---------------------|
| `ip`       | 161.163.44.195 | TEXT      | IP address          |
| `hostname` | walmart.com    | TEXT      | Associated hostname |

# Samples

- [CSV Database] [IP to rDNS - Domains Database Sample](/IP%20to%20rDNS/ip_rdns_domains_sample.csv)
- [JSON Database] [IP to rDNS - Domains Database Sample](/IP%20to%20rDNS/ip_rdns_domains_sample.json)
- [MMDB Database] [IP to rDNS - Domains Database Sample](/IP%20to%20rDNS/ip_rdns_domains_sample.mmdb)
- [CSV Database] [IP to rDNS - Hostnames Database Sample](/IP%20to%20rDNS/ip_rdns_hostnames_sample.csv)
- [JSON Database] [IP to rDNS - Hostnames Database Sample](/IP%20to%20rDNS/ip_rdns_hostnames_sample.json)
- [MMDB Database] [IP to rDNS - Hostnames Database Sample](/IP%20to%20rDNS/ip_rdns_hostnames_sample.mmdb)

If you have any questions about using our data, feel free to ask us about it in the [IPinfo Community](https://community.ipinfo.io/).

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)