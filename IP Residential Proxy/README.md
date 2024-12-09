# IP to Residential Proxy

## Identify residential proxy IPs, including mobile network proxies, from more than 100 services with acitivity level.

# Database Schema & Description

*[data updated as of December, 2024]*

The following database schema represents the CSV database. We also provide JSON and MMDB format data.

| Field Name        | Example          | Data Type | Description                                                                                                                                                         |
|-------------------|------------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ip                | 38.222.31.85     | TEXT      | IPv4 or IPv6 address associated with a residential proxy.                                                                                                           |
| service           | lightningproxies | TEXT      | Name of the residential proxy service. Carrier/mobile services are suffixed with _mobile (e.g., soax_mobile).                                                       |
| last_seen         | 2024-09-07       | TEXT      | Last recorded date when the residential proxy IP was active, formatted as YYYY-MM-DD (ISO-8601). Timezone is UTC.                                                   |
| percent_days_seen | 2                | TEXT      | Integer indicating the percentage of days the IP was active in the last 90-day period, reflecting its activity and frequency of IP within a residential proxy pool. |



> Please refer to "[How to choose the best file format for your IPinfo database?](https://ipinfo.io/blog/ipinfo-database-formats/)" article to select the best format possible for your use case.
>
> The usage of the IP data downloads relies on the software or application of the data. Check out our [documentation](https://ipinfo.io/developers/database-download), [community](https://community.ipinfo.io/c/docs/8), and our [integrations](https://ipinfo.io/integrations) pages to find the best path forward.

# Samples

- [CSV Database] [IP to Residental Proxy Database Sample](/IP%20Residential%20Proxy/ip_residential_proxy_sample.csv)
- [JSON Database] [IP to Residental Proxy Database Sample](/IP%20Residential%20Proxy/ip_residential_proxy_sample.json)
- [MMDB Database] [IP to Residental Proxy Database Sample](/IP%20Residential%20Proxy/ip_residential_proxy_sample.mmdb)

# Guides, Resources & Links

## Links

🔗 [Residential Proxy Detection Data Downloads Documentation](https://ipinfo.io/developers/ip-to-residential-proxy)


If you have any questions about using our data, feel free to ask us about it in the [IPinfo Community](https://community.ipinfo.io/).

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)