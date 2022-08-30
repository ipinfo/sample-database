# [<img src="https://ipinfo.io/static/ipinfo-small.svg" alt="IPinfo" width="24"/>](https://ipinfo.io/) IPinfo Sample Database Repository


## This repository contains CSV sample datasets of all the [IP address database products](https://ipinfo.io/account/data-downloads) we have to offer.

![IPinfoio product overview](./assets/header_grahics_main_readme.png)


# Database Overview

![Product Demo](./assets/product_demo_main_readme.gif)

The database products [IPInfo.io](http://IPInfo.io) has to offer are -

| Database Product | Sample Database Repo | Description |
| --- | --- | --- |
| [IP Geolocation Database](https://ipinfo.io/products/ip-geolocation-database) | [IP Geolocation Sample](/IP%20Geolocation) |  |
| [IP to Company Database](https://ipinfo.io/products/ip-company-database) | - |  |
| [ASN Database](https://ipinfo.io/products/asn-database) | - |  |
| [IP to Mobile Carrier Database](https://ipinfo.io/products/mobile-ip-database) | - |  |
| [Privacy Detection Database](https://ipinfo.io/products/anonymous-ip-database) | - |  |
| [Hosted Domain Database](https://ipinfo.io/products/hosted-domains-database) | - |  |
| [Abuse Contact Database](https://ipinfo.io/products/ip-abuse-contact-database) | - |  |
| [WHOIS Database](https://ipinfo.io/products/ip-whois-data-download) | - |  |

**All of these products are available as CSV, JSON and MMDB type.**

# Features of the Repository

Please visit each folder to learn more about the databases. Each directory README contains -

- Sample Dataset (200 rows)
- API response (in `.json`)
- Breakdown of the dataset with description of the fields
- Breakdown of the API response
- Helpful guides, resources and articles

# Relevant Articles

## Guides

- [Our downloadable IP WHOIS data sets are live!](https://ipinfo.io/blog/our-downloadable-ip-whois-data-sets-are-live)
- [Data downloads vs API, or both?](https://ipinfo.io/blog/data-downloads-vs-api-or-both/)
- [Ingesting IPinfo geolocation data with PostgreSQL 13](https://ipinfo.io/blog/ingesting-ipinfo-geolocation-data-with-postgresql-13/)
- [Introducing a Simpler Way to get IP Address Data in Snowflake](https://ipinfo.io/blog/ip-address-data-in-snowflake/)

## FAQs

The list of FAQs (Frequently Asked Questions) can be found here [here](https://ipinfo.io/faq/category/137-data-downloads).

# Other Information (Usage, Exploration etc.)

### How to explore the sample databases

- Please visit the folders for each database. You can also find the API response samples there for each products.
- If you would like to explore CSV files, feel free to use any of these online services and import the raw CSV there -
    - [https://csvfiddle.io/](https://csvfiddle.io/)
    - [https://lite.datasette.io/](https://lite.datasette.io/)
- Or you can you just download the CSV files to take a closer look.

### Usage Information

- After signing up for database downloads service, you can either download the database from our website or you can `curl` the database from the database download endpoint. But make sure you have redirect [enabled](https://ipinfo.io/faq/article/142-when-i-access-the-database-endpoint-using-something-like-curl-it-doesn-t-seem-to-work-and-i-get-a-corrupted-empty-file-what-am-i-doing-wrong).
- You can select how frequently the database gets updated. It can be daily, weekly, bi-weekly or monthly.
- To lookup an specific database you can use any kind of data exploration package or database system you want to use. [Here is an example](https://ipinfo.io/faq/article/144-how-do-you-do-a-lookup-of-an-ip-address-using-your-database) of using mySQL and PosgreSQL to lookup a specific IP address.

<details id=0>
<summary><h1>Summary of the Databases Fields</h1></summary>

Please visit the database directories to learn more.

<details id=1>
<summary><h2>IP Geolocation</h2></summary>

**Get geolocation information from IP Addresses.**

The CSV database includes the following fields:

- start_ip
- end_ip
- join_key
- city
- region
- country
- latitude
- longitude
- postal_code
- timezone

### 🔗 [IP Geolocation Database Page](https://ipinfo.io/products/ip-geolocation-database)

### 🔗 IP Geolocation Repository

</details>

<details id=2>
<summary><h2>IP to Company</h2></summary>

**Get firmographics data and identify the company behind the IP Address and network traffic.**

Database includes the following fields:

- start_ip
- end_ip
- join_key
- name
- domain
- type
- asn
- as_name
- as_domain
- as_type
- country

### 🔗 [IP to Company Database Page](Sample%20Database%20fb322a60f0544458ad861eb738e869cd/IP%20to%20Company%20Database%2081d7f85aaeb244b19608f3a1de1fecad.md)

### 🔗 IP to Company Repository

</details>

<details id=3>
<summary><h2>ASN</h2></summary>


**Get ASN data from ASN or IP Address information.**

Database (CSV) contains the following fields:

- start_ip
- end_ip
- join_key
- asn
- domain
- name
- type
- country

### 🔗 [ASN Database Page](https://ipinfo.io/products/asn-database)

### 🔗 ASN Repository

</details>

<details id=4>
<summary><h2> IP to Mobile Carrier </h2></summary>

**Lookup Mobile Carrier data such as - MCC and MNC from IP addresses.** 

The database (CSV) contains the following fields:

- start_ip
- end_ip
- join_key
- name
- country
- mcc
- mnc

### 🔗 [IP to Mobile Carrier Database Page](https://ipinfo.io/products/mobile-ip-database)

### 🔗 IP to Mobile Carrier Repository

</details>

<details id=5>
<summary><h2>Privacy Detection</h2></summary>

**Privacy detection such as VPN, Tor, Proxies, Relays and Hosting from IP addresses. Demystify anonymous IP addresses.**

The CSV database includes the following fields:

- start_ip
- end_ip
- join_key
- hosting
- proxy
- tor
- vpn
- relay
- service

### 🔗 [Privacy Detection Database Page](https://ipinfo.io/products/anonymous-ip-database)

### 🔗 Privacy Detection Repository

</details>

<details id=6>
<summary><h2>Hosted Domains</h2></summary>

**Hosted Domains database enables you to do reverse IP lookups.** Through our Hosted Domains service, you can see the the full list of domain hosted on a single IP address. 

The fields in the database includes:

- ip
- total
- domains

### 🔗 [Hosted Domains Database Page](https://ipinfo.io/products/hosted-domains-database)

### 🔗 Hosted Domains Repository

</details>



<details id=7>
<summary><h2>Abuse Contact</h2></summary>

**Get the abuse contact information of every ISP in the internet.**

The fields of the database are:

- start_ip
- end_ip
- join_key
- name
- email
- address
- country
- phone

### 🔗 [Abuse Contact Database Page](https://ipinfo.io/products/ip-abuse-contact-database)

### 🔗 Abuse Contact Repository

</details>



<details id=8>
<summary><h2>WHOIS</h2></summary>



**IPinfo WHOIS database is contextual, robust and consistent database of various types of WHOIS data.**

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

### 🔗 Abuse Contact Repository

</details>

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