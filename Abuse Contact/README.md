# Abuse Contact Database

## The Abuse Contact database provides the contact information of all internet organizations for reporting abusive activity, spam, or other malicious activities. The dataset is sourced from WHOIS records. It is parsed to provide a structured format.

# Database Schema & Description

*[data updated as of May, 2024]*

The following database schema represents the CSV database. We also provide JSON and MMDB format data.

| Field Name | Example                                           | Data Type | Notes                                                    |
|------------|---------------------------------------------------|-----------|----------------------------------------------------------|
| `start_ip` | 119.93.20.248                                     | TEXT      | Starting IP address of an IP address block               |
| `end_ip`   | 119.93.20.255                                     | TEXT      | Ending IP address of an IP address block                 |
| `join_key` | 119.93.0.0                                        | TEXT      | Special variable to facilitate database `join` operation |
| `name`     | Nilo Agir                                         | TEXT      | Name of the abuse contact                                |
| `email`    | abuse@pldt.net                                    | TEXT      | Organizational email of the abuse contact                |
| `address`  | Philippine Long Distance Telephone Company, 6/... | TEXT      | Organizational address of the abuse contact              |
| `country`  | PH                                                | TEXT      | ISO 3166 country code                                    |
| `phone`    | +632-584-1045                                     | TEXT      | Organizational phone number of the abuse contact         |

> `join_key` represents the Class C network each IP address is part of, allowing you to filter the result set significantly before `join`ing. Learn more about `join_key` [here](https://community.ipinfo.io/t/ipinfos-join-key-column-explained/5526).
> 
> Please refer to "[How to choose the best file format for your IPinfo database?](https://ipinfo.io/blog/ipinfo-database-formats/)" article to select the best format possible for your use case.
>
> The usage of the IP data downloads relies on the software or application of the data. Check out our [documentation](https://ipinfo.io/developers/database-download), [community](https://community.ipinfo.io/c/docs/8), and our [integrations](https://ipinfo.io/integrations) pages to find the best path forward.


# API Response

As well as the database product, [IPinfo](https://ipinfo.io/) also provides a robust API service. Please visit the [IPinfo Documentation](https://ipinfo.io/developers/data-types#abuse-contact-data) portal to learn more. The Abuse Contact API service is available as part of our [Business Tier](https://ipinfo.io/developers/responses#business-plan) plan.

API Query:

```bash
$ curl ipinfo.io/$IP_ADDRESS/abuse?token=$TOKEN
```

Response:

```json
{
    "address": "US, WA, Bellevue, 12920 SE 38th Street, 98006",
    "country": "US",
    "email": "abuse@t-mobile.com",
    "name": "abuse",
    "network": "100.128.0.0/9",
    "phone": "+1-888-662-4662"
}
```

![Abuse Contact API Response.png](../assets/Abuse_Contact_API_Response.png)

# Samples

- [CSV Database] [Abuse Contact Database Sample](/Abuse%20Contact/abuse_contact_sample.csv)
- [JSON Database] [Abuse Contact Database Sample](/Abuse%20Contact/abuse_contact_sample.json)
- [MMDB Database] [Abuse Contact Database Sample](/Abuse%20Contact/abuse_contact_sample.mmdb)
- [API] [Abuse Contact API Response Sample](/Abuse%20Contact/abuse_contact_api_sample.json)

# Guides, Resources & Links

## Links

🔗 [Abuse Contact Database Page](https://ipinfo.io/products/ip-abuse-contact-database)

🔗 [Abuse Contact Data Downloads Documentation](https://ipinfo.io/developers/abuse-contact-database)

🔗 [Abuse Contact API Page](https://ipinfo.io/products/ip-abuse-contact-api)

🔗 [Abuse Contact Data Type Documentation](https://ipinfo.io/developers/data-types#abuse-contact-data)

If you have any questions about using our data, feel free to ask us about it in the [IPinfo Community](https://community.ipinfo.io/).

## FAQs (Frequently Asked Questions)

- [How to report IP abuse?](https://ipinfo.io/faq/article/86-how-to-report-ip-abuse)

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)