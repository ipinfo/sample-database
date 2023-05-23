# IP Geolocation Database

## Geolocation data such as city, region, country, location, timezone etc. identified from IP address.

# Database Schema & Description

*[data updated as of August, 2022]*

The following database schema represents the CSV database. We also provide JSON and MMDB format data.

| Field Name    | Example          | Data Type | Notes                                         |
|---------------|------------------|-----------|-----------------------------------------------|
| `start_ip`    | 1.253.242.0      | TEXT      | Starting IP address of an IP address range    |
| `end_ip`      | 1.253.242.255    | TEXT      | Ending IP address of an IP address range      |
| `join_key`    | 1.253.0.0        | TEXT      | Special variable to facilitate join operation |
| `city`        | Yangsan          | TEXT      | City of the location                          |
| `region`      | Gyeongsangnam-do | TEXT      | Region of the location                        |
| `country`     | KR               | TEXT      | ISO 3166 country code                         |
| `latitude`    | 35.34199         | FLOAT     | Latitude value of the location                |
| `longitude`   | 129.03358        | FLOAT     | Longitude value of the location               |
| `postal_code` | 50593            | TEXT      | Postal code of the location                   |
| `timezone`    | Asia/Seoul       | TEXT      | Local time zone                               |


> `join_key` → This key represents the Class C network each IP address is part of, allowing you to filter the result set significantly before filtering to the exact IP address you want. [[*Source*](https://ipinfo.io/blog/ingesting-ipinfo-geolocation-data-with-postgresql-13/)]
> 

IP address data like `start_ip`, `end_ip` and `join_key` should be assigned `inet` data type if you are ingesting the data in PostgreSQL.

# API Response

As well as the database product, IPinfo also provides a robust API service. Please visit the [IPinfo Documentation](https://ipinfo.io/developers) portal to learn more.

```bash
$ curl ipinfo.io/IP_ADDRESS?token=TOKEN
```

![IP Geolocation API (1).png](../assets/IP_Geolocation_API.png)

# Samples

- [CSV Database] [IP Geolocation Database Sample](/IP%20Geolocation/ip_geolocation_sample.csv)
- [JSON Database] [IP Geolocation Database Sample](/IP%20Geolocation/ip_geolocation_sample.json)
- [MMDB Database] [IP Geolocation Database Sample](/IP%20Geolocation/ip_geolocation_sample.mmdb)
- [API] [IP Geolocation API Response Sample](/IP%20Geolocation/ip_geolocation_api_sample.json)

# Guides, Resources & Links

## Links

🔗 [IP Geolocation Database Page](https://ipinfo.io/products/ip-geolocation-database)

🔗 [IP Geolocation API Page](https://ipinfo.io/products/ip-geolocation-api)

🔗 [IP Geolocation Data Type Documentation](https://ipinfo.io/developers/data-types#geolocation-data)

## Articles & Guides (9)

- [Top ways to use IP geolocation data](https://ipinfo.io/blog/top-ways-to-use-ip-geolocation-data/)
- [How to develop a mobile app with a geolocation feature](https://ipinfo.io/blog/how-to-develop-a-mobile-application-software-with-a-geolocation-feature/)
- [How to use IP address data for digital media and entertainment](https://ipinfo.io/blog/ip-address-data-for-digital-media-and-entertainment/)
- [Breaking Down Geographic Market Segmentation and How to Utilize it](https://ipinfo.io/blog/breaking-down-geographic-market-segmentation-and-how-to-utilize-it/)
- [How many IPs changed geolocation over a year](https://ipinfo.io/blog/how-many-ips-change-geolocation-over-a-year/)
- [How to use IP address data for better PPC geotargeting](https://ipinfo.io/blog/how-to-use-ip-address-data-for-better-ppc-geotargeting/)
- [How the travel industry can use IP address data to save money](https://ipinfo.io/blog/how-the-travel-industry-can-use-ip-address-data-to-save-money/)
- [How to prevent localized pricing policy abuse](https://ipinfo.io/blog/how-to-prevent-localized-pricing-policy-abuse/)
- [6 common geolocation marketing mistakes & how to solve them](https://ipinfo.io/blog/6-common-geolocation-marketing-mistakes-how-to-solve-them/)

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfoio) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)