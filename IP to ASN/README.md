# IP to ASN

## Get accurate ASN information of IP address range.

The IP to ASN database is part of our [free IP data downloads offering](https://ipinfo.io/products/free-ip-database). Features of the [IP to ASN free database](https://ipinfo.io/developers/ip-to-asn-database) includes:

- Full accuracy with zero compromise. The dataset is updated daily to ensure the highest accuracy possible.
- The dataset is a subset of our premium [ASN database](https://ipinfo.io/products/asn-database).
- The IP to ASN dataset provides ranges, ASN, AS name, and AS name domain.
- It includes both IPv4 and IPv6 data in a single dataset.
- The data is tabular and unnested, making it extremely easy to use.
- The IP to ASN dataset aggregates ranges by ASN, making it ideal for ASN to range lookups.
- Our free databases are licensed under CC-BY-SA 4.0.
- Comes in MMDB, CSV, and JSON formats.

# Database Schema & Description

*[data updated as of May, 2024]*

The following database schema represents the CSV database. We also provide JSON and MMDB format data.

| Field Name | Example            | Data Type | Description                                       |
|------------|--------------------|-----------|---------------------------------------------------|
| `start_ip` | 1.0.0.0            | TEXT      | Starting IP address of an IP address range        |
| `end_ip`   | 1.0.0.255          | TEXT      | Ending IP address of an IP address range          |
| `asn`      | AS13335            | TEXT      | Autonomous System Number                          |
| `name`     | Cloudflare, Inc.   | TEXT      | Name of the AS (Autonomous System) organization   |
| `domain`   | cloudflare.com     | TEXT      | Official domain or website of the AS organization |

# Samples

- [CSV Database] [IP to ASN Database Sample](/IP%20to%20ASN/ip_asn_sample.csv)
- [JSON Database] [IP to ASN Database Sample](/IP%20to%20ASN/ip_asn_sample.json)
- [MMDB Database] [IP to ASN Sample](/IP%20to%20ASN/ip_asn_sample.mmdb)

# Guides, Resources & Links

## Links

🔗 [IP to ASN Database Documentation](https://ipinfo.io/developers/ip-to-asn-database)

If you have any questions about using our data, feel free to ask us about it in the [IPinfo Community](https://community.ipinfo.io/).

## FAQs (Frequently Asked Questions)

- [IPinfo Community posts tagged as `ASN`](https://community.ipinfo.io/tag/asn)
- [Choosing between the ASN, IP to ASN and IP to Company database](https://community.ipinfo.io/t/choosing-between-the-asn-ip-to-asn-and-ip-to-company-database/731)
- [Differences in data for the ASN and the IP to Company database](https://community.ipinfo.io/t/differences-in-data-for-the-asn-and-the-ip-to-company-database/730)

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)