# Privacy Detection

## IP Addresses associated with identity hiding services such as VPN, Tor, Proxies, Relays and Hosting service.

# Database Schema & Description

*[data updated as of August, 2022]*

The following database schema represents the CSV database. We also provide JSON and MMDB format data.

| Field Name | Example     | Data Type | Notes                                                                |
|------------|-------------|-----------|----------------------------------------------------------------------|
| `start_ip` | 115.9.76.79 | TEXT      | Starting IP address of an IP address range                           |
| `end_ip`   | 115.9.76.79 | TEXT      | Ending IP address of an IP address range                             |
| `join_key` | 115.9.0.0   | TEXT      | Special variable to facilitate databas `join` operation              |
| `hosting`  |             | BOOLEAN   | Indicates a hosting/cloud service/data center IP address             |
| `proxy`    |             | BOOLEAN   | Indicates a open web proxy IP address                                |
| `tor`      |             | BOOLEAN   | Indicates a TOR (The Onion Router) exit node IP address              |
| `vpn`      | True        | BOOLEAN   | Indicates Virtual Private Network (VPN) service exit node IP address |
| `relay`    |             | BOOLEAN   | Indicates location preserving anonymous relay service                |
| `service`  |             | TEXT      | Name of the anonymous IP service provider                            |


> `join_key` represents the Class C network each IP address is part of, allowing you to filter the result set significantly before `join`ing. Learn more about `join_key` [here](https://community.ipinfo.io/t/ipinfos-join-key-column-explained/5526).
> 
> Please refer to "[How to choose the best file format for your IPinfo database?](https://ipinfo.io/blog/ipinfo-database-formats/)" article to select the best format possible for your use case.
>
> The usage of the IP data downloads relies on the software or application of the data. Check out our [documentation](https://ipinfo.io/developers/database-download), [community](https://community.ipinfo.io/c/docs/8), and our [integrations](https://ipinfo.io/integrations) pages to find the best path forward.

# API Response

As well as the database product, IPinfo also provides a robust API service. Please visit the [IPinfo Documentation](https://ipinfo.io/developers/data-types#privacy-data) portal to learn more. The Privacy Detection API service is available as part of our [Standard Tier](https://ipinfo.io/developers/responses#standard-plan) plan.

API Query:

```bash
$ curl ipinfo.io/$IP_ADDRESS/carrier?token=TOKEN
```

Reponse:

```json
{
    "vpn": true,
    "proxy": false,
    "tor": false,
    "relay": false,
    "hosting": false,
    "service": "NordVPN"
}
```


🔗 [Privacy Data Documentation](https://ipinfo.io/developers/data-types#privacy-data)

![privacy detection API response.png](../assets/privacy_detection_api_response.png)

# Samples

- [CSV Database] [Privacy Detection Database Sample](/Privacy%20Detection/privacy_detection_sample.csv)
- [JSON Database] [Privacy Detection Database Sample](/Privacy%20Detection/privacy_detection_sample.json)
- [MMDB Database] [Privacy Detection Database Sample](/Privacy%20Detection/privacy_detection_sample.mmdb)
- [API] [Privacy Detection API Response Sample](/Privacy%20Detection/privacy_detection_api_sample.json)

# Guides, Resources & Links

## Links

🔗 [Privacy Detection Database Type](https://ipinfo.io/products/anonymous-ip-database)

🔗 [Privacy Detection Data Downloads Documentation](https://ipinfo.io/developers/privacy-detection-database)

🔗 [Privacy Detection API Page](https://ipinfo.io/products/proxy-vpn-detection-api)

🔗 [Privacy Detection Data Type](https://ipinfo.io/developers/data-types#privacy-data)

## Articles & Guides

- [Deep dive into privacy detection data and masked IPs](https://ipinfo.io/blog/deep-dive-into-privacy-detection-data-and-masked-ips/)
- [How to privacy-proof your online targeting](https://ipinfo.io/blog/privacy-adtech-online-targeting/)
- [5 businesses who use privacy detection data well](https://ipinfo.io/blog/using-privacy-detection-data/)
- [What to expect from our Privacy Detection API](https://ipinfo.io/blog/what-to-expect-from-our-privacy-detection-api/)

## FAQ (Frequently Asked Questions)

- [IPinfo Community posts tagged as `ip-privacy-detection`](https://community.ipinfo.io/tag/ip-privacy-detection)
- [Why the provider’s name is sometimes is missing from our IP to privacy detection data?](https://community.ipinfo.io/t/why-the-provider-s-name-is-sometimes-is-missing-from-our-ip-to-privacy-detection-data/1719)
- [Do we provide a confidence score for our IP to Privacy data?](https://community.ipinfo.io/t/do-we-provide-a-confidence-score-for-our-ip-to-privacy-data/1723)
- [How we classify IP addresses in the IP to Privacy Detection Dataset](https://community.ipinfo.io/t/how-we-classify-ip-addresses-in-the-ip-to-privacy-detection-dataset/5573)
- [Preventing bot activity with IPinfo’s IP to Privacy Data](https://community.ipinfo.io/t/preventing-bot-activity-with-ipinfos-ip-to-privacy-data/1811)
- [Difference between proxy and VPN according to our privacy detection](https://community.ipinfo.io/t/difference-between-proxy-and-vpn-according-to-our-privacy-detection/5604)
- [Why are some IP addresses not always flagged in the privacy detection data?](https://community.ipinfo.io/t/why-are-some-ip-addresses-not-always-flagged-in-the-privacy-detection-data/5626)
- [Getting IP data from anonymous IP addresses](https://community.ipinfo.io/t/getting-ip-data-from-anonymous-ip-addresses/1743)
- [Preventing Ad Fraud using IPinfo’s data](https://community.ipinfo.io/t/preventing-ad-fraud-using-ipinfo-s-data/5591)
- [Anonymous or masked IP address](https://ipinfo.io/faq/article/83-anonymous-or-masked-ip-address)
- [What is Tor?](https://ipinfo.io/faq/article/81-what-is-tor)
- [What is a proxy?](https://ipinfo.io/faq/article/82-what-is-proxy)
- [What is a VPN?](https://ipinfo.io/faq/article/80-what-is-vpn)

If you have any questions about using our data, feel free to ask us about it in the [IPinfo Community](https://community.ipinfo.io/).

---

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)