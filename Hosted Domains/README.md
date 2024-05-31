# Hosted Domain Database

## Hosted Domain Database facilitates reverse IP lookup and shows how many and which domains are hosted on which IP Addresses.

*If you are interested in Domain Name API / Database check out: [host.io](https://host.io/)*

# Database Schema & Description

*[data updated as of May, 2024]*

The following database schema represents the CSV database. We also provide JSON and MMDB format data.

| Field Name | Example                                  | Data Type | Notes                                          |
|------------|------------------------------------------|-----------|------------------------------------------------|
| `ip`       | 135.125.236.225                          | TEXT      | IP address for reverse IP lookup               |
| `total`    | 3                                        | INTEGER   | Number of domains registered to the IP Address |
| `domains`  | farmanaut.com,pharmanaut.be,farmanaut.be | TEXT      | Name of the domain(s) under the IP address     |

Each domain in the `domains` column is separated by a `,` (comma).

The Hosted Domains database contains domains that are hosted on a web server IP address, cached in a CDN server IP address, and the IP address that domain finally redirects to.

# API Response

As well as the database product, IPinfo also provides a robust Hosted Domains API service. Please visit the [IPinfo Hosted Domains API Documentation](https://ipinfo.io/developers/hosted-domains) portal to learn about the API, it's API parameters and features.

API Query:

```bash
$ curl "ipinfo.io/domains/$IP_ADDRESS?token=$TOKEN"
```

Response:

```json
{
    "ip": "34.168.30.71",
    "total": 1994,
    "domains": [
        "3stadt.com",
        "flytfrem.no",
        "aptalis-pharma.ca",
        "nftevening.xyz",
        "sub.quest"
        // ...
    ]
}
```

![Hosted Domains Reverse IP Lookup.png](../assets/Hosted_Domains__Reverse_IP_Lookup.png)

# Samples

- [CSV Database] [Hosted Domains Database Sample](/Hosted%20Domains/hosted_domains_sample.csv)
- [JSON Database] [Hosted Domains Database Sample](/Hosted%20Domains/hosted_domains_sample.json)
- [MMDB Database] [Hosted Domains Database Sample](/Hosted%20Domains/hosted_domains_sample.mmdb)
- [API] [Hosted Domains API Response Sample](/Hosted%20Domains/hosted_domains_api_sample.json)

# Guides, Resources & Links

## Links

🔗 [Hosted Domains Database Page](https://ipinfo.io/products/hosted-domains-database)

🔗 [Hosted Domains Data Downloads Documentation](https://ipinfo.io/developers/hosted-domains-database)

🔗 [Hosted Domains API Page](https://ipinfo.io/products/reverse-ip-api)

🔗 [Hosted Domains Documentation](https://ipinfo.io/developers/hosted-domains)

🔗 [Hosted Domains Data Type Documentation](https://ipinfo.io/developers/data-types#hosted-domains-data)

## Articles & Guides

- [Difference between rDNS and Hosted Domains](https://community.ipinfo.io/t/difference-between-rdns-and-hosted-domains/5601)
- [Reverse IP lookups: powerful yet overlooked tool](https://ipinfo.io/blog/reverse-ip-lookup-what-is-it-how-it-works)

## FAQs (Frequently Asked Questions)

- [Difference between rDNS and Hosted Domains](https://community.ipinfo.io/t/difference-between-rdns-and-hosted-domains/5601)
- [Do you provide domain data?](https://ipinfo.io/faq/article/51-domain-data)

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)