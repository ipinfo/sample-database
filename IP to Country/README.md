# IP to Country

## Get the country and continent where the IP addresses are located

The IP to Country database is part of our [free IP data downloads offering](https://ipinfo.io/products/free-ip-database). Features of the [IP to Country Database](https://ipinfo.io/developers/ip-to-country-database) includes:

- Full accuracy with zero compromise. The dataset is updated daily to ensure the highest accuracy possible.
- The dataset is a subset of our premium [IP to Geolocation Database](https://ipinfo.io/products/ip-geolocation-database).
- The IP to Country dataset provides ranges, country, and continent information.
- It includes both IPv4 and IPv6 data in a single dataset.
- The data is tabular and unnested, making it extremely easy to use.
- The IP to Country dataset aggregates ranges by country, making it ideal for country to range lookups and firewall lists.
- Our free databases are licensed under CC-BY-SA 4.0.
- Comes in MMDB, CSV, and JSON formats.

# Database Schema & Description

*[data updated as of May, 2024]*

The following database schema represents the CSV database. We also provide JSON and MMDB format data.

| Field Name       | Example         | Data Type | Description                                |
|------------------|-----------------|-----------|--------------------------------------------|
| `start_ip`       | 217.220.0.0     | TEXT      | Starting IP address of an IP address range |
| `end_ip`         | 217.223.255.255 | TEXT      | Ending IP address of an IP address range   |
| `country`        | IT              | TEXT      | ISO 3166 country code of the IP address    |
| `country_name`   | Italy           | TEXT      | Name of the country                        |
| `continent`      | EU              | TEXT      | Continent code of the country              |
| `continent_name` | Europe          | TEXT      | Name of the continent                      |


# Samples

- [CSV Database] [IP to Country Database Sample](/IP%20to%20Country/ip_country_sample.csv)
- [JSON Database] [IP to Country Database Sample](/IP%20to%20Country/ip_country_sample.json)
- [MMDB Database] [IP to Database Sample](/IP%20to%20Country/ip_country_sample.mmdb)

# Guides, Resources & Links

## Links

🔗 [IP to Country Database Documentation](https://ipinfo.io/developers/ip-to-country-database)

If you have any questions about using our data, feel free to ask us about it in the [IPinfo Community](https://community.ipinfo.io/).

## FAQs (Frequently Asked Questions)

- [IPinfo Community posts on the IP to Country data](https://community.ipinfo.io/search?q=country)

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)