# IP to Mobile Carrier

## Detect the carrier's IP address and retrieve mobile carrier information (carrier, MCC, MNC).

# Database Schema & Description

*[data updated as of May, 2024]*

The following database schema represents the CSV database. We also provide JSON and MMDB format data.

| Field Name | Example                                  | Data Type | Notes                                                    |
|------------|------------------------------------------|-----------|----------------------------------------------------------|
| `start_ip` | 5.208.203.0                              | TEXT      | Starting IP address of an IP address range               |
| `end_ip`   | 5.208.203.255                            | TEXT      | Ending IP address of an IP address range                 |
| `join_key` | 5.208.0.0                                | TEXT      | Special variable to facilitate database `join` operation |
| `name`     | Mobile Communication Company of Iran PLC | TEXT      | Name of the mobile carrier                               |
| `country`  | IR                                       | TEXT      | ISO 3166 country code of the IP addresses                |
| `mcc`      | 432                                      | TEXT      | Mobile Country Code (MCC) of the carrier                 |
| `mnc`      | 11                                       | TEXT      | Mobile Network Code (MNC) of the carrier                 |

> `join_key` represents the Class C network each IP address is part of, allowing you to filter the result set significantly before `join`ing. Learn more about `join_key` [here](https://community.ipinfo.io/t/ipinfos-join-key-column-explained/5526).
> 
> Please refer to "[How to choose the best file format for your IPinfo database?](https://ipinfo.io/blog/ipinfo-database-formats/)" article to select the best format possible for your use case.
>
> The usage of the IP data downloads relies on the software or application of the data. Check out our [documentation](https://ipinfo.io/developers/database-download), [community](https://community.ipinfo.io/c/docs/8), and our [integrations](https://ipinfo.io/integrations) pages to find the best path forward.

# API Response

As well as the database product, IPinfo also provides a robust API service. Please visit the [IPinfo Documentation](https://ipinfo.io/developers/data-types#carrier-data) portal to learn more. The Carrier API service is available as part of our [Business Tier](https://ipinfo.io/developers/responses#business-plan) plan.

API Query:

```bash
$ curl ipinfo.io/$IP_ADDRESS/carrier?token=TOKEN
```

Reponse:

```json
{
    "name": "Algar Telecom",
    "mcc": "724",
    "mnc": "32"
}
```

![mobile carrier API response.png](../assets/mobile_carrier_api_response.png)

# Samples

- [CSV Database] [IP to Mobile Carrier Database Sample](/IP%20to%20Mobile%20Carrier/ip_carrier_sample.csv)
- [JSON Database] [IP to Mobile Carrier Database Sample](/IP%20to%20Mobile%20Carrier/ip_carrier_sample.json)
- [MMDB Database] [IP to Mobile Carrier Database Sample](/IP%20to%20Mobile%20Carrier/ip_carrier_sample.mmdb)
- [API] [IP to Mobile Carrier API Response Sample](/IP%20to%20Mobile%20Carrier/ip_carrier_api_sample.json)

# Guides, Resources & Links

## Links

🔗 [IP to Mobile Carrier Database Page](https://ipinfo.io/products/mobile-ip-database)

🔗 [IP to Mobile Carrier Data Downloads Documentation](https://ipinfo.io/developers/ip-to-mobile-carrier-database)

🔗 [IP to Mobile Carrier API Page](https://ipinfo.io/products/ip-carrier-api)

🔗 [Carrier Information Data Type Documentation](https://ipinfo.io/developers/data-types#carrier-data)

If you have any questions about using our data, feel free to ask us about it in the [IPinfo Community](https://community.ipinfo.io/).

## Articles & Guides

- [How to develop a mobile app with a geolocation feature](https://ipinfo.io/blog/how-to-develop-a-mobile-application-software-with-a-geolocation-feature/)

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)