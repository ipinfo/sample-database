# [<img src="https://ipinfo.io/static/ipinfo-small.svg" alt="IPinfo" width="24"/>](https://ipinfo.io/) IPinfo Sample Database Repository


## This repository contains CSV sample datasets of all the [IP address database products](https://ipinfo.io/account/data-downloads) we have to offer.


<p align="center">
  <img src="./assets/header_grahics_main_readme.png">
</p>


# Database Overview

<p align="center">
  <img src="./assets/product_demo_main_readme.gif">
</p>

The database products [IPInfo.io](http://IPInfo.io) has to offer are -

| Database Product | Sample Database Repo | Description |
| --- | --- | --- |
| [IP Geolocation Database](https://ipinfo.io/products/ip-geolocation-database) | [IP Geolocation Sample](/IP%20Geolocation) | IP geolocation information |
| [IP to Company Database](https://ipinfo.io/products/ip-company-database) | [IP to Company Sample](/IP%20to%20Company) | Company associated with IP address |
| [ASN Database](https://ipinfo.io/products/asn-database) | [ASN Sample](/ASN) | IP range and ASN |
| [IP to Mobile Carrier Database](https://ipinfo.io/products/mobile-ip-database) | [IP to Mobile Sample](/IP%20to%20Mobile%20Carrier) | Carrier and country information |
| [Privacy Detection Database](https://ipinfo.io/products/anonymous-ip-database) | [Privacy Detection Sample](/Privacy%20Detection) | VPN, Proxies, Tor, Relays |
| [Hosted Domain Database](https://ipinfo.io/products/hosted-domains-database) | [Hosted Domains Sample](/Hosted%20Domains) | Reverse IP lookup |
| [Abuse Contact Database](https://ipinfo.io/products/ip-abuse-contact-database) | [Abuse Contact Sample](/Abuse%20Contact) | Abuse contact information |
| [WHOIS Database](https://ipinfo.io/products/ip-whois-data-download) | [WHOIS Sample](/WHOIS) | Contexualized WHOIS Database |

**All of these products are available as CSV, JSON and MMDB type.**

# Features of the Repository

Please visit each folder to learn more about the databases. Each directory README contains -

- Sample Dataset (200 rows)
- API response (in `.json`)
- Breakdown of the dataset with description of the fields
- Breakdown of the API response
- Helpful guides, resources and articles


<details id=0>
<summary><h1>Summary of the Databases</h1></summary>

Please visit the database directories to learn more.

<details id=1>
<summary><h2>IP Geolocation</h2></summary>

**Get geolocation information from IP Addresses.**

You can find the schema, database sample, API response sample, and other information from the **[IP Geolocation folder](/IP%20Geolocation)**. The CSV database includes the following fields:

| Field Name | Example | Notes |
| --- | --- | --- |
| `start_ip` | 1.253.242.0 | Starting IP address of an IP address range |
| `end_ip` | 1.253.242.255 | Ending IP address of an IP address range |
| `join_key` | 1.253.0.0 | Special variable to facilitate join operation |
| `city` | Yangsan | City of the location |
| `region` | Gyeongsangnam-do | Region of the location |
| `country` | KR | ISO 3166 country code |
| `latitude` | 35.34199 | Latitude value of the location |
| `longitude` | 129.03358 | Longitude value of the location |
| `postal_code` | 50593 | Postal code of the region. This is not the same as zip code. |
| `timezone` | Asia/Seoul | Local time zone |


### 🔗 [IP Geolocation Database Page](https://ipinfo.io/products/ip-geolocation-database)

</details>

<details id=2>
<summary><h2>IP to Company</h2></summary>

**Get firmographics data and identify the company behind the IP Address and network traffic.**

You can find the schema, database sample, API response sample, and other information from the **[IP to Company folder](/IP%20to%20Company)**. Database includes the following fields:

| Field Name | Example | Notes |
| --- | --- | --- |
| `start_ip` | 107.136.106.168 | Starting IP address of an IP address range |
| `end_ip` | 107.136.106.175 | Ending IP address of an IP address range |
| `join_key` | 107.136.0.0 | Specialized variable to facilitate join operation |
| `name` | ZSPEC FLOW-180709174314 | Name of the company |
| `domain` | zspec.com | Domain of the company |
| `type` | business | Type of business. e.g. Business, ISP, Hosting or Education |
| `asn` | AS7018 | ASN associated with the company |
| `as_name` | AT&T Services, Inc. | Name of the ASN |
| `as_domain` | att.com | Domain name of the ASN |
| `as_type` | isp | ASN Type: ISP, Hosting, Business or Education |
| `country` | US | ISO 3166 country code |


### 🔗 [IP to Company Database Page](Sample%20Database%20fb322a60f0544458ad861eb738e869cd/IP%20to%20Company%20Database%2081d7f85aaeb244b19608f3a1de1fecad.md)



</details>

<details id=3>
<summary><h2>ASN</h2></summary>


**Get ASN data from ASN or IP Address information.**

You can find the schema, database sample, API response sample, and other information from the **[ASN folder](/ASN)**. Database (CSV) contains the following fields:

| Field Name | Example | Notes |
| --- | --- | --- |
| `start_ip` | 125.113.0.0 | Starting IP address of the ASN IP address block |
| `end_ip` | 125.113.255.255 | Ending IP address of the ASN IP address block |
| `join_key` | 125.113.0.0 | Special variable to facilitate join operation |
| `asn` | AS4134 | Autonomous System Number (ASN) |
| `domain` | chinatelecom.com.cn | Domain name of the AS |
| `name` | CHINANET-BACKBONE | Name of the ASN |
| `type` | isp | ASN Type: ISP, Hosting, Education or Business |
| `country` | CN | ISO 3166 country code |

### 🔗 [ASN Database Page](https://ipinfo.io/products/asn-database)


</details>

<details id=4>
<summary><h2> IP to Mobile Carrier </h2></summary>

**Lookup Mobile Carrier data such as - MCC and MNC from IP addresses.** 

You can find the schema, database sample, API response sample, and other information from the **[IP to Mobile Carrier folder](/IP%20to%20Mobile%20Carrier)**. The database (CSV) contains the following fields:

| Field Name | Example | Notes |
| --- | --- | --- |
| `start_ip` | 5.208.203.0 | Starting IP address of an IP address range |
| `end_ip` | 5.208.203.255 | Ending IP address of an IP address range |
| `join_key` | 5.208.0.0 | Special variable to facilitate join operation. |
| `name` | Mobile Communication Company of Iran PLC | Name of the mobile carrier |
| `country` | IR | ISO 3166 country code |
| `mcc` | 432 | Mobile Country Code (MCC) of the carrier |
| `mnc` | 11 | Mobile Network Code (MNC) of the carrier |

### 🔗 [IP to Mobile Carrier Database Page](https://ipinfo.io/products/mobile-ip-database)

</details>

<details id=5>
<summary><h2>Privacy Detection</h2></summary>

**Demystify anonymous IP addresses. Privacy detection such as VPN, Tor, Proxies, Relays and Hosting from IP addresses.**

You can find the schema, database sample, API response sample, and other information from the **[Privacy Detection folder](/Privacy%20Detection)**. The CSV database includes the following fields:

| Field Name | Example | Notes |
| --- | --- | --- |
| `start_ip` | 115.9.76.79 | Starting IP address of an IP address range |
| `end_ip` | 115.9.76.79 | Ending IP address of an IP address range |
| `join_key` | 115.9.0.0 | Special variable to facilitate join operation |
| `hosting` |  | Indicates a hosting IP address most of the time based on a datacenter. Indicative of bots, scrapers or malicious activities |
| `proxy` |  | Similar to VPN mainly used by businesses |
| `tor` |  | IP address originated from the Onion router |
| `vpn`| True | Virtual Private Network (VPN) service IP address |
| `relay` |  | Traffic relays often provided by CDN companies |
| `service` |  | Name of the privacy service provider |

### 🔗 [Privacy Detection Database Page](https://ipinfo.io/products/anonymous-ip-database)

</details>

<details id=6>
<summary><h2>Hosted Domains</h2></summary>

**Hosted Domains database enables you to do reverse IP lookups.** Through our Hosted Domains service, you can see the the full list of domain hosted on a single IP address. 

You can find the schema, database sample, API response sample, and other information from the **[Hosted Domains folder](/Hosted%20Domains)**. The fields in the database includes:

| Field Name | Example | Notes |
| --- | --- | --- |
| `ip` | 135.125.236.225 | IP address for reverse IP lookup |
| `total` | 3 | Number of domains registered to the IP Address |
| `domains` | farmanaut.com,pharmanaut.be,farmanaut.be | Name of the domain(s) under the IP address |

### 🔗 [Hosted Domains Database Page](https://ipinfo.io/products/hosted-domains-database)

</details>

<details id=7>
<summary><h2>Abuse Contact</h2></summary>

**Get the abuse contact information of every ISP in the internet.**

You can find the schema, database sample, API response sample, and other information from the **[Abuse Contact folder](/Abuse%20Contact)**. The fields of the database are:

| Field Name | Example | Notes |
| --- | --- | --- |
| `start_ip` | 119.93.20.248 | Starting IP address of an IP address block |
| `end_ip` | 119.93.20.255 | Ending IP address of an IP address block |
| `join_key` | 119.93.0.0 | Special variable to facilitate join operation |
| `name` | Nilo Agir | Name of the abuse contact |
| `email` | abuse@pldt.net | Organizational email of the abuse contact |
| `address` | Philippine Long Distance Telephone Company, 6/... | Organizational address of the abuse contact |
| `country` | PH | ISO 3166 country code |
| `phone` | +632-584-1045 | Organizational phone number of the abuse contact |

### 🔗 [Abuse Contact Database Page](https://ipinfo.io/products/ip-abuse-contact-database)

</details>

<details id=8>
<summary><h2>WHOIS</h2></summary>


**IPinfo WHOIS database is contextual, robust and consistent database of various types of WHOIS data.**

You can find the schema, database sample, API response sample, and other information from the **[WHOIS folder](/WHOIS)**. The WHOIS database and their respective fields are listed below:

The WHOIS database and their respective fields are listed below:

| R WHOIS | WHOIS ASN | WHOIS MNT | WHOIS NET | WHOIS ORG | WHOIS POC |
| --- | --- | --- | --- | --- | --- |
| range | id | id | range | id | id |
| id | name | name | id | name | name |
| name | country | admin_id | name | address | mobilephone |
| descr | org_id | tech_id | country | street | officephone |
| host | created | org_id | domain | city | fax |
| country | updated | created | org_id | state | addres |
| email | source | updated | status | postalcode | country |
| abuse | raw | source | tech_id | country | email |
| domain |  | raw | mnt_id | admin_id | abuse_email |
| countr.1 |  |  | admin_id | tech_id | created |
| city |  |  | created | abuse_id | updated |
| street |  |  | updated | mnt_id | source |
| postal |  |  | source | email | raw |
| updated |  |  | raw | domain |  |
| imported |  |  |  | created |  |
|  |  |  |  | updated |  |
|  |  |  |  | source |  |
|  |  |  |  | raw |  |


### 🔗 [WHOIS Database Page](https://ipinfo.io/products/ip-abuse-contact-database)

</details>

</details>

<details id=usage>
<summary><h1>Other Information (Usage, Exploration etc.)</h1></summary>

## How to explore the sample databases

- Please visit the folders for each database. You can also find the API response samples there for each products.
- If you would like to explore CSV files, feel free to use any of these online services and import the raw CSV there -
    - [https://csvfiddle.io/](https://csvfiddle.io/)
    - [https://lite.datasette.io/](https://lite.datasette.io/)
- Or you can you just download the CSV files to take a closer look.

## Usage Information

- After signing up for database downloads service, you can either download the database from our website or you can `curl` the database from the database download endpoint. But make sure you have redirect [enabled](https://ipinfo.io/faq/article/142-when-i-access-the-database-endpoint-using-something-like-curl-it-doesn-t-seem-to-work-and-i-get-a-corrupted-empty-file-what-am-i-doing-wrong).
- You can select how frequently the database gets updated. It can be daily, weekly, bi-weekly or monthly.
- To lookup an specific database you can use any kind of data exploration package or database system you want to use. [Here is an example](https://ipinfo.io/faq/article/144-how-do-you-do-a-lookup-of-an-ip-address-using-your-database) of using mySQL and PosgreSQL to lookup a specific IP address.

</details>

# Relevant Articles

## Guides

- [Our downloadable IP WHOIS data sets are live!](https://ipinfo.io/blog/our-downloadable-ip-whois-data-sets-are-live)
- [Data downloads vs API, or both?](https://ipinfo.io/blog/data-downloads-vs-api-or-both/)
- [Ingesting IPinfo geolocation data with PostgreSQL 13](https://ipinfo.io/blog/ingesting-ipinfo-geolocation-data-with-postgresql-13/)
- [Introducing a Simpler Way to get IP Address Data in Snowflake](https://ipinfo.io/blog/ip-address-data-in-snowflake/)

## FAQs

The list of FAQs (Frequently Asked Questions) can be found here [here](https://ipinfo.io/faq/category/137-data-downloads).

<details>

<summary><h2>External Resources</h2></summary>


- IP Address Data Type declaration:
    - [PostgreSQL: Network Address Types: INET vs CIDR](https://www.postgresql.org/docs/current/datatype-net-types.html#DATATYPE-INET-VS-CIDR)

</details>



# Found a bug?

If you found an issue or would like to submit an improvement to this project, please submit an issue using the issues tab above. If you would like to submit a PR with a fix, reference the issue you created!

# Interested in more?

Currently we are limiting the sample datasets to only **200 rows**. If you would like to request a larger sample or would like to get a quote on the database products [feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form). Follow us on [Twitter](https://twitter.com/ipinfoio) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

---

# IPinfo Tools

There are official IPinfo client libraries available for many languages including PHP, Python, Go, Java, Ruby, and many popular frameworks such as Django, Rails and Laravel. There are also many third party libraries and integrations available for our API.

We also have an excellent CLI tool (**928 Stars on Github**) and mapping tool.

See [https://ipinfo.io/developers/libraries](https://ipinfo.io/developers/libraries) for more details.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)