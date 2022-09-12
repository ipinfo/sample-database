# IP to Company Database

## Identify the company, their type, their domain and the IP addresses they own.

# Database Schema & Description

*[data updated as of August, 2022]*

| Field Name | Example | Data Type | Notes |
| --- | --- | --- | --- |
| `start_ip` | 107.136.106.168 | TEXT | Starting IP address of an IP address range |
| `end_ip` | 107.136.106.175 | TEXT | Ending IP address of an IP address range |
| `join_key` | 107.136.0.0 | TEXT | Specialized variable to facilitate join operation |
| `name` | ZSPEC FLOW-180709174314 | TEXT | Name of the company |
| `domain` | zspec.com | TEXT | Domain of the company |
| `type` | business | TEXT | Type of business. e.g. Business, ISP, Hosting, Education |
| `asn` | AS7018 | TEXT | ASN associated with the company |
| `as_name` | AT&T Services, Inc. | TEXT | Name of the ASN |
| `as_domain` | att.com | TEXT | Domain name of the ASN |
| `as_type` | isp | TEXT | ASN Type: ISP, Hosting, Business or Education |
| `country` | US | TEXT | ISO 3166 country code |

> `join_key` → This key represents the Class C network each IP address is part of, allowing you to filter the result set significantly before filtering to the exact IP address you want. [[*Source*](https://ipinfo.io/blog/ingesting-ipinfo-geolocation-data-with-postgresql-13/)]
> 

IP address data like `start_ip`, `end_ip` and `join_key` should be assigned `inet` data type if you are ingesting the data in PostgreSQL.

# API Response

![IP to Company API Response](../assets/IP_to_Company_API_example.png)

As well as the database product, IPinfo also provides a robust API service. Please visit the [IPinfo Documentation](https://ipinfo.io/developers) portal to learn more.

```bash
$ curl ipinfo.io/IP_ADDRESS?token=TOKEN
```

![IP to Company (1).png](../assets/IP_to_Company.png)

# Guides, Resources & Links

## Links

🔗 [IP to Company Database Page](https://ipinfo.io/products/ip-company-database)

🔗 [IP to Company API Page](https://ipinfo.io/products/ip-company-api)

🔗 [IP to Company Data Type Documentation](https://ipinfo.io/developers/data-types#company-data)

## Article & Guides (2)

- [How to use IP address data to add value to sales funnels](https://ipinfo.io/blog/how-to-use-ip-address-data-to-add-value-to-sales-funnels/)
- [What firmographics can be gathered from IP address data](https://ipinfo.io/blog/company-data-from-ip-address/)

---

# Interested in more?

Currently, we are limiting the sample datasets to only **200 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfoio) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)