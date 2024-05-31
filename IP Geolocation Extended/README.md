# IP Geolocation Extended Database

## IP to Geolocation database with accuracy radius data as a confidence metric.

This database provides IP geolocation data with an accuracy radius, which is the estimated distance between the actual location of the user (based on our ground truth daata) and the geolocation coordinates returned by the database. The accuracy radius varies depending on the city, country, connection type, and IP address type. The database also comes with the `geoname_id` field that provide additional geographic information from [geonames.org](https://www.geonames.org/).

# Database Schema & Description

*[data updated as of May, 2023]*

The following database schema represents the CSV database. We also provide JSON and MMDB format data.

| Field Name    | Example             | Description                                                 |
|---------------|---------------------|-------------------------------------------------------------|
| `start_ip`    | 171.71.0.0          | Starting IP address of an IP address range                  |
| `end_ip`      | 171.71.127.255      | Ending IP address of an IP address range                    |
| `join_key`    | 171.71.0.0          | Special variable to facilitate `join` operation             |
| `city`        | San Jose            | City of the IP address                                      |
| `region`      | California          | Region of the IP address                                    |
| `country`     | US                  | ISO 3166 country code of the IP address                     |
| `latitude`    | 37.4087             | Latitude value of the IP address                            |
| `longitude`   | -121.9406           | Longitude value of the IP address                           |
| `postal_code` | 95134               | Postal code or zip code of the IP address                   |
| `timezone`    | America/Los_Angeles | Local timezone of the IP address                            |
| `geoname_id`  | 5392171             | `geoname_id` from [geonames.org](https://www.geonames.org/) |
| `radius`      | 5                   | Accuracy radius in terms of kilometers                      |

> `join_key` represents the Class C network each IP address is part of, allowing you to filter the result set significantly before `join`ing. Learn more about `join_key` [here](https://community.ipinfo.io/t/ipinfos-join-key-column-explained/5526).
> 
> Please refer to "[How to choose the best file format for your IPinfo database?](https://ipinfo.io/blog/ipinfo-database-formats/)" article to select the best format possible for your use case.
>
> The usage of the IP data downloads relies on the software or application of the data. Check out our [documentation](https://ipinfo.io/developers/database-download), [community](https://community.ipinfo.io/c/docs/8), and our [integrations](https://ipinfo.io/integrations) pages to find the best path forward.

# Samples

- [CSV Database] [IP Geolocation (Extended) Database Sample](/IP%20Geolocation%20Extended/ip_geolocation_extended_sample.csv)
- [JSON Database] [IP Geolocation (Extended) Database Sample](/IP%20Geolocation%20Extended/ip_geolocation_extended_sample.json)
- [MMDB Database] [IP Geolocation (Extended) Database Sample](/IP%20Geolocation%20Extended/ip_geolocation_extended_sample.mmdb)
- [CSV Database] [IP Geolocation (Extended) Database - IPv4 Sample](/IP%20Geolocation%20Extended/ip_geolocation_extended_ipv4_sample.csv)
- [JSON Database] [IP Geolocation (Extended) Database - IPv4 Sample](/IP%20Geolocation%20Extended/ip_geolocation_extended_ipv4_sample.json)
- [MMDB Database] [IP Geolocation (Extended) Database - IPv4 Sample](/IP%20Geolocation%20Extended/ip_geolocation_extended_ipv4_sample.mmdb)
- [CSV Database] [IP Geolocation (Extended) Database - IPv6 Sample](/IP%20Geolocation%20Extended/ip_geolocation_extended_ipv6_sample.csv)
- [JSON Database] [IP Geolocation (Extended) Database - IPv6 Sample](/IP%20Geolocation%20Extended/ip_geolocation_extended_ipv6_sample.json)
- [MMDB Database] [IP Geolocation (Extended) Database - IPv6 Sample](/IP%20Geolocation%20Extended/ip_geolocation_extended_ipv6_sample.mmdb)

## Links

🔗 [IP Geolocation Extended Data Downloads Documentation](https://ipinfo.io/developers/ip-to-geolocation-extended)

The IP Geolocation Extended Database is a customized product available only through request. [Reach out to our sales team to get started](https://ipinfo.io/contact).

## FAQs (Frequently Asked Questions)

- [The radius field in the IP to Geolocation extended database explained](https://community.ipinfo.io/t/the-radius-field-in-the-ip-to-geolocation-extended-database-explained/694)
- [Measuring geolocation accuracy with ground truth dataset](https://community.ipinfo.io/t/measuring-geolocation-accuracy-with-ground-truth-dataset/1717)

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)