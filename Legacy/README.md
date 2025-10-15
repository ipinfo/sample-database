# [<img src="https://ipinfo.io/static/ipinfo-small.svg" alt="IPinfo" width="24"/>](https://ipinfo.io/) IPinfo Sample Database Repository

## Legacy IP Database Downloads

IPinfo recommends that new users avoid the following legacy IP database downloads. We now offer multi-contextual IP databases that provide a richer mix of IP context in a single data package.

**User Question: I want city-level information on IP addresses. Should I choose IPinfo Core or the IP Geolocation Database?**

You should choose the IPinfo Core database. It includes detailed location information, such as city-level data, and network flags that provide valuable geolocation context. For example, carrier IPs often have lower geolocation confidence, and anonymous IP addresses are used by VPN services. This context is not available in single-context IP geolocation data.

**User Question: I want confident, accurate insights. Which database should I choose?**

Choose IPinfo Plus. It combines the reliability of the IP Geolocation Extended database with additional insightful IP geolocation data.

**User Question: I want to mix X IP insights with Y IP insights.**

Review the offerings in Lite, Core, Plus, and other options first. While we can provide custom database solutions, standard off-the-shelf data solutions are more accessible and require less engineering investment. Custom solutions are available if needed.

## Database Overview

The legacy IP database products from [IPinfo](https://ipinfo.io) include:

| Database Product                                                               | Sample Database Repo                                 | Description                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------|----------------------------------------------|
| [IP Geolocation Database](https://ipinfo.io/products/ip-geolocation-database)  | [IP Geolocation Sample](../IP%20Geolocation)         | IP geolocation information                   |
| [IP to Company Database](https://ipinfo.io/products/ip-company-database)       | [IP to Company Sample](../IP%20to%20Company)         | Company associated with IP address           |
| [ASN Database](https://ipinfo.io/products/asn-database)                        | [ASN Database Sample](../ASN%20Database)             | IP range and ASN information                 |
| [IP to Mobile Carrier Database](https://ipinfo.io/products/mobile-ip-database) | [IP to Mobile Carrier Sample](../IP%20to%20Mobile%20Carrier) | Mobile carrier and country information       |
| [Privacy Detection Database](https://ipinfo.io/products/anonymous-ip-database) | [Privacy Detection Sample](../Privacy%20Detection)   | VPN, proxy, Tor, relay detection             |
| IP Geolocation Extended Database                                              | [IP Geolocation Extended Sample](../IP%20Geolocation%20Extended)          | IP geolocation database with accuracy radius |

**All of these products are available in CSV, JSON, Parquet, and MMDB formats.**

## Features of the Repository

Visit each folder to learn more about the databases. Each directory README contains detailed information about the respective database.

## Summary of the Databases

Visit the individual database directories to learn more.

<details>
<summary><h2>IP Geolocation</h2></summary>

**Get geolocation information from IP addresses.**

You can find the schema, database sample, API response sample, and other information in the **[IP Geolocation folder](../IP%20Geolocation)**. The database includes the following fields:

| Field Name         | Example            | Description                                    |
| ------------------ | ------------------ | ---------------------------------------------- |
| **network**        | `71.50.174.48/28`  | CIDR or single address of the IP address block |
| **city**           | `Spring Lake`      | City of the IP address                         |
| **region**         | `North Carolina`   | Region/State of the IP address                 |
| **region_code**    | `NC`               | Two-letter ISO 3166 region code                |
| **country**        | `United States`    | Name of the country of the IP address          |
| **country_code**   | `US`               | ISO 3166 country code of the IP address        |
| **continent**      | `North America`    | Name of the continent                          |
| **continent_code** | `NA`               | Two-letter continent code                      |
| **latitude**       | `35.16794`         | Latitude value of the IP address               |
| **longitude**      | `-78.97281`        | Longitude value of the IP address              |
| **timezone**       | `America/New_York` | Local time zone of the IP address location     |
| **postal_code**    | `28390`            | Postal code or ZIP code of the IP address      |

### 🔗 [IP Geolocation Database Product Page](https://ipinfo.io/products/ip-geolocation-database)

</details>

<details>
<summary><h2>IP to Company</h2></summary>

**Get organization data and identify the company behind the IP address and network traffic.**

You can find the schema, database sample, API response sample, and other information in the **[IP to Company folder](../IP%20to%20Company)**. This database can be used to identify large-scale organizations or companies behind IP address ranges. The database includes the following fields:

| Field Name  | Example                 | Description                                                |
| ----------- | ----------------------- | ---------------------------------------------------------- |
| `start_ip`  | 107.136.106.168         | Starting IP address of an IP address range                 |
| `end_ip`    | 107.136.106.175         | Ending IP address of an IP address range                   |
| `join_key`  | 107.136.0.0             | Special variable to facilitate database `join` operation   |
| `name`      | ZSPEC FLOW-180709174314 | Name of the organization                                   |
| `domain`    | zspec.com               | Domain of the organization                                 |
| `type`      | business                | Type of business, e.g., Business, ISP, Hosting, or Education |
| `asn`       | AS7018                  | ASN of the IP range                                        |
| `as_name`   | AT&T Services, Inc.     | Name of the ASN                                            |
| `as_domain` | att.com                 | Domain name of the ASN                                     |
| `as_type`   | isp                     | ASN Type: ISP, Hosting, Business, or Education              |
| `country`   | US                      | ISO 3166 country code                                      |

### 🔗 [IP to Company Database Product Page](https://ipinfo.io/products/ip-company-database)

</details>

<details>
<summary><h2>ASN Database</h2></summary>

**Get ASN data from ASN or IP Address information.**

You can find the schema, database sample, API response sample, and other information in the **[ASN folder](../ASN%20Database)**. The database contains the following fields:

| Field Name  | Example          | Description                                                               |
| ----------- | ---------------- | ------------------------------------------------------------------------- |
| **network** | `115.76.56.0/23` | CIDR or single IP address of the IP address block                         |
| **asn**     | `AS7552`         | Autonomous System Number (ASN)                                            |
| **domain**  | `viettel.com.vn` | Organization domain name of the ASN                                       |
| **name**    | `Viettel Group`  | Name of the ASN organization                                              |
| **type**    | `isp`            | ASN Type: ISP, Hosting, Education, Government, or Business                |
| **country** | `VN`             | ISO 3166 two-letter country code of the ASN declared in the WHOIS records |

### 🔗 [ASN Database Product Page](https://ipinfo.io/products/asn-database)

</details>

<details>
<summary><h2>IP to Mobile Carrier</h2></summary>

**Look up mobile carrier data such as MCC and MNC from IP addresses.**

You can find the schema, database sample, API response sample, and other information in the **[IP to Mobile Carrier folder](../IP%20to%20Mobile%20Carrier)**. The database contains the following fields:

| Field Name | Example                                  | Description                                              |
| ---------- | ---------------------------------------- | -------------------------------------------------------- |
| `start_ip` | 5.208.203.0                              | Starting IP address of an IP address range               |
| `end_ip`   | 5.208.203.255                            | Ending IP address of an IP address range                 |
| `name`     | Mobile Communication Company of Iran PLC | Name of the mobile carrier                               |
| `country`  | IR                                       | ISO 3166 country code                                    |
| `mcc`      | 432                                      | Mobile Country Code (MCC) of the carrier                 |
| `mnc`      | 11                                       | Mobile Network Code (MNC) of the carrier                 |

### 🔗 [IP to Mobile Carrier Database Product Page](https://ipinfo.io/products/mobile-ip-database)

</details>

<details>
<summary><h2>Privacy Detection / Anonymous IP Detection</h2></summary>

**Demystify anonymous IP addresses. Identify privacy-masking services such as VPN, Tor, proxies, relays, and hosting from IP addresses.**

You can find the schema, database sample, API response sample, and other information in the **[Privacy Detection folder](../Privacy%20Detection)**. The database includes the following fields:

| Field Name  | Example             | Description                                                          |
| ----------- | ------------------- | -------------------------------------------------------------------- |
| **network** | `146.70.174.112/31` | CIDR or single IP address of the IP address block                    |
| **hosting** | `true`              | Indicates a hosting/cloud service/data center IP address             |
| **proxy**   | `false`             | Indicates an open web proxy IP address                               |
| **tor**     | `false`             | Indicates a Tor (The Onion Router) exit node IP address              |
| **relay**   | `false`             | Indicates a Virtual Private Network (VPN) service exit node IP address |
| **vpn**     | `true`              | Indicates a location-preserving anonymous relay service              |
| **service** | `ProtonVPN`         | Name of the anonymous IP service provider                            |

### 🔗 [Privacy Detection Database Product Page](https://ipinfo.io/products/anonymous-ip-database)

</details>

<details>
<summary><h2>IP Geolocation Extended</h2></summary>

**IP to Geolocation database with confidence metric or accuracy radius for each entry.**

You can find the schema, database sample, API response sample, and other information in the **[IP Geolocation Extended folder](../IP%20Geolocation%20Extended)**. The database includes the following fields:

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
| `geoname_id`  | 5392171             | GeoNames ID from geonames.org                                |
| `radius`      | 5                   | Accuracy radius in terms of kilometers                       |

</details>
