# [<img src="https://ipinfo.io/static/ipinfo-small.svg" alt="IPinfo" width="24"/>](https://ipinfo.io/) IPinfo Sample Database Repository


## Sample datasets of all the [IP address database products](https://ipinfo.io/account/data-downloads).


<p align="center">
  <img src="./assets/header_grahics_main_readme.png">
</p>

- [Database Overview](#database-overview)
- [Features of the Repository](#features-of-the-repository)
- [Summary of the Databases](#summary-of-the-databases)
    - [IP to Country](#ip-to-country)
    - [IP to ASN](#ip-to-asn)
    - [IP to Country + ASN](#ip-to-country--asn)
    - [IP Geolocation](#ip-geolocation)
    - [IP to Company](#ip-to-company)
    - [ASN Database](#asn-database)
    - [IP to Mobile Carrier](#ip-to-mobile-carrier)
    - [Privacy Detection](#privacy-detection--anonymous-ip-detection)
    - [Hosted Domains](#hosted-domains--reverse-ip-lookup)
    - [Abuse Contact](#abuse-contact)
    - [IP Geolocation Extended](#ip-geolocation-extended)
    - [Privacy Detection Extended](#privacy-detection-extended)
    - [IPinfo Lite](#ipinfo-lite-database)
    - [IPinfo Standard](#ipinfo-standard-database)
    - [IPinfo Plus](#ipinfo-plus-database)
    - [WHOIS](#whois)
- [Relevant Articles](#relevant-articles)
  - [Guides](#guides)
  - [FAQs](#faqs)
- [Found a bug?](#found-a-bug)
- [Interested in more?](#interested-in-more)
- [IPinfo Tools](#ipinfo-tools)
- [About IPinfo](#about-ipinfo)

# Database Overview

<p align="center">
  <img src="./assets/product_demo_main_readme.gif">
</p>

The database products [IPinfo.io](https://ipinfo.io) has to offer are -

| Database Product                                                               | Sample Database Repo                               | Description                                  |
| ------------------------------------------------------------------------------ | -------------------------------------------------- | -------------------------------------------- |
| [IP Geolocation Database](https://ipinfo.io/products/ip-geolocation-database)  | [IP Geolocation Sample](/IP%20Geolocation)         | IP geolocation information                   |
| [IP to Company Database](https://ipinfo.io/products/ip-company-database)       | [IP to Company Sample](/IP%20to%20Company)         | Company associated with IP address           |
| [ASN Database](https://ipinfo.io/products/asn-database)                        | [ASN Database Sample](/ASN%20Database)             | IP range and ASN information                 |
| [IP to Mobile Carrier Database](https://ipinfo.io/products/mobile-ip-database) | [IP to Mobile Sample](/IP%20to%20Mobile%20Carrier) | Mobile carrier and country information       |
| [Privacy Detection Database](https://ipinfo.io/products/anonymous-ip-database) | [Privacy Detection Sample](/Privacy%20Detection)   | VPN, proxy, Tor, relay detection             |
| [Hosted Domain Database](https://ipinfo.io/products/hosted-domains-database)   | [Hosted Domains Sample](/Hosted%20Domains)         | Reverse IP lookup                            |
| [Abuse Contact Database](https://ipinfo.io/products/ip-abuse-contact-database) | [Abuse Contact Sample](/Abuse%20Contact)           | Abuse contact information                    |
| [WHOIS Database](https://ipinfo.io/products/ip-whois-data-download)            | [WHOIS Sample](/WHOIS)                             | Contextualized and structured WHOIS database |


IPinfo also provides the following [IP databases for free](https://ipinfo.io/products/free-ip-database). The database provide full accuracy, daily updates and complete IP data solution. The databases are licensed under (CC BY-SA 4.0) and require an attribution statement, which can found on your account dashboard.

| Database Product                                                   | Sample Database Repo                                   | Description                                    |
| ------------------------------------------------------------------ | ------------------------------------------------------ | ---------------------------------------------- |
| [IP to Country](https://ipinfo.io/products/free-ip-database)       | [IP to Country Sample](/IP%20to%20Country)             | IP to Country Information                      |
| [IP to ASN](https://ipinfo.io/products/free-ip-database)           | [IP to ASN Sample](/IP%20to%20ASN)                     | IP to ASN information                          |
| [IP to Country + ASN](https://ipinfo.io/products/free-ip-database) | [IP to Country + ASN Sample](/IP%20to%20Country%20ASN) | Joined database of IP to Country and IP to ASN |


We offer a few detailed database that comes with additional columns that gives insights to the accuracy and our data methodology. These enterprise grade databases are only available upon request.

| Database Product                          | Sample Database Repo                                                       | Description                                                   |
| ----------------------------------------- | -------------------------------------------------------------------------- | ------------------------------------------------------------- |
| IP to Geolocation Extended Database       | [IP to Geolocation Extended Sample](/IP%20Geolocation%20Extended)          | IP to Geolocation database with accuracy radius               |
| IP to Privacy Detection Extended Database | [IP to Privacy Detection Extended Sample](/Privacy%20Detection%20Extended) | IP to Privacy Detection database detection method information |
| IP to Residential Proxy Database          | [IP to Residential Proxy Sample](/IP%20Residential%20Proxy)                | IP to residential proxy or ISP proxy detection data           |

From January 2025, we are offering several new IP database downloads that bundle multiple IP contexts in single data downloads

| Database Product | Sample Database Repo                     | Description                                                                 |
| ---------------- | ---------------------------------------- | --------------------------------------------------------------------------- |
| IPinfo Lite      | [IP Lite Sample](/IPinfo%20Lite)         | The ultimate free IP database from IPinfo                                   |
| IPinfo Plus      | [IP Standard Sample](/IPinfo%20Standard) | Location, ASN and newtork flags IP database                                 |
| IPinfo Standard  | [IP Plus Sample](/IPinfo%20Plus)         | Enterprise IP database with location, insights, network metadata, and flags |



**All of these products are available as CSV, JSON, Parquet and MMDB type.**

# Features of the Repository

Please visit each folder to learn more about the databases. Each directory README contains -

- Sample Dataset (100 rows) in `.csv`, `.json` and `.mmdb` format
- API response (in `.json`)
- Breakdown of the dataset with description of the fields
- Breakdown of the API response
- Helpful guides, resources and articles


# Summary of the Databases

Please visit the individual database directories to learn more. The database schemas were generated in May, 2024.

<details id=1>
<summary><h2>IP to Country</h2></summary>

**Get the country and continent information from IP addresses.**

You can find the schema, database sample, API response sample, and other information in the **[IP to Country folder](/IP%20to%20Country)**. The database includes the following fields:

| Field Name       | Example         | Description                                |
| ---------------- | --------------- | ------------------------------------------ |
| `start_ip`       | 217.220.0.0     | Starting IP address of an IP address range |
| `end_ip`         | 217.223.255.255 | Ending IP address of an IP address range   |
| `country`        | IT              | ISO 3166 country code of the IP addresses  |
| `country_name`   | Italy           | Name of the country                        |
| `continent`      | EU              | Continent code of the country              |
| `continent_name` | Europe          | Name of the continent                      |


</details>

<details id=2>
<summary><h2>IP to ASN</h2></summary>

**Get ASN information (limited) from an IP address range.**

You can find the schema, database sample, API response sample, and other information in the **[IP to ASN folder](/IP%20to%20ASN)**. The database includes the following fields:

| Field Name | Example       | Description                                       |
| ---------- | ------------- | ------------------------------------------------- |
| `start_ip` | 62.235.50.0   | Starting IP address of an IP address range        |
| `end_ip`   | 62.235.50.255 | Ending IP address of an IP address range          |
| `asn`      | AS29005       | Autonomous System Number                          |
| `name`     | Proximus NV   | Name of the AS (Autonomous System) organization   |
| `domain`   | proximus.com  | Official domain or website of the AS organization |


</details>


<details id=3>
<summary><h2>IP to Country + ASN</h2></summary>

**Joined database of IP to Country and IP to ASN database.**

You can find the schema, database sample, API response sample, and other information in the **[IP to Country ASN folder](/IP%20to%20Country%20ASN)**. The database includes the following fields:

| Field Name       | Example        | Description                                       |
| ---------------- | -------------- | ------------------------------------------------- |
| `start_ip`       | 194.87.139.0   | Starting IP address of an IP address range        |
| `end_ip`         | 194.87.139.255 | Ending IP address of an IP address range          |
| `country`        | NL             | ISO 3166 country code of the IP addresses         |
| `country_name`   | Netherlands    | Name of the country                               |
| `continent`      | EU             | Continent code of the country                     |
| `continent_name` | Europe         | Name of the continent                             |
| `asn`            | AS1239         | Autonomous System Number                          |
| `as_name`        | Sprint         | Name of the AS (Autonomous System) organization   |
| `as_domain`      | sprint.net     | Official domain or website of the AS organization |


</details>

<details id=4>
<summary><h2>IP Geolocation</h2></summary>

**Get geolocation information from IP addresses.**

You can find the schema, database sample, API response sample, and other information in the **[IP Geolocation folder](/IP%20Geolocation)**. The database includes the following fields:

| Field Name         | Example            | Description                                    |
| ------------------ | ------------------ | ---------------------------------------------- |
| **network**        | `71.50.174.48/28`  | CIDR or single Address of the IP address block |
| **city**           | `Spring Lake`      | City of the IP address                         |
| **region**         | `North Carolina`   | Region/State of the IP address                 |
| **region_code**    | `NC`               | Region code in two-letter format in ISO 3166   |
| **country**        | `United States`    | Name of the country of the IP address          |
| **country_code**   | `US`               | ISO 3166 country code of the IP address        |
| **continent**      | `North America`    | Name of the continent                          |
| **continent_code** | `NA`               | Continent name code in two-letter format       |
| **latitude**       | `35.16794`         | Latitude value of the IP address               |
| **longitude**      | `-78.97281`        | Longitude value of the IP address              |
| **timezone**       | `America/New_York` | Local timezone of the IP address location      |
| **postal_code**    | `28390`            | Postal code or zip code of the IP address      |


### 🔗 [IP Geolocation Database Product Page](https://ipinfo.io/products/ip-geolocation-database)

</details>

<details id=5>
<summary><h2>IP to Company</h2></summary>

**Get organization data and identify the company behind the IP address and network traffic.**

You can find the schema, database sample, API response sample, and other information in the **[IP to Company folder](/IP%20to%20Company)**. This database is can be used to identify large scale organization or companies behind IP address ranges. The database includes the following fields:

| Field Name  | Example                 | Description                                                |
| ----------- | ----------------------- | ---------------------------------------------------------- |
| `start_ip`  | 107.136.106.168         | Starting IP address of an IP address range                 |
| `end_ip`    | 107.136.106.175         | Ending IP address of an IP address range                   |
| `join_key`  | 107.136.0.0             | Special variable to facilitate database `join` operation   |
| `name`      | ZSPEC FLOW-180709174314 | Name of the organization                                   |
| `domain`    | zspec.com               | Domain of the organization                                 |
| `type`      | business                | Type of business. e.g. Business, ISP, Hosting or Education |
| `asn`       | AS7018                  | ASN of the IP range                                        |
| `as_name`   | AT&T Services, Inc.     | Name of the ASN                                            |
| `as_domain` | att.com                 | Domain name of the ASN                                     |
| `as_type`   | isp                     | ASN Type: ISP, Hosting, Business or Education              |
| `country`   | US                      | ISO 3166 country code                                      |



### 🔗 [IP to Company Database Product Page](https://ipinfo.io/products/ip-company-database)

</details>

<details id=6>
<summary><h2>ASN Database</h2></summary>


**Get ASN data from ASN or IP Address information.**

You can find the schema, database sample, API response sample, and other information in the **[ASN folder](/ASN%20Database)**. The Database contains the following fields:

| Field Name  | Example          | Description                                                               |
| ----------- | ---------------- | ------------------------------------------------------------------------- |
| **network** | `115.76.56.0/23` | CIDR or single IP address of the IP address block                         |
| **asn**     | `AS7552`         | Autonomous System Number (ASN)                                            |
| **domain**  | `viettel.com.vn` | Organization domain name of the ASN                                       |
| **name**    | `Viettel Group`  | Name of the ASN organization                                              |
| **type**    | `isp`            | ASN Type: ISP, Hosting, Education, Government or Business                 |
| **country** | `VN`             | ISO 3166 two letter country code of the ASN declared in the WHOIS records |


### 🔗 [ASN Database Product Page](https://ipinfo.io/products/asn-database)

</details>

<details id=7>
<summary><h2>IP to Mobile Carrier</h2></summary>

**Lookup Mobile Carrier data such as - MCC and MNC from IP addresses.** 

You can find the schema, database sample, API response sample, and other information in the **[IP to Mobile Carrier folder](/IP%20to%20Mobile%20Carrier)**. The database contains the following fields:

| Field Name | Example                                  | Description                                              |
| ---------- | ---------------------------------------- | -------------------------------------------------------- |
| `start_ip` | 5.208.203.0                              | Starting IP address of an IP address range               |
| `end_ip`   | 5.208.203.255                            | Ending IP address of an IP address range                 |
| `join_key` | 5.208.0.0                                | Special variable to facilitate database `join` operation |
| `name`     | Mobile Communication Company of Iran PLC | Name of the mobile carrier                               |
| `country`  | IR                                       | ISO 3166 country code                                    |
| `mcc`      | 432                                      | Mobile Country Code (MCC) of the carrier                 |
| `mnc`      | 11                                       | Mobile Network Code (MNC) of the carrier                 |



### 🔗 [IP to Mobile Carrier Database Product Page](https://ipinfo.io/products/mobile-ip-database)

</details>

<details id=8>
<summary><h2>Privacy Detection / Anonymous IP Detection</h2></summary>

**Demystify anonymous IP addresses. Identify privacy masking services such as VPN, Tor, proxies, relays and hosting from IP addresses.**

You can find the schema, database sample, API response sample, and other information in the **[Privacy Detection folder](/Privacy%20Detection)**. The database includes the following fields:

| Field Name  | Example             | Descrption                                                           |
| ----------- | ------------------- | -------------------------------------------------------------------- |
| **network** | `146.70.174.112/31` | CIDR or single IP address of the IP address block                    |
| **hosting** | `true`              | Indicates a hosting/cloud service/data center IP address             |
| **proxy**   | `false`             | Indicates a open web proxy IP address                                |
| **tor**     | `false`             | Indicates a TOR (The Onion Router) exit node IP address              |
| **relay**   | `false`             | Indicates Virtual Private Network (VPN) service exit node IP address |
| **vpn**     | `true`              | Indicates location preserving anonymous relay service                |
| **service** | `ProtonVPN`         | Name of the anonymous IP service provider                            |



### 🔗 [Privacy Detection Database Product Page](https://ipinfo.io/products/anonymous-ip-database)

</details>

<details id=9>
<summary><h2>Hosted Domains / Reverse IP Lookup</h2></summary>

**Hosted Domains database enables you to do reverse IP lookups.**

Through our Hosted Domains service, you can see the list of domains hosted on a single IP address. 

You can find the schema, database sample, API response sample, and other information in the **[Hosted Domains folder](/Hosted%20Domains)**. The database includes the following fields:

| Field Name | Example                                  | Description                                    |
| ---------- | ---------------------------------------- | ---------------------------------------------- |
| `ip`       | 135.125.236.225                          | IP address for reverse IP lookup               |
| `total`    | 3                                        | Number of domains registered to the IP Address |
| `domains`  | farmanaut.com,pharmanaut.be,farmanaut.be | Name of the domain(s) under the IP address     |


### 🔗 [Hosted Domains Database Product Page](https://ipinfo.io/products/hosted-domains-database)

</details>

<details id=10>
<summary><h2>Abuse Contact</h2></summary>

**Get the abuse contact information of every ISP on the internet.**

You can find the schema, database sample, API response sample, and other information in the **[Abuse Contact folder](/Abuse%20Contact)**. The database includes the following fields:

| Field Name | Example                                           | Description                                              |
| ---------- | ------------------------------------------------- | -------------------------------------------------------- |
| `start_ip` | 119.93.20.248                                     | Starting IP address of an IP address block               |
| `end_ip`   | 119.93.20.255                                     | Ending IP address of an IP address block                 |
| `join_key` | 119.93.0.0                                        | Special variable to facilitate database `join` operation |
| `name`     | Nilo Agir                                         | Name of the abuse contact                                |
| `email`    | abuse@pldt.net                                    | Organizational email of the abuse contact                |
| `address`  | Philippine Long Distance Telephone Company, 6/... | Organizational address of the abuse contact              |
| `country`  | PH                                                | ISO 3166 country code                                    |
| `phone`    | +632-584-1045                                     | Organizational phone number of the abuse contact         |


### 🔗 [Abuse Contact Database Product Page](https://ipinfo.io/products/ip-abuse-contact-database)

</details>

<details id=11>
<summary><h2>IP Geolocation Extended</h2></summary>

**IP to Geolocation database with confidence metric or accuracy radius for each entry**

You can find the schema, database sample, API response sample, and other information in the **[IP Geolocation Extended folder](/IP%20Geolocation%20Extended)**. The database includes the following fields:

| Field Name    | Example             | Description                                                  |
| ------------- | ------------------- | ------------------------------------------------------------ |
| `start_ip`    | 171.71.0.0          | Starting IP address of an IP address range                   |
| `end_ip`      | 171.71.127.255      | Ending IP address of an IP address range                     |
| `join_key`    | 171.71.0.0          | Special variable to facilitate database `join` operation     |
| `city`        | San Jose            | City of the location                                         |
| `region`      | California          | Region of the location                                       |
| `country`     | US                  | ISO 3166 country code of the location                        |
| `latitude`    | 37.4087             | Latitude value of the location                               |
| `longitude`   | -121.9406           | Longitude value of the location                              |
| `postal_code` | 95134               | Postal code of the location                                  |
| `timezone`    | America/Los_Angeles | Local time zone                                              |
| `geoname_id`  | 5392171             | `Geonames_id` from [geonames.org](https://www.geonames.org/) |
| `radius`      | 5                   | Accuracy radius in terms of kilometers                       |



</details>


<details id=12>
<summary><h2>Privacy Detection Extended</h2></summary>

**Get detection method for each private IP address**

You can find the schema, database sample, API response sample, and other information in the **[Privacy Detection Extended folder](/Privacy%20Detection%20Extended)**. The database includes the following fields:

 | Field Name          | Example         | Data Type                                                                                                                                                                                                                                                                                                                             | Descrption |
 | ------------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
 | **network**         | `45.129.35.234` | CIDR/IP Range or single IP address block                                                                                                                                                                                                                                                                                              |
 | **hosting**         | `true`          | Indicates a hosting/cloud service/data center IP address                                                                                                                                                                                                                                                                              |
 | **proxy**           | `false`         | Indicates a open web proxy IP address                                                                                                                                                                                                                                                                                                 |
 | **relay**           | `false`         | Indicates location preserving anonymous relay service                                                                                                                                                                                                                                                                                 |
 | **tor**             | `false`         | Indicates a TOR (The Onion Router) exit node IP address                                                                                                                                                                                                                                                                               |
 | **vpn**             | `true`          | Indicates Virtual Private Network (VPN) service exit node IP address                                                                                                                                                                                                                                                                  |
 | **service**         | `NordVPN`       | Name of the privacy service provider includes VPN, Proxy and Relay service providers names                                                                                                                                                                                                                                            |
 | **first_seen**      | `2024-10-31`    | Date when the activity on an anonymous IP address was first observed: Date in YYYY-MM-DD format, ISO-8601. Within the 3-month lookback period.                                                                                                                                                                                        |
 | **last_seen**       | `2025-01-03`    | Date when the activity on an anonymous IP address was last/recently observed: Date in YYYY-MM-DD format, ISO-8601.                                                                                                                                                                                                                    |
 | **confidence**      | `3`             | The level (from 1 to 3) of confidence attributed to the best source associated with this range                                                                                                                                                                                                                                        |
 | **coverage**        | `1.0`           | For inferred ranges (see `inferred` flag), represents the proportion of the range (in IP count) that we saw direct evidence of VPN activity on; the remaining percentage of the range (1 - coverage) is composed of IPs we did not directly observe. For IPs/ranges we've fully directly observed VPN evidence on, this value is 1.0. |
 | **census**          | `false`         | Ranges where we've observed VPN software/ports on; we run scans on ports and protocols commonly associated with VPN software. Ranges with the census flag are those where these scans obtained positive results                                                                                                                       |
 | **census_ports**    | ``              | The ports we've gotten positive results for when running our VPN detection census                                                                                                                                                                                                                                                     |
 | **device_activity** | `false`         | Ranges on which we've observed device activity compatible with VPN usage (outside of known infrastructure area; simultaneous use around a large area; pingable and/or associated with hosting providers)                                                                                                                              |
 | **inferred**        | `false`         | Whether the range associated with the record is the result of direct observation or inference based on neighboring IPs                                                                                                                                                                                                                |
 | **vpn_config**      | `true`          | Ranges where we confirmed VPN activity by directly running VPN software from almost 200 different providers and collecting exit IPs                                                                                                                                                                                                   |
 | **whois**           | `false`         | Ranges where we've observed VPN software/ports on AND have a WHOIS association with either VPNs in general or specific VPN providers. e.g. if our ipsec scan returned a positive result for an IP and its WHOIS record indicates that it is owned by a VPN provider, this flag will be true.                                          |

</details>

<details id=13>
<summary><h2>Residential Proxy Detection Database</h2></summary>

**Identify residential proxy IPs, including mobile network proxies, from more than 100 services**

You can find the schema, database sample, and other information in the **[Residential Proxy Detection folder](/IP%20Residential%20Proxy)**. The database includes the following fields:

| Fields              | Example          | Description                                                                                                                                                      |
| ------------------- | ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ip`                | 38.222.31.85     | IP address associated with a residential proxy.                                                                                                                  |
| `service`           | lightningproxies | Name of the residential proxy service. Carrier/mobile services are suffixed with `_mobile` (e.g., soax_mobile).                                                  |
| `last_seen`         | 2024-09-07       | Last recorded active date of a residential proxy IP in ISO 8601 format (YYYY-MM-DD), with the timezone set to UTC.                                               |
| `percent_days_seen` | 2                | Integer representing the percentage of days an IP was active over the past 90 days, indicating its activity level and frequency within a residential proxy pool. |


<details id=14>
<summary><h2>IPinfo Lite Database</h2></summary>

**IPinfo's free IP database provides location (country + continent) and ASN information in a single database.**

You can find the schema, database sample, and other information in the **[IPinfo Lite folder](/IPinfo%20Lite)**. The database includes the following fields:

| Field Name         | Example                 | Descrption                                                             |
| ------------------ | ----------------------- | ---------------------------------------------------------------------- |
| **network**        | `154.24.39.204/30`      | CIDR/IP range or single IP address                                     |
| **country**        | `Canada`                | Country name                                                           |
| **country_code**   | `CA`                    | Two-letter ISO 3166 country code of the IP addresses                   |
| **continent**      | `North America`         | Continent name of the IP location                                      |
| **continent_code** | `NA`                    | Two-letter continent code of the IP location                           |
| **asn**            | `AS174`                 | Autonomous System Number, an organization that owns the IP range block |
| **as_name**        | `Cogent Communications` | Name of the AS (Autonomous System Number) organization                 |
| **as_domain**      | `cogentco.com`          | Official domain or website of the ASN organization                     |


<details id=15>
<summary><h2>IPinfo Standard Database</h2></summary>

**IPinfo's Standard is a robust IP database that combines our location, ASN, and network flags data into a single database**

You can find the schema, database sample, and other information in the **[IPinfo Standard folder](/IPinfo%20Standard)**. The database includes the following fields:

| Field Name     | Example                       | Descrption                                                                  |
| -------------- | ----------------------------- | --------------------------------------------------------------------------- |
| network        | 66.202.64.131                 | CIDR/IP range or single IP address                                          |
| city           | Chicago                       | City of the IP address                                                      |
| region         | Illinois                      | Region/State of the IP address                                              |
| region_code    | IL                            | Region code in two-letter format in ISO 3166                                |
| country        | United States                 | Name of the country of the IP address                                       |
| country_code   | US                            | ISO 3166 country code of the IP address                                     |
| continent      | North America                 | Name of the continent                                                       |
| continent_code | NA                            | Continent name code in two-letter format                                    |
| latitude       | 41.85003                      | Latitude value of the IP address                                            |
| longitude      | -87.65005                     | Longitude value of the IP address                                           |
| timezone       | America/Chicago               | Local timezone of the IP address location                                   |
| postal_code    | 60666                         | Postal code or zip code of the IP address                                   |
| asn            | AS7029                        | Autonomous System Number (ASN)                                              |
| as_name        | Windstream Communications LLC | Organization domain name of the ASN                                         |
| as_domain      | windstream.com                | Name of the ASN organization                                                |
| as_type        | isp                           | ASN Type: ISP, Hosting, Education, Government or Business                   |
| is_anon        | false                         | Indicates whether the IP address is anonymous.                              |
| is_anycast     | false                         | dicates whether the IP address is an internet service hosting IP address    |
| is_hosting     | false                         | Indicates whether the IP address is an hosting/cloud/data center IP address |
| is_mobile      | false                         | Indicates whether the IP address belongs to a mobile network                |
| is_satellite   | false                         | Indicates whether the IP address is part of a satellite internet connection |



<details id=16>
<summary><h2>Residential Proxy Detection Database</h2></summary>

**IPinfo's Plus is an enterprise-grade IP database that includes location, insights, confidence, ASN, privacy, carrier, and network flags all in one.**

You can find the schema, database sample, and other information in the **[IPinfo Plus folder](/IPinfo%20Plus)**. The database includes the following fields:

| Field Name         | Example                        | Descrption                                                                                                 |
| ------------------ | ------------------------------ | ---------------------------------------------------------------------------------------------------------- |
| network            | 86.179.219.192/29              | CIDR/IP range or single IP address                                                                         |
| city               | Weymouth                       | City of the IP address                                                                                     |
| region             | England                        | Region/State of the IP address                                                                             |
| region_code        | ENG                            | Region code in two-letter format in ISO 3166                                                               |
| country            | United Kingdom                 | Name of the country of the IP address                                                                      |
| country_code       | GB                             | ISO 3166 country code of the IP address                                                                    |
| continent          | Europe                         | Name of the continent                                                                                      |
| continent_code     | EU                             | Continent name code in two-letter format                                                                   |
| latitude           | 50.61448                       | Latitude value of the IP address                                                                           |
| longitude          | -2.45991                       | Longitude value of the IP address                                                                          |
| timezone           | Europe/London                  | Local timezone of the IP address location                                                                  |
| postal_code        | DT3                            | Postal code or zip code of the IP address                                                                  |
| dma_code           | 13w                            | Direct Marketing Area (DMA) is a unique regional identifier for marketing.                                 |
| geoname_id         | 2634202                        | geonames.org's unique numercial identifier for geographic locations.                                       |
| radius             | 20                             | Location accuracy radius in terms of kilometers                                                            |
| city_confidence    | high                           | Indicates the accuracy of city-level geolocation data.                                                     |
| region_confidence  | high                           | Indicates the accuracy of region or state level geolocation data.                                          |
| country_confidence | high                           | Indicates the accuracy of country level geolocation data.                                                  |
| asn                | AS2856                         | Autonomous System Number (ASN)                                                                             |
| as_name            | British Telecommunications PLC | Organization domain name of the ASN                                                                        |
| as_domain          | bt.com                         | Name of the ASN organization                                                                               |
| as_type            | isp                            | ASN Type: ISP, Hosting, Education, Government or Business                                                  |
| carrier_name       |                                | Name of the mobile carrier organization                                                                    |
| mcc                |                                | Mobile Country Code (MCC) of the carrier                                                                   |
| mnc                |                                | Mobile Network Code (MNC) of the carrier                                                                   |
| as_changed         | 2025-01-10                     | Date when the IP address's ASN last changed: Date in YYYY-MM-DD format, ISO-8601                           |
| geo_changed        | 2024-11-10                     | Date when the IP address's location last changed: Date in YYYY-MM-DD format, ISO-8601                      |
| as_stability       | 1.0                            | The stability/change of ASN data for the IP address within a recent period of time. 1.0 means very stable. |
| geo_stability      | 1.0                            | The stability/change of locaion for the IP address within a recent period of time. 1.0 means very stable.  |
| is_anon            | false                          | Indicates whether the IP address is anonymous.                                                             |
| is_anycast         | false                          | dicates whether the IP address is an internet service hosting IP address                                   |
| is_hosting         | false                          | Indicates whether the IP address is an hosting/cloud/data center IP address                                |
| is_mobile          | false                          | Indicates whether the IP address belongs to a mobile network                                               |
| is_satellite       | false                          | Indicates whether the IP address is part of a satellite internet connection                                |
| is_proxy           | false                          | Indicates a open web proxy IP address                                                                      |
| is_relay           | false                          | Indicates location preserving anonymous relay service like iCloud private relay.                           |
| is_tor             | false                          | Indicates a TOR (The Onion Router) exit node IP address                                                    |
| is_vpn             | false                          | Indicates Virtual Private Network (VPN) service exit node IP address                                       |
| privacy_name       |                                | The name of the privacy service provider includes VPN, Proxy, or Relay service provider name               |
| cdn_name           |                                | Name of the CDN provider, if it is CDN IP address                                                          |

</details>

<details id=17>
<summary><h2>WHOIS</h2></summary>


**IPinfo WHOIS database is a contextual, robust and consistent database of various types of WHOIS data.**

You can find the schema, database sample, API response sample, and other information in the **[WHOIS folder](/WHOIS)**. The WHOIS database and their respective fields are listed below:

### R WHOIS

| Field Name  | Example                             | Description                         |
| ----------- | ----------------------------------- | ----------------------------------- |
| `range`     | 50.28.18.195                        | IP Address range/netblock           |
| `id`        | NETBLK-GRADOCEROPUB.50.28.18.195/32 | Raw netblock identifier from WHOIS  |
| `name`      | Grado Cero Publicidad S.A. de C.V.  | Name of netblock                    |
| `descr`     | GRADOCEROPUB-50.28.18.195           | Description                         |
| `host`      | rwhois.liquidweb.com:4321           | Host information                    |
| `country`   | MX                                  | ISO 3166 country code               |
| `email`     | webmaster@gradocero.com             | Contact email information           |
| `abuse`     | abuse@sourcedns.com                 | Abuse email information             |
| `domain`    | gradocero.com                       | Domain associated with the netblock |
| `country.1` | MX                                  | Secondary country information       |
| `city`      | Naucalpan de Juarez                 | City information                    |
| `street`    | Calle Andes #46                     | Street information                  |
| `postal`    | 53125                               | Postal Code information             |
| `updated`   | 2021-01-26 00:00:00                 | Update date in the WHOIS registry   |
| `imported`  | 2021-01-27 04:44:47.206483          | Imported date in the WHOIS registry |



### RIR WHOIS

| Field Name     | Example                                    | Description                                                                                                          |
| -------------- | ------------------------------------------ | -------------------------------------------------------------------------------------------------------------------- |
| `range`        | 45.142.160.224-45.142.161.255              | IP Address range/netblock                                                                                            |
| `id`           | PL-DOMYNET-NETWORK                         | Raw netblock identifier from WHOIS                                                                                   |
| `name`         | DomyNet Sp. z o.o.                         | Name of netblock                                                                                                     |
| `country`      | PL                                         | ISO 3166 country code                                                                                                |
| `status`       | ASSIGNED PA                                | Range assignment type ([RIPE’s documentation](https://www.ripe.net/publications/docs/ripe-733))                      |
| `tech`         | PK9274-RIPE                                | ID for technical contact of WHOIS record                                                                             |
| `maintainer`   | MNT-PL-DOMYNET-1                           | ID for contact authorized to update WHOIS record for netblock                                                        |
| `admin`        | PK9274-RIPE                                | ID for administrative contact of netblock                                                                            |
| `source`       | ripe                                       | RIR associated with record (RIPE, ARIN, etc.)                                                                        |
| `whois_domain` | domynet.pl                                 | Domain name (from WHOIS entry)                                                                                       |
| `updated`      | 2020-01-09                                 | Last updated date (taken from WHOIS entry)                                                                           |
| `org`          | ORG-DSZO39-RIPE                            | ID or name of organization responsible for netblock                                                                  |
| `rdns_domain`  | domynet.pl                                 | Domain associated with IP range (only available if a majority of IPs within range share a common reverse DNS domain) |
| `domain`       | domynet.pl                                 | Domain associated with netblock (based on our data sets)                                                             |
| `geoloc`       | 52.2260524 20.9941955                      | Latitude/longitude coordinates indicating where users of network are located                                         |
| `org_address`  | ul. Lindleya 16/301 02-013 Warszawa POLAND | Address of the associated organization                                                                               |
| `asn`          | AS208348                                   | Autonomous system number for organization that routes traffic for IP (based on BGP routing data)                     |
| `as_name`      | DomyNet Sp. z o.o.                         | Name of AS (based on our data sets and data processing)                                                              |
| `as_domain`    | domynet.pl                                 | Domain of AS (based on our data sets and data processing)                                                            |
| `as_type`      | isp                                        | ISP, business, or hosting (based on around 20 different features and our custom training set)                        |



<details id=18>
<summary><h3>Other WHOIS Databases</h3></summary>

Other kinds of WHOIS Database IPinfo offers:

| WHOIS ASN | WHOIS MNT | WHOIS NET | WHOIS ORG  | WHOIS POC   |
| --------- | --------- | --------- | ---------- | ----------- |
| id        | id        | range     | id         | id          |
| name      | name      | id        | name       | name        |
| country   | admin_id  | name      | address    | mobilephone |
| org_id    | tech_id   | country   | street     | officephone |
| created   | org_id    | domain    | city       | fax         |
| updated   | created   | org_id    | state      | addres      |
| source    | updated   | status    | postalcode | country     |
| raw       | source    | tech_id   | country    | email       |
|           | raw       | mnt_id    | admin_id   | abuse_email |
|           |           | admin_id  | tech_id    | created     |
|           |           | created   | abuse_id   | updated     |
|           |           | updated   | mnt_id     | source      |
|           |           | source    | email      | raw         |
|           |           | raw       | domain     |             |
|           |           |           | created    |             |
|           |           |           | updated    |             |
|           |           |           | source     |             |
|           |           |           | raw        |             |


</details>

### 🔗 [WHOIS Database Product Page](https://ipinfo.io/products/ip-whois-data-download)

</details>

# Relevant Articles

## Guides

We highly recommend exploring the [IPinfo community](https://community.ipinfo.io/) for posts and detailed instructions on using our database. Feel free to participate in the community if you have any questions.

- [Database downloads articles in the community](https://community.ipinfo.io/c/docs/database-downloads/10)
- [Lookup IP geolocation and ASN with ClickHouse and IPinfo’s free database](https://community.ipinfo.io/t/lookup-ip-geolocation-and-asn-with-clickhouse-and-ipinfos-free-database/149)
- [https://community.ipinfo.io/t/using-ipinfo-s-data-downloads-in-postgresql/1000](https://community.ipinfo.io/t/using-ipinfo-s-data-downloads-in-postgresql/1000)
- [Querying IPinfo IP databases inside BigQuery](https://community.ipinfo.io/t/querying-ipinfo-ip-databases-inside-bigquery/4579)
- [Using IPinfo’s MMDB data downloads with Golang](https://community.ipinfo.io/t/using-ipinfos-mmdb-data-downloads-with-golang/4415)
- [How to choose the best file format for your IPinfo database?](https://ipinfo.io/blog/ipinfo-database-formats/)
- [How to get IP data and IP location in C# with IPinfo](https://ipinfo.io/blog/ip-geolocation-c-sharp/)
- [Our downloadable IP WHOIS data sets are live!](https://ipinfo.io/blog/our-downloadable-ip-whois-data-sets-are-live)
- [Data downloads vs API, or both?](https://ipinfo.io/blog/data-downloads-vs-api-or-both/)
- [Ingesting IPinfo geolocation data with PostgreSQL 13](https://ipinfo.io/blog/ingesting-ipinfo-geolocation-data-with-postgresql-13/)
- [Introducing a Simpler Way to get IP Address Data in Snowflake](https://ipinfo.io/blog/ip-address-data-in-snowflake/)
- [IP data enrichment with IPinfo: 4 ways to add insights to your traffic/server logs](https://ipinfo.io/blog/ip-data-enrichment-in-4-ways/)
- [Meet IPinfo’s Free IP Data Downloads](https://ipinfo.io/blog/meet-free-ip-address-database/)

## FAQs

The list of FAQs (Frequently Asked Questions) can be found [here](https://ipinfo.io/faq/category/137-data-downloads) or in the [IPinfo Community](https://community.ipinfo.io/).

# Found a bug?

If you found an issue or would like to submit an improvement to this project, please submit an issue using the issues tab above. If you would like to submit a PR with a fix, reference the issue you created!

# Interested in more?

Currently, we are limiting the sample datasets to only **100 rows**. If you would like to request a larger sample or would like to get a quote on the database products, **[feel free to reach to us](https://ipinfo.io/products/ip-database-download#request_form)**.

Follow us on [Twitter](https://twitter.com/ipinfo) and [LinkedIn](https://www.linkedin.com/company/ipinfo/) to learn more about IP Address data and it’s fascinating potential.

---

# IPinfo Tools

There are official IPinfo client libraries available for many languages including PHP, Python, Go, Java, Ruby, and many popular frameworks such as Django, Rails and Laravel. There are also many third party libraries and integrations available for our API.

We also have an excellent CLI tool (**1700 Stars on Github**) and mapping tool.

See [https://ipinfo.io/developers/libraries](https://ipinfo.io/developers/libraries) for more details.

# About IPinfo

Founded in 2013, IPinfo prides itself on being the most reliable, accurate, and in-depth source of IP address data available anywhere. We process terabytes of data to produce our custom IP geolocation, company, carrier, VPN detection, hosted domains, and IP type data sets. Our API handles over 40 billion requests a month for 100,000 businesses and developers.

[![image](https://avatars3.githubusercontent.com/u/15721521?s=128&u=7bb7dde5c4991335fb234e68a30971944abc6bf3&v=4)](https://ipinfo.io/)
