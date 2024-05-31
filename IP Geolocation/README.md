# IP Geolocation Database

## Get location data such as zipcode, city, region, country, location, timezone etc. of IP addresses.

Our IP geolocation data is our primary data product and is considered one of the best in the industry. We operate a large scale network infrastructure consisting of hundreds of servers around the world through which we take active network measurements over the entire internet ecosystem. Through our active measurement, we produce reliable and accurate IP geolocation data. You can learn more about our network from this article:[Probe network - how we make sure our data is accurate](https://ipinfo.io/blog/probe-network-how-we-make-sure-our-data-is-accurate/).

# Database Schema & Description

*[data updated as of May, 2024]*

The following database schema represents the CSV database. We also provide JSON and MMDB format data.

| Field Name    | Example          | Data Type | Notes                                                    |
|---------------|------------------|-----------|----------------------------------------------------------|
| `start_ip`    | 1.253.242.0      | TEXT      | Starting IP address of an IP address range               |
| `end_ip`      | 1.253.242.255    | TEXT      | Ending IP address of an IP address range                 |
| `join_key`    | 1.253.0.0        | TEXT      | Special variable to facilitate database `join` operation |
| `city`        | Yangsan          | TEXT      | City of the IP address                                   |
| `region`      | Gyeongsangnam-do | TEXT      | Region of the IP address                                 |
| `country`     | KR               | TEXT      | ISO 3166 country code of the IP address                  |
| `latitude`    | 35.34199         | FLOAT     | Latitude value of the IP address                         |
| `longitude`   | 129.03358        | FLOAT     | Longitude value of the IP address                        |
| `postal_code` | 50593            | TEXT      | Postal code or zip code of the IP address                |
| `timezone`    | Asia/Seoul       | TEXT      | Local timezone of the IP address                         |


> `join_key` represents the Class C network each IP address is part of, allowing you to filter the result set significantly before `join`ing. Learn more about `join_key` [here](https://community.ipinfo.io/t/ipinfos-join-key-column-explained/5526).
> 
> Please refer to "[How to choose the best file format for your IPinfo database?](https://ipinfo.io/blog/ipinfo-database-formats/)" article to select the best format possible for your use case.
>
> The usage of the IP data downloads relies on the software or application of the data. Check out our [documentation](https://ipinfo.io/developers/database-download), [community](https://community.ipinfo.io/c/docs/8), and our [integrations](https://ipinfo.io/integrations) pages to find the best path forward.

# API Response

IPinfo also provides a robust IP to Geolocation API service. Please visit the [IPinfo Documentation](https://ipinfo.io/developers/data-types#geolocation-data) portal to learn more. IP to Geolocation is our IP data available from tier to enterprise tier API access.

API Query:

```bash
$ curl ipinfo.io/$IP_ADDRESS?token=$TOKEN
```

Response:

```json
{
    "ip": "77.224.89.172",
    "hostname": "static-172-89-224-77.ipcom.comunitel.net",
    "city": "Vigo",
    "region": "Galicia",
    "country": "ES",
    "loc": "42.2328,-8.7226",
    "postal": "36201",
    "timezone": "Europe/Madrid"
}
```

![IP Geolocation API.png](../assets/IP_Geolocation_API.png)

# Samples

- [CSV Database] [IP Geolocation Database Sample](/IP%20Geolocation/ip_geolocation_sample.csv)
- [JSON Database] [IP Geolocation Database Sample](/IP%20Geolocation/ip_geolocation_sample.json)
- [MMDB Database] [IP Geolocation Database Sample](/IP%20Geolocation/ip_geolocation_sample.mmdb)
- [API] [IP Geolocation API Response Sample](/IP%20Geolocation/ip_geolocation_api_sample.json)

# Guides, Resources & Links

## Links

🔗 [IP Geolocation Database Page](https://ipinfo.io/products/ip-geolocation-database)

🔗 [IP Geolocation Data Downloads Documentation](https://ipinfo.io/developers/ip-to-geolocation-database)

🔗 [IP Geolocation API Page](https://ipinfo.io/products/ip-geolocation-api)

🔗 [IP Geolocation Data Type Documentation](https://ipinfo.io/developers/data-types#geolocation-data)

## Articles & Guides

- [Probe network - how we make sure our data is accurate](https://ipinfo.io/blog/probe-network-how-we-make-sure-our-data-is-accurate/)
- [Community posts on location data](https://community.ipinfo.io/search?q=location)
- [IPinfo location data accuracy](https://ipinfo.io/accuracy)
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

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)