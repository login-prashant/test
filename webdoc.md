[Skip to main content](#main)

[](https://www.microsoft.com)

Contents

Exit focus mode

-   Bookmark
-   [Feedback](#feedback "Send feedback about this page")
-   [Edit](https://github.com/MicrosoftDocs/BusinessApplicationPlatform-Connectors/blob/live/docs/hyasinsight/index.yml "Edit This Document")
-   Share
    -   Twitter
    -   LinkedIn
    -   Facebook
    -   Email

Table of contents

HYAS Insight (Preview)
======================

![](https://connectoricons-prod.azureedge.net/releases/v1.0.1403/1.0.1403.2163/hyasinsight/icon.png)

HYAS Insight integration to Microsoft Azure Sentinel provides direct,
high volume access to HYAS Insight data. It enables investigators and
analysts to understand and defend against cyber adversaries and their
infrastructure.

### In this article

This connector is available in the following products and regions:

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Service              Class      Regions
  -------------------- ---------- -----------------------------------------------------------------------------------------------------------------------------------------------
  **Logic Apps**       Standard   All [Logic Apps regions](https://azure.microsoft.com/global-infrastructure/services/?products=logic-apps&regions=all) except the following: \
                                   - Azure Government regions \
                                   - Azure China regions

  **Power Automate**   Premium    All [Power Automate regions](/en-us/flow/regions-overview) except the following: \
                                   - US Government (GCC) \
                                   - US Government (GCC High) \
                                   - China Cloud operated by 21Vianet

  **Power Apps**       Premium    All [Power Apps regions](/en-us/powerapps/administrator/regions-overview#what-regions-are-available) except the following: \
                                   - US Government (GCC) \
                                   - US Government (GCC High) \
                                   - China Cloud operated by 21Vianet
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

  Contact   
  --------- --------------------------------------------------------------
  Name      HYAS Infosec
  URL       [https://www.hyas.com/contact](https://www.hyas.com/contact)
  Email     support@hyas.com

  Connector Metadata   
  -------------------- ------------------------------------------------------------------------------------
  Publisher            HYAS Infosec
  Website              [https://www.hyas.com](https://www.hyas.com)
  Privacy policy       [https://www.hyas.com/privacy-statement/](https://www.hyas.com/privacy-statement/)
  Categories           Security;Website

Pre-requisites
--------------

You will need the following to proceed:

-   A Microsoft Power Apps or Power Automate plan with custom connector
    feature
-   An Azure subscription
-   HYAS Insight API Key

Support and documentation:
--------------------------

For all the support requests and general queries you can contact
support@hyas.com or visit [contact-us](https://www.hyas.com/contact)

Creating a connection
---------------------

To connect your account, you will need the following information:

+--------------------------+--------------------------+--------------------------+
| Name                     | Type                     | Description              |
+==========================+==========================+==========================+
| HYAS Insight API Key     | securestring             | The HYAS Insight API Key |
|                          |                          | for this api             |
+--------------------------+--------------------------+--------------------------+

Throttling Limits {#limits}
-----------------

  Name                       Calls   Renewal Period
  -------------------------- ------- ----------------
  API calls per connection   100     60 seconds

Actions
-------

+--------------------------------------+--------------------------------------+
| [Retrieve Current WHOIS information  | Retrieve Current WHOIS enrichment    |
| for                                  | data for domain.                     |
| domain](#retrieve-current-whois-info |                                      |
| rmation-for-domain)                  |                                      |
+--------------------------------------+--------------------------------------+
| [Retrieve Device Geo information for | Retrieve Device Geo enrichment data  |
| IPv4                                 | for IPv4 address.                    |
| address](#retrieve-device-geo-inform |                                      |
| ation-for-ipv4-address)              |                                      |
+--------------------------------------+--------------------------------------+
| [Retrieve Device Geo information for | Retrieve Device Geo enrichment data  |
| IPv6                                 | for IPv6 address.                    |
| address](#retrieve-device-geo-inform |                                      |
| ation-for-ipv6-address)              |                                      |
+--------------------------------------+--------------------------------------+
| [Retrieve Dynamic DNS information    | Retrieve Dynamic DNS enrichment data |
| for email                            | for email address.                   |
| address](#retrieve-dynamic-dns-infor |                                      |
| mation-for-email-address)            |                                      |
+--------------------------------------+--------------------------------------+
| [Retrieve Dynamic DNS information    | Retrieve Dynamic DNS enrichment data |
| for IP                               | for IP address.                      |
| address](#retrieve-dynamic-dns-infor |                                      |
| mation-for-ip-address)               |                                      |
+--------------------------------------+--------------------------------------+
| [Retrieve Historic WHOIS information | Retrieve Historic WHOIS enrichment   |
| for                                  | data for domain.                     |
| domain](#retrieve-historic-whois-inf |                                      |
| ormation-for-domain)                 |                                      |
+--------------------------------------+--------------------------------------+
| [Retrieve Historic WHOIS information | Retrieve Historic WHOIS enrichment   |
| for email                            | data for email address.              |
| address](#retrieve-historic-whois-in |                                      |
| formation-for-email-address)         |                                      |
+--------------------------------------+--------------------------------------+
| [Retrieve Historic WHOIS information | Retrieve Historic WHOIS enrichment   |
| for phone                            | data for phone number.               |
| number](#retrieve-historic-whois-inf |                                      |
| ormation-for-phone-number)           |                                      |
+--------------------------------------+--------------------------------------+
| [Retrieve Passive DNS information    | Retrieve Passive DNS enrichment data |
| for                                  | for domain.                          |
| domain](#retrieve-passive-dns-inform |                                      |
| ation-for-domain)                    |                                      |
+--------------------------------------+--------------------------------------+
| [Retrieve Passive DNS information    | Retrieve Passive DNS enrichment data |
| for IP                               | for IP address.                      |
| address](#retrieve-passive-dns-infor |                                      |
| mation-for-ip-address)               |                                      |
+--------------------------------------+--------------------------------------+
| [Retrieve Passive Hash information   | Retrieve Passive Hash enrichment     |
| for IP                               | data for IP address.                 |
| address](#retrieve-passive-hash-info |                                      |
| rmation-for-ip-address)              |                                      |
+--------------------------------------+--------------------------------------+
| [Retrieve Sinkhole information for   | Retrieve Sinkhole enrichment data    |
| IP                                   | for IP address.                      |
| address](#retrieve-sinkhole-informat |                                      |
| ion-for-ip-address)                  |                                      |
+--------------------------------------+--------------------------------------+
| [Retrieve SSL certificate            | Retrieve SSL certificate enrichment  |
| information for IP                   | data for IP address.                 |
| address](#retrieve-ssl-certificate-i |                                      |
| nformation-for-ip-address)           |                                      |
+--------------------------------------+--------------------------------------+

### Retrieve Current WHOIS information for domain

Operation ID:
:   DOMAIN\_WHOIS\_CURRENT

Retrieve Current WHOIS enrichment data for domain.

#### Parameters {#required-parameters}

+----------------+----------------+----------------+----------------+----------------+
| Name           | Key            | Required       | Type           | Description    |
+================+================+================+================+================+
| Domain         | domain         | True           | string         | Domain you     |
|                |                |                |                | want to        |
|                |                |                |                | enrich.        |
+----------------+----------------+----------------+----------------+----------------+

#### Returns

+--------------------+--------------------+--------------------+--------------------+
| Name               | Path               | Type               | Description        |
+====================+====================+====================+====================+
| items              | items              | array of object    | The items object.  |
+--------------------+--------------------+--------------------+--------------------+
| abuse\_emails      | items.abuse\_email | array of string    | The abuse emails   |
|                    | s                  |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| address            | items.address      | array of string    | The address        |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| city               | items.city         | array of string    | The city of the    |
|                    |                    |                    | registrant.        |
+--------------------+--------------------+--------------------+--------------------+
| country            | items.country      | array of string    | The country of the |
|                    |                    |                    | registrant.        |
+--------------------+--------------------+--------------------+--------------------+
| data               | items.data         | string             | The data           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| datetime           | items.datetime     | string             | The datetime       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| domain             | items.domain       | string             | The domain of the  |
|                    |                    |                    | registrant.        |
+--------------------+--------------------+--------------------+--------------------+
| domain\_2tld       | items.domain\_2tld | string             | The second-level   |
|                    |                    |                    | domain of the      |
|                    |                    |                    | registrant.        |
+--------------------+--------------------+--------------------+--------------------+
| domain\_created\_d | items.domain\_crea | string             | The date and time  |
| atetime            | ted\_datetime      |                    | when the Whois     |
|                    |                    |                    | record was         |
|                    |                    |                    | created.           |
+--------------------+--------------------+--------------------+--------------------+
| domain\_expires\_d | items.domain\_expi | string             | The date and time  |
| atetime            | res\_datetime      |                    | when the Whois     |
|                    |                    |                    | record expires.    |
+--------------------+--------------------+--------------------+--------------------+
| domain\_updated\_d | items.domain\_upda | string             | The date and time  |
| atetime            | ted\_datetime      |                    | when the Whois     |
|                    |                    |                    | record was last    |
|                    |                    |                    | updated.           |
+--------------------+--------------------+--------------------+--------------------+
| email              | items.email        | array of string    | The email          |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| idn\_name          | items.idn\_name    | string             | The international  |
|                    |                    |                    | domain name        |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| meta\_data         | items.meta\_data   | string             | The metadata       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| name               | items.name         | array of string    | The contact name   |
|                    |                    |                    | (registrant        |
|                    |                    |                    | contact,           |
|                    |                    |                    | administrative     |
|                    |                    |                    | contact, technical |
|                    |                    |                    | contact, or abuse  |
|                    |                    |                    | contact.)          |
+--------------------+--------------------+--------------------+--------------------+
| nameserver         | items.nameserver   | array of string    | The nameserver     |
|                    |                    |                    | domain.            |
+--------------------+--------------------+--------------------+--------------------+
| organization       | items.organization | array of string    | The organization   |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| phone              | items.phone        | array of string    | The phone number   |
|                    |                    |                    | of the registrant  |
|                    |                    |                    | in e164 format.    |
+--------------------+--------------------+--------------------+--------------------+
| registrar          | items.registrar    | string             | The domain         |
|                    |                    |                    | registrar.         |
+--------------------+--------------------+--------------------+--------------------+
| state              | items.state        | array of string    | The state where    |
|                    |                    |                    | domain was         |
|                    |                    |                    | registered.        |
+--------------------+--------------------+--------------------+--------------------+
| whois\_hash        | items.whois\_hash  | string             | The hash           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| whois\_id          | items.whois\_id    | string             | The whois id       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| whois\_nameserver  | items.whois\_names | array of object    | The                |
|                    | erver              |                    | whois\_nameserver  |
|                    |                    |                    | object.            |
+--------------------+--------------------+--------------------+--------------------+
| domain             | items.whois\_names | string             | The nameserver’s   |
|                    | erver.domain       |                    | domain             |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| domain\_2tld       | items.whois\_names | string             | The nameserver’s   |
|                    | erver.domain\_2tld |                    | domain\_2tld       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| whois\_related\_na | items.whois\_names | string             | The nameserver’s   |
| meserver\_id       | erver.whois\_relat |                    | Id Information.    |
|                    | ed\_nameserver\_id |                    |                    |
+--------------------+--------------------+--------------------+--------------------+
| whois\_pii         | items.whois\_pii   | array of object    | The whois\_pii     |
|                    |                    |                    | object.            |
+--------------------+--------------------+--------------------+--------------------+
| address            | items.whois\_pii.a | string             | The personal       |
|                    | ddress             |                    | identity address   |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| city               | items.whois\_pii.c | string             | The personal       |
|                    | ity                |                    | identity city      |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| data               | items.whois\_pii.d | string             | The personal       |
|                    | ata                |                    | identity data      |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| email              | items.whois\_pii.e | string             | The personal       |
|                    | mail               |                    | identity email     |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| geo\_country\_alph | items.whois\_pii.g | string             | The personal       |
| a\_2               | eo\_country\_alpha |                    | identity country   |
|                    | \_2                |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| name               | items.whois\_pii.n | string             | The personal       |
|                    | ame                |                    | identity name      |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| organization       | items.whois\_pii.o | string             | The personal       |
|                    | rganization        |                    | identity           |
|                    |                    |                    | organization       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| phone\_e164        | items.whois\_pii.p | string             | The personal       |
|                    | hone\_e164         |                    | identity           |
|                    |                    |                    | Phone\_e164        |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| state              | items.whois\_pii.s | string             | The personal       |
|                    | tate               |                    | identity state     |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| whois\_related\_pi | items.whois\_pii.w | string             | The personal       |
| i\_id              | hois\_related\_pii |                    | identity Id        |
|                    | \_id               |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| whois\_related\_ty | items.whois\_pii.w | string             | The personal       |
| pe                 | hois\_related\_typ |                    | identity related   |
|                    | e                  |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| source             | source             | string             | The source         |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| total\_count       | total\_count       | integer            | The total count    |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+

### Retrieve Device Geo information for IPv4 address

Operation ID:
:   IPV4\_DEVICE\_GEO

Retrieve Device Geo enrichment data for IPv4 address.

#### Parameters {#required-parameters}

+----------------+----------------+----------------+----------------+----------------+
| Name           | Key            | Required       | Type           | Description    |
+================+================+================+================+================+
| IPv4 address   | ipv4           | True           | string         | IPv4 address   |
|                |                |                |                | you want to    |
|                |                |                |                | enrich.        |
+----------------+----------------+----------------+----------------+----------------+

#### Returns {#returns}

+--------------------+--------------------+--------------------+--------------------+
| Name               | Path               | Type               | Description        |
+====================+====================+====================+====================+
|                    |                    | array of object    |                    |
+--------------------+--------------------+--------------------+--------------------+
| datetime           | datetime           | string             | A date-time string |
|                    |                    |                    | in RFC 3339        |
|                    |                    |                    | format.            |
+--------------------+--------------------+--------------------+--------------------+
| device\_geo\_id    | device\_geo\_id    | string             | Internal record    |
|                    |                    |                    | ID.                |
+--------------------+--------------------+--------------------+--------------------+
| device\_user\_agen | device\_user\_agen | string             | The user agent     |
| t                  | t                  |                    | string for the     |
|                    |                    |                    | device.            |
+--------------------+--------------------+--------------------+--------------------+
| geo\_country\_alph | geo\_country\_alph | string             | The ISO 3316       |
| a\_2               | a\_2               |                    | alpha-2 code for   |
|                    |                    |                    | the country        |
|                    |                    |                    | associated with    |
|                    |                    |                    | the lat/long       |
|                    |                    |                    | reported.          |
+--------------------+--------------------+--------------------+--------------------+
|                    | geo\_horizontal\_a | float              | The GPS horizontal |
|                    | ccuracy            |                    | accuracy.          |
+--------------------+--------------------+--------------------+--------------------+
| ipv4               | ipv4               | string             | The ipv4 address   |
|                    |                    |                    | assigned to the    |
|                    |                    |                    | device. A device   |
|                    |                    |                    | may have either or |
|                    |                    |                    | ipv4 and ipv6.     |
+--------------------+--------------------+--------------------+--------------------+
| ipv6               | ipv6               | string             | The ipv6 address   |
|                    |                    |                    | assigned to the    |
|                    |                    |                    | device. A device   |
|                    |                    |                    | may have either or |
|                    |                    |                    | ipv4 and ipv6.     |
+--------------------+--------------------+--------------------+--------------------+
| latitude           | latitude           | float              | Units are degrees  |
|                    |                    |                    | on the WGS 84      |
|                    |                    |                    | spheroid.          |
+--------------------+--------------------+--------------------+--------------------+
| longitude          | longitude          | float              | Units are degrees  |
|                    |                    |                    | on the WGS 84      |
|                    |                    |                    | spheroid.          |
+--------------------+--------------------+--------------------+--------------------+
| wifi\_bssid        | wifi\_bssid        | string             | The BSSID (MAC     |
|                    |                    |                    | address) of the    |
|                    |                    |                    | wifi router that   |
|                    |                    |                    | the device         |
|                    |                    |                    | communicated       |
|                    |                    |                    | through.           |
+--------------------+--------------------+--------------------+--------------------+
| wifi\_ssid         | wifi\_ssid         | string             | The SSID (name) of |
|                    |                    |                    | the wifi network   |
|                    |                    |                    | that the device    |
|                    |                    |                    | communicated       |
|                    |                    |                    | through.           |
+--------------------+--------------------+--------------------+--------------------+

### Retrieve Device Geo information for IPv6 address

Operation ID:
:   IPV6\_DEVICE\_GEO

Retrieve Device Geo enrichment data for IPv6 address.

#### Parameters {#required-parameters}

+----------------+----------------+----------------+----------------+----------------+
| Name           | Key            | Required       | Type           | Description    |
+================+================+================+================+================+
| IPv6 address   | ipv6           | True           | string         | IPv6 address   |
|                |                |                |                | you want to    |
|                |                |                |                | enrich.        |
+----------------+----------------+----------------+----------------+----------------+

#### Returns {#returns}

+--------------------+--------------------+--------------------+--------------------+
| Name               | Path               | Type               | Description        |
+====================+====================+====================+====================+
|                    |                    | array of object    |                    |
+--------------------+--------------------+--------------------+--------------------+
| datetime           | datetime           | string             | A date-time string |
|                    |                    |                    | in RFC 3339        |
|                    |                    |                    | format.            |
+--------------------+--------------------+--------------------+--------------------+
| device\_geo\_id    | device\_geo\_id    | string             | Internal record    |
|                    |                    |                    | ID.                |
+--------------------+--------------------+--------------------+--------------------+
| device\_user\_agen | device\_user\_agen | string             | The user agent     |
| t                  | t                  |                    | string for the     |
|                    |                    |                    | device.            |
+--------------------+--------------------+--------------------+--------------------+
| geo\_country\_alph | geo\_country\_alph | string             | The ISO 3316       |
| a\_2               | a\_2               |                    | alpha-2 code for   |
|                    |                    |                    | the country        |
|                    |                    |                    | associated with    |
|                    |                    |                    | the lat/long       |
|                    |                    |                    | reported.          |
+--------------------+--------------------+--------------------+--------------------+
|                    | geo\_horizontal\_a | float              | The GPS horizontal |
|                    | ccuracy            |                    | accuracy.          |
+--------------------+--------------------+--------------------+--------------------+
| ipv4               | ipv4               | string             | The ipv4 address   |
|                    |                    |                    | assigned to the    |
|                    |                    |                    | device. A device   |
|                    |                    |                    | may have either or |
|                    |                    |                    | ipv4 and ipv6.     |
+--------------------+--------------------+--------------------+--------------------+
| ipv6               | ipv6               | string             | The ipv6 address   |
|                    |                    |                    | assigned to the    |
|                    |                    |                    | device. A device   |
|                    |                    |                    | may have either or |
|                    |                    |                    | ipv4 and ipv6.     |
+--------------------+--------------------+--------------------+--------------------+
| latitude           | latitude           | float              | Units are degrees  |
|                    |                    |                    | on the WGS 84      |
|                    |                    |                    | spheroid.          |
+--------------------+--------------------+--------------------+--------------------+
| longitude          | longitude          | float              | Units are degrees  |
|                    |                    |                    | on the WGS 84      |
|                    |                    |                    | spheroid.          |
+--------------------+--------------------+--------------------+--------------------+
| wifi\_bssid        | wifi\_bssid        | string             | The BSSID (MAC     |
|                    |                    |                    | address) of the    |
|                    |                    |                    | wifi router that   |
|                    |                    |                    | the device         |
|                    |                    |                    | communicated       |
|                    |                    |                    | through.           |
+--------------------+--------------------+--------------------+--------------------+
| wifi\_ssid         | wifi\_ssid         | string             | The SSID (name) of |
|                    |                    |                    | the wifi network   |
|                    |                    |                    | that the device    |
|                    |                    |                    | communicated       |
|                    |                    |                    | through.           |
+--------------------+--------------------+--------------------+--------------------+

### Retrieve Dynamic DNS information for email address

Operation ID:
:   EMAIL\_DYNAMIC\_DNS

Retrieve Dynamic DNS enrichment data for email address.

#### Parameters {#required-parameters}

+----------------+----------------+----------------+----------------+----------------+
| Name           | Key            | Required       | Type           | Description    |
+================+================+================+================+================+
| Email address  | email          | True           | string         | Email address  |
|                |                |                |                | you want to    |
|                |                |                |                | enrich.        |
+----------------+----------------+----------------+----------------+----------------+

#### Returns {#returns}

+--------------------+--------------------+--------------------+--------------------+
| Name               | Path               | Type               | Description        |
+====================+====================+====================+====================+
|                    |                    | array of object    |                    |
+--------------------+--------------------+--------------------+--------------------+
| a\_record          | a\_record          | string             | The A record for   |
|                    |                    |                    | the domain.        |
+--------------------+--------------------+--------------------+--------------------+
| account            | account            | string             | The account holder |
|                    |                    |                    | name.              |
+--------------------+--------------------+--------------------+--------------------+
| created            | created            | string             | The date which the |
|                    |                    |                    | domain was         |
|                    |                    |                    | created.           |
+--------------------+--------------------+--------------------+--------------------+
| created\_ip        | created\_ip        | string             | The ip address of  |
|                    |                    |                    | the account        |
|                    |                    |                    | holder.            |
+--------------------+--------------------+--------------------+--------------------+
| domain             | domain             | string             | The domain         |
|                    |                    |                    | associated with    |
|                    |                    |                    | the dynamic dns    |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| domain\_creator\_i | domain\_creator\_i | string             | The ip address of  |
| p                  | p                  |                    | the domain         |
|                    |                    |                    | creator.           |
+--------------------+--------------------+--------------------+--------------------+
| email              | email              | string             | The email address  |
|                    |                    |                    | connected to the   |
|                    |                    |                    | domain.            |
+--------------------+--------------------+--------------------+--------------------+

### Retrieve Dynamic DNS information for IP address

Operation ID:
:   IP\_DYNAMIC\_DNS

Retrieve Dynamic DNS enrichment data for IP address.

#### Parameters {#required-parameters}

+----------------+----------------+----------------+----------------+----------------+
| Name           | Key            | Required       | Type           | Description    |
+================+================+================+================+================+
| IPv4 address   | ip             | True           | string         | IPv4 address   |
|                |                |                |                | you want to    |
|                |                |                |                | enrich.        |
+----------------+----------------+----------------+----------------+----------------+

#### Returns {#returns}

+--------------------+--------------------+--------------------+--------------------+
| Name               | Path               | Type               | Description        |
+====================+====================+====================+====================+
|                    |                    | array of object    |                    |
+--------------------+--------------------+--------------------+--------------------+
| a\_record          | a\_record          | string             | The A record for   |
|                    |                    |                    | the domain.        |
+--------------------+--------------------+--------------------+--------------------+
| account            | account            | string             | The account holder |
|                    |                    |                    | name.              |
+--------------------+--------------------+--------------------+--------------------+
| created            | created            | string             | The date which the |
|                    |                    |                    | domain was         |
|                    |                    |                    | created.           |
+--------------------+--------------------+--------------------+--------------------+
| created\_ip        | created\_ip        | string             | The ip address of  |
|                    |                    |                    | the account        |
|                    |                    |                    | holder.            |
+--------------------+--------------------+--------------------+--------------------+
| domain             | domain             | string             | The domain         |
|                    |                    |                    | associated with    |
|                    |                    |                    | the dynamic dns    |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| domain\_creator\_i | domain\_creator\_i | string             | The ip address of  |
| p                  | p                  |                    | the domain         |
|                    |                    |                    | creator.           |
+--------------------+--------------------+--------------------+--------------------+
| email              | email              | string             | The email address  |
|                    |                    |                    | connected to the   |
|                    |                    |                    | domain.            |
+--------------------+--------------------+--------------------+--------------------+

### Retrieve Historic WHOIS information for domain

Operation ID:
:   DOMAIN\_WHOIS\_HISTORIC

Retrieve Historic WHOIS enrichment data for domain.

#### Parameters {#required-parameters}

+----------------+----------------+----------------+----------------+----------------+
| Name           | Key            | Required       | Type           | Description    |
+================+================+================+================+================+
| Domain         | domain         | True           | string         | Domain you     |
|                |                |                |                | want to        |
|                |                |                |                | enrich.        |
+----------------+----------------+----------------+----------------+----------------+

#### Returns {#returns}

+--------------------+--------------------+--------------------+--------------------+
| Name               | Path               | Type               | Description        |
+====================+====================+====================+====================+
|                    |                    | array of object    |                    |
+--------------------+--------------------+--------------------+--------------------+
| address            | address            | array of string    | The address        |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| city               | city               | array of string    | The city           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| country            | country            | array of string    | The country        |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| data               | data               | string             | The data           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| datetime           | datetime           | string             | The datetime       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| domain             | domain             | string             | The domain of the  |
|                    |                    |                    | registrant.        |
+--------------------+--------------------+--------------------+--------------------+
| domain\_2tld       | domain\_2tld       | string             | The second-level   |
|                    |                    |                    | domain of the      |
|                    |                    |                    | registrant.        |
+--------------------+--------------------+--------------------+--------------------+
| domain\_created\_d | domain\_created\_d | string             | The date and time  |
| atetime            | atetime            |                    | when the whois     |
|                    |                    |                    | record was         |
|                    |                    |                    | created.           |
+--------------------+--------------------+--------------------+--------------------+
| domain\_expires\_d | domain\_expires\_d | string             | The date and time  |
| atetime            | atetime            |                    | when the whois     |
|                    |                    |                    | record expires.    |
+--------------------+--------------------+--------------------+--------------------+
| domain\_updated\_d | domain\_updated\_d | string             | The date and time  |
| atetime            | atetime            |                    | when the whois     |
|                    |                    |                    | record was last    |
|                    |                    |                    | updated.           |
+--------------------+--------------------+--------------------+--------------------+
| email              | email              | array of string    | The email          |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| idn\_name          | idn\_name          | string             | The international  |
|                    |                    |                    | domain name.       |
+--------------------+--------------------+--------------------+--------------------+
| meta\_data         | meta\_data         | string             | The metadata       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| name               | name               | array of string    | The name           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| nameserver         | nameserver         | array of string    | The nameserver     |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| phone              | phone              | array of object    | Array of object,   |
|                    |                    |                    | The phone number   |
|                    |                    |                    | registrant contact |
|                    |                    |                    | in e164 format     |
|                    |                    |                    | along with geo     |
|                    |                    |                    | info.              |
+--------------------+--------------------+--------------------+--------------------+
| phone              | phone.phone        | string             | The phone number   |
|                    |                    |                    | registrant contact |
|                    |                    |                    | in e164 format.    |
+--------------------+--------------------+--------------------+--------------------+
| carrier            | phone.phone\_info. | string             | Phone number       |
|                    | carrier            |                    | carrier.           |
+--------------------+--------------------+--------------------+--------------------+
| country            | phone.phone\_info. | string             | Phone number       |
|                    | country            |                    | country.           |
+--------------------+--------------------+--------------------+--------------------+
| geo                | phone.phone\_info. | string             | Phone number geo   |
|                    | geo                |                    | Can be city or     |
|                    |                    |                    | province or region |
|                    |                    |                    | or country.        |
+--------------------+--------------------+--------------------+--------------------+
| privacy\_punch     | privacy\_punch     | boolean            | True if this       |
|                    |                    |                    | record has         |
|                    |                    |                    | additional         |
|                    |                    |                    | information        |
|                    |                    |                    | bypassing privacy  |
|                    |                    |                    | protect.           |
+--------------------+--------------------+--------------------+--------------------+
| registrar          | registrar          | string             | The domain         |
|                    |                    |                    | registrar.         |
+--------------------+--------------------+--------------------+--------------------+
| whois\_hash        | whois\_hash        | string             | The hash           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| whois\_id          | whois\_id          | string             | The whois id       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+

### Retrieve Historic WHOIS information for email address

Operation ID:
:   EMAIL\_WHOIS\_HISTORIC

Retrieve Historic WHOIS enrichment data for email address.

#### Parameters {#required-parameters}

+----------------+----------------+----------------+----------------+----------------+
| Name           | Key            | Required       | Type           | Description    |
+================+================+================+================+================+
| Email address  | email          | True           | string         | Email address  |
|                |                |                |                | you want to    |
|                |                |                |                | enrich.        |
+----------------+----------------+----------------+----------------+----------------+

#### Returns {#returns}

+--------------------+--------------------+--------------------+--------------------+
| Name               | Path               | Type               | Description        |
+====================+====================+====================+====================+
|                    |                    | array of object    |                    |
+--------------------+--------------------+--------------------+--------------------+
| address            | address            | array of string    | The address        |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| city               | city               | array of string    | The city           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| country            | country            | array of string    | The country        |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| data               | data               | string             | The data           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| datetime           | datetime           | string             | The datetime       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| domain             | domain             | string             | The domain of the  |
|                    |                    |                    | registrant.        |
+--------------------+--------------------+--------------------+--------------------+
| domain\_2tld       | domain\_2tld       | string             | The second-level   |
|                    |                    |                    | domain of the      |
|                    |                    |                    | registrant.        |
+--------------------+--------------------+--------------------+--------------------+
| domain\_created\_d | domain\_created\_d | string             | The date and time  |
| atetime            | atetime            |                    | when the whois     |
|                    |                    |                    | record was         |
|                    |                    |                    | created.           |
+--------------------+--------------------+--------------------+--------------------+
| domain\_expires\_d | domain\_expires\_d | string             | The date and time  |
| atetime            | atetime            |                    | when the whois     |
|                    |                    |                    | record expires.    |
+--------------------+--------------------+--------------------+--------------------+
| domain\_updated\_d | domain\_updated\_d | string             | The date and time  |
| atetime            | atetime            |                    | when the whois     |
|                    |                    |                    | record was last    |
|                    |                    |                    | updated.           |
+--------------------+--------------------+--------------------+--------------------+
| email              | email              | array of string    | The email          |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| idn\_name          | idn\_name          | string             | The international  |
|                    |                    |                    | domain name.       |
+--------------------+--------------------+--------------------+--------------------+
| meta\_data         | meta\_data         | string             | The metadata       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| name               | name               | array of string    | The name           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| nameserver         | nameserver         | array of string    | The nameserver     |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| phone              | phone              | array of object    | Array of object,   |
|                    |                    |                    | The phone number   |
|                    |                    |                    | registrant contact |
|                    |                    |                    | in e164 format     |
|                    |                    |                    | along with geo     |
|                    |                    |                    | info.              |
+--------------------+--------------------+--------------------+--------------------+
| phone              | phone.phone        | string             | The phone number   |
|                    |                    |                    | registrant contact |
|                    |                    |                    | in e164 format.    |
+--------------------+--------------------+--------------------+--------------------+
| carrier            | phone.phone\_info. | string             | Phone number       |
|                    | carrier            |                    | carrier.           |
+--------------------+--------------------+--------------------+--------------------+
| country            | phone.phone\_info. | string             | Phone number       |
|                    | country            |                    | country.           |
+--------------------+--------------------+--------------------+--------------------+
| geo                | phone.phone\_info. | string             | Phone number geo   |
|                    | geo                |                    | Can be city or     |
|                    |                    |                    | province or region |
|                    |                    |                    | or country.        |
+--------------------+--------------------+--------------------+--------------------+
| privacy\_punch     | privacy\_punch     | boolean            | True if this       |
|                    |                    |                    | record has         |
|                    |                    |                    | additional         |
|                    |                    |                    | information        |
|                    |                    |                    | bypassing privacy  |
|                    |                    |                    | protect.           |
+--------------------+--------------------+--------------------+--------------------+
| registrar          | registrar          | string             | The domain         |
|                    |                    |                    | registrar.         |
+--------------------+--------------------+--------------------+--------------------+
| whois\_hash        | whois\_hash        | string             | The hash           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| whois\_id          | whois\_id          | string             | The whois id       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+

### Retrieve Historic WHOIS information for phone number

Operation ID:
:   PHONE\_WHOIS\_HISTORIC

Retrieve Historic WHOIS enrichment data for phone number.

#### Parameters {#required-parameters}

+----------------+----------------+----------------+----------------+----------------+
| Name           | Key            | Required       | Type           | Description    |
+================+================+================+================+================+
| Phone number   | phone          | True           | string         | Phone number   |
|                |                |                |                | you want to    |
|                |                |                |                | enrich. ( e164 |
|                |                |                |                | format. Eg: (  |
|                |                |                |                | +41585855634 ) |
|                |                |                |                | )              |
+----------------+----------------+----------------+----------------+----------------+

#### Returns {#returns}

+--------------------+--------------------+--------------------+--------------------+
| Name               | Path               | Type               | Description        |
+====================+====================+====================+====================+
|                    |                    | array of object    |                    |
+--------------------+--------------------+--------------------+--------------------+
| address            | address            | array of string    | The address        |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| city               | city               | array of string    | The city           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| country            | country            | array of string    | The country        |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| data               | data               | string             | The data           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| datetime           | datetime           | string             | The datetime       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| domain             | domain             | string             | The domain of the  |
|                    |                    |                    | registrant.        |
+--------------------+--------------------+--------------------+--------------------+
| domain\_2tld       | domain\_2tld       | string             | The second-level   |
|                    |                    |                    | domain of the      |
|                    |                    |                    | registrant.        |
+--------------------+--------------------+--------------------+--------------------+
| domain\_created\_d | domain\_created\_d | string             | The date and time  |
| atetime            | atetime            |                    | when the whois     |
|                    |                    |                    | record was         |
|                    |                    |                    | created.           |
+--------------------+--------------------+--------------------+--------------------+
| domain\_expires\_d | domain\_expires\_d | string             | The date and time  |
| atetime            | atetime            |                    | when the whois     |
|                    |                    |                    | record expires.    |
+--------------------+--------------------+--------------------+--------------------+
| domain\_updated\_d | domain\_updated\_d | string             | The date and time  |
| atetime            | atetime            |                    | when the whois     |
|                    |                    |                    | record was last    |
|                    |                    |                    | updated.           |
+--------------------+--------------------+--------------------+--------------------+
| email              | email              | array of string    | The email          |
|                    |                    |                    | information        |
+--------------------+--------------------+--------------------+--------------------+
| idn\_name          | idn\_name          | string             | The international  |
|                    |                    |                    | domain name.       |
+--------------------+--------------------+--------------------+--------------------+
| meta\_data         | meta\_data         | string             | The metadata       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| name               | name               | array of string    | The name           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| nameserver         | nameserver         | array of string    | The nameserver     |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| phone              | phone              | array of object    | Array of object,   |
|                    |                    |                    | The phone number   |
|                    |                    |                    | registrant contact |
|                    |                    |                    | in e164 format     |
|                    |                    |                    | along with geo     |
|                    |                    |                    | info.              |
+--------------------+--------------------+--------------------+--------------------+
| phone              | phone.phone        | string             | The phone number   |
|                    |                    |                    | registrant contact |
|                    |                    |                    | in e164 format.    |
+--------------------+--------------------+--------------------+--------------------+
| carrier            | phone.phone\_info. | string             | Phone number       |
|                    | carrier            |                    | carrier.           |
+--------------------+--------------------+--------------------+--------------------+
| country            | phone.phone\_info. | string             | Phone number       |
|                    | country            |                    | country.           |
+--------------------+--------------------+--------------------+--------------------+
| geo                | phone.phone\_info. | string             | Phone number geo   |
|                    | geo                |                    | Can be city or     |
|                    |                    |                    | province or region |
|                    |                    |                    | or country.        |
+--------------------+--------------------+--------------------+--------------------+
| privacy\_punch     | privacy\_punch     | boolean            | True if this       |
|                    |                    |                    | record has         |
|                    |                    |                    | additional         |
|                    |                    |                    | information        |
|                    |                    |                    | bypassing privacy  |
|                    |                    |                    | protect.           |
+--------------------+--------------------+--------------------+--------------------+
| registrar          | registrar          | string             | The domain         |
|                    |                    |                    | registrar.         |
+--------------------+--------------------+--------------------+--------------------+
| whois\_hash        | whois\_hash        | string             | The hash           |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+
| whois\_id          | whois\_id          | string             | The whois id       |
|                    |                    |                    | information.       |
+--------------------+--------------------+--------------------+--------------------+

### Retrieve Passive DNS information for domain

Operation ID:
:   DOMAIN\_PASSIVE\_DNS

Retrieve Passive DNS enrichment data for domain.

#### Parameters {#required-parameters}

+----------------+----------------+----------------+----------------+----------------+
| Name           | Key            | Required       | Type           | Description    |
+================+================+================+================+================+
| Domain         | domain         | True           | string         | Domain you     |
|                |                |                |                | want to        |
|                |                |                |                | enrich.        |
+----------------+----------------+----------------+----------------+----------------+

#### Returns {#returns}

+--------------------+--------------------+--------------------+--------------------+
| Name               | Path               | Type               | Description        |
+====================+====================+====================+====================+
|                    |                    | array of object    |                    |
+--------------------+--------------------+--------------------+--------------------+
| cert\_name         | cert\_name         | string             | The certificate    |
|                    |                    |                    | provider name.     |
+--------------------+--------------------+--------------------+--------------------+
| count              | count              | integer            | The passive dns    |
|                    |                    |                    | count.             |
+--------------------+--------------------+--------------------+--------------------+
| domain             | domain             | string             | The domain of the  |
|                    |                    |                    | passive dns        |
|                    |                    |                    | information        |
|                    |                    |                    | requested.         |
+--------------------+--------------------+--------------------+--------------------+
| first\_seen        | first\_seen        | string             | The first time     |
|                    |                    |                    | this domain was    |
|                    |                    |                    | seen.              |
+--------------------+--------------------+--------------------+--------------------+
| city\_name         | ip.geo.city\_name  | string             | City of the ip     |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| country\_iso\_code | ip.geo.country\_is | string             | Country ISO code   |
|                    | o\_code            |                    | of the ip          |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| country\_name      | ip.geo.country\_na | string             | Country name of    |
|                    | me                 |                    | the ip             |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| location\_latitude | ip.geo.location\_l | string             | The latitude of    |
|                    | atitude            |                    | the ip             |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| location\_longitud | ip.geo.location\_l | string             | The longitude of   |
| e                  | ongitude           |                    | the ip             |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| postal\_code       | ip.geo.postal\_cod | string             | The postalcode of  |
|                    | e                  |                    | the ip             |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| ip                 | ip.ip              | string             | IP of the          |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| autonomous\_system | ip.isp.autonomous\ | string             | The ASN of the ip. |
| \_number           | _system\_number    |                    |                    |
+--------------------+--------------------+--------------------+--------------------+
| autonomous\_system | ip.isp.autonomous\ | string             | The ASO of the ip. |
| \_organization     | _system\_organizat |                    |                    |
|                    | ion                |                    |                    |
+--------------------+--------------------+--------------------+--------------------+
| ip\_address        | ip.isp.ip\_address | string             | The IP.            |
+--------------------+--------------------+--------------------+--------------------+
| isp                | ip.isp.isp         | string             | The Internet       |
|                    |                    |                    | Service Provider.  |
+--------------------+--------------------+--------------------+--------------------+
| organization       | ip.isp.organizatio | string             | The ISP            |
|                    | n                  |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| ipv4               | ipv4               | string             | The ipv4 address   |
|                    |                    |                    | of the passive dns |
|                    |                    |                    | record.            |
+--------------------+--------------------+--------------------+--------------------+
| ipv6               | ipv6               | string             | The ipv6 address   |
|                    |                    |                    | of the passive dns |
|                    |                    |                    | record.            |
+--------------------+--------------------+--------------------+--------------------+
| last\_seen         | last\_seen         | string             | The last time this |
|                    |                    |                    | domain was seen.   |
+--------------------+--------------------+--------------------+--------------------+
| sha1               | sha1               | string             | The sha1.          |
+--------------------+--------------------+--------------------+--------------------+
| sources            | sources            | array of string    | A list of pDNS     |
|                    |                    |                    | providers which    |
|                    |                    |                    | the data came      |
|                    |                    |                    | from.              |
+--------------------+--------------------+--------------------+--------------------+

### Retrieve Passive DNS information for IP address

Operation ID:
:   IP\_PASSIVE\_DNS

Retrieve Passive DNS enrichment data for IP address.

#### Parameters {#required-parameters}

+----------------+----------------+----------------+----------------+----------------+
| Name           | Key            | Required       | Type           | Description    |
+================+================+================+================+================+
| IPv4 address   | ipv4           | True           | string         | IPv4 address   |
|                |                |                |                | you want to    |
|                |                |                |                | enrich.        |
+----------------+----------------+----------------+----------------+----------------+

#### Returns {#returns}

+--------------------+--------------------+--------------------+--------------------+
| Name               | Path               | Type               | Description        |
+====================+====================+====================+====================+
|                    |                    | array of object    |                    |
+--------------------+--------------------+--------------------+--------------------+
| cert\_name         | cert\_name         | string             | The certificate    |
|                    |                    |                    | provider name.     |
+--------------------+--------------------+--------------------+--------------------+
| count              | count              | integer            | The passive dns    |
|                    |                    |                    | count.             |
+--------------------+--------------------+--------------------+--------------------+
| domain             | domain             | string             | The domain of the  |
|                    |                    |                    | passive dns        |
|                    |                    |                    | information        |
|                    |                    |                    | requested.         |
+--------------------+--------------------+--------------------+--------------------+
| first\_seen        | first\_seen        | string             | The first time     |
|                    |                    |                    | this domain was    |
|                    |                    |                    | seen.              |
+--------------------+--------------------+--------------------+--------------------+
| city\_name         | ip.geo.city\_name  | string             | City of the ip     |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| country\_iso\_code | ip.geo.country\_is | string             | Country ISO code   |
|                    | o\_code            |                    | of the ip          |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| country\_name      | ip.geo.country\_na | string             | Country name of    |
|                    | me                 |                    | the ip             |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| location\_latitude | ip.geo.location\_l | string             | The latitude of    |
|                    | atitude            |                    | the ip             |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| location\_longitud | ip.geo.location\_l | string             | The longitude of   |
| e                  | ongitude           |                    | the ip             |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| postal\_code       | ip.geo.postal\_cod | string             | The postalcode of  |
|                    | e                  |                    | the ip             |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| ip                 | ip.ip              | string             | IP of the          |
|                    |                    |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| autonomous\_system | ip.isp.autonomous\ | string             | The ASN of the ip. |
| \_number           | _system\_number    |                    |                    |
+--------------------+--------------------+--------------------+--------------------+
| autonomous\_system | ip.isp.autonomous\ | string             | The ASO of the ip. |
| \_organization     | _system\_organizat |                    |                    |
|                    | ion                |                    |                    |
+--------------------+--------------------+--------------------+--------------------+
| ip\_address        | ip.isp.ip\_address | string             | The IP.            |
+--------------------+--------------------+--------------------+--------------------+
| isp                | ip.isp.isp         | string             | The Internet       |
|                    |                    |                    | Service Provider.  |
+--------------------+--------------------+--------------------+--------------------+
| organization       | ip.isp.organizatio | string             | The ISP            |
|                    | n                  |                    | organization.      |
+--------------------+--------------------+--------------------+--------------------+
| ipv4               | ipv4               | string             | The ipv4 address   |
|                    |                    |                    | of the passive dns |
|                    |                    |                    | record.            |
+--------------------+--------------------+--------------------+--------------------+
| ipv6               | ipv6               | string             | The ipv6 address   |
|                    |                    |                    | of the passive dns |
|                    |                    |                    | record.            |
+--------------------+--------------------+--------------------+--------------------+
| last\_seen         | last\_seen         | string             | The last time this |
|                    |                    |                    | domain was seen.   |
+--------------------+--------------------+--------------------+--------------------+
| sha1               | sha1               | string             | The sha1.          |
+--------------------+--------------------+--------------------+--------------------+
| sources            | sources            | array of string    | A list of pDNS     |
|                    |                    |                    | providers which    |
|                    |                    |                    | the data came      |
|                    |                    |                    | from.              |
+--------------------+--------------------+--------------------+--------------------+

### Retrieve Passive Hash information for IP address

Operation ID:
:   PASSIVE\_HASH

Retrieve Passive Hash enrichment data for IP address.

#### Parameters {#required-parameters}

+----------------+----------------+----------------+----------------+----------------+
| Name           | Key            | Required       | Type           | Description    |
+================+================+================+================+================+
| IPv4 address   | ipv4           | True           | string         | IPv4 address   |
|                |                |                |                | you want to    |
|                |                |                |                | enrich.        |
+----------------+----------------+----------------+----------------+----------------+

#### Returns {#returns}

+--------------------+--------------------+--------------------+--------------------+
| Name               | Path               | Type               | Description        |
+====================+====================+====================+====================+
|                    |                    | array of object    |                    |
+--------------------+--------------------+--------------------+--------------------+
| domain             | domain             | string             | The domain of the  |
|                    |                    |                    | passive hash       |
|                    |                    |                    | information        |
|                    |                    |                    | requested.         |
+--------------------+--------------------+--------------------+--------------------+
| md5\_count         | md5\_count         | integer            | The passive dns    |
|                    |                    |                    | count.             |
+--------------------+--------------------+--------------------+--------------------+

### Retrieve Sinkhole information for IP address

Operation ID:
:   SINKHOLE

Retrieve Sinkhole enrichment data for IP address.

#### Parameters {#required-parameters}

+----------------+----------------+----------------+----------------+----------------+
| Name           | Key            | Required       | Type           | Description    |
+================+================+================+================+================+
| IPv4 address   | ipv4           | True           | string         | IPv4 address   |
|                |                |                |                | you want to    |
|                |                |                |                | enrich.        |
+----------------+----------------+----------------+----------------+----------------+

#### Returns {#returns}

+--------------------+--------------------+--------------------+--------------------+
| Name               | Path               | Type               | Description        |
+====================+====================+====================+====================+
|                    |                    | array of object    |                    |
+--------------------+--------------------+--------------------+--------------------+
| count              | count              | integer            | The sinkhole       |
|                    |                    |                    | count.             |
+--------------------+--------------------+--------------------+--------------------+
| country\_name      | country\_name      | string             | The country of the |
|                    |                    |                    | ip.                |
+--------------------+--------------------+--------------------+--------------------+
| data\_port         | data\_port         | integer            | The data port.     |
+--------------------+--------------------+--------------------+--------------------+
| datetime           | datetime           | string             | The first seen     |
|                    |                    |                    | date of the        |
|                    |                    |                    | sinkhole.          |
+--------------------+--------------------+--------------------+--------------------+
| ipv4               | ipv4               | string             | The ipv4 of the    |
|                    |                    |                    | sinkhole.          |
+--------------------+--------------------+--------------------+--------------------+
| last\_seen         | last\_seen         | string             | The last seen date |
|                    |                    |                    | of the sinkhole.   |
+--------------------+--------------------+--------------------+--------------------+
| organization\_name | organization\_name | string             | The isp            |
|                    |                    |                    | organization for   |
|                    |                    |                    | the ip.            |
+--------------------+--------------------+--------------------+--------------------+
| sink\_source       | sink\_source       | string             | The ipv4 of the    |
|                    |                    |                    | sink source.       |
+--------------------+--------------------+--------------------+--------------------+

### Retrieve SSL certificate information for IP address

Operation ID:
:   SSL\_CERTIFICATE

Retrieve SSL certificate enrichment data for IP address.

#### Parameters {#required-parameters}

+----------------+----------------+----------------+----------------+----------------+
| Name           | Key            | Required       | Type           | Description    |
+================+================+================+================+================+
| IPv4 address   | ip             | True           | string         | IPv4 address   |
|                |                |                |                | you want to    |
|                |                |                |                | enrich.        |
+----------------+----------------+----------------+----------------+----------------+

#### Returns {#returns}

+--------------------+--------------------+--------------------+--------------------+
| Name               | Path               | Type               | Description        |
+====================+====================+====================+====================+
| related\_count     | related\_count     | integer            | The number of ip   |
|                    |                    |                    | addresses          |
|                    |                    |                    | connected to this  |
|                    |                    |                    | certificate.       |
+--------------------+--------------------+--------------------+--------------------+
| ssl\_certs         | ssl\_certs         | array of object    | The ssl\_certs     |
|                    |                    |                    | object.            |
+--------------------+--------------------+--------------------+--------------------+
| ip                 | ssl\_certs.ip      | string             | The ip address     |
|                    |                    |                    | associated with    |
|                    |                    |                    | certificate.       |
+--------------------+--------------------+--------------------+--------------------+
| cert\_key          | ssl\_certs.ssl\_ce | string             | The certificate    |
|                    | rt.cert\_key       |                    | key (sha1).        |
+--------------------+--------------------+--------------------+--------------------+
| expire\_date       | ssl\_certs.ssl\_ce | string             | The expiry date of |
|                    | rt.expire\_date    |                    | the certificate.   |
+--------------------+--------------------+--------------------+--------------------+
| issue\_date        | ssl\_certs.ssl\_ce | string             | The issue date of  |
|                    | rt.issue\_date     |                    | the certificate.   |
+--------------------+--------------------+--------------------+--------------------+
| issuer\_commonName | ssl\_certs.ssl\_ce | string             | The common name    |
|                    | rt.issuer\_commonN |                    | that the           |
|                    | ame                |                    | certificate was    |
|                    |                    |                    | issued from.       |
+--------------------+--------------------+--------------------+--------------------+
| issuer\_countryNam | ssl\_certs.ssl\_ce | string             | The country ISO    |
| e                  | rt.issuer\_country |                    | the certificate    |
|                    | Name               |                    | was issued from.   |
+--------------------+--------------------+--------------------+--------------------+
| issuer\_localityNa | ssl\_certs.ssl\_ce | string             | The city where the |
| me                 | rt.issuer\_localit |                    | issuer company is  |
|                    | yName              |                    | legally located.   |
+--------------------+--------------------+--------------------+--------------------+
| issuer\_organizati | ssl\_certs.ssl\_ce | string             | The organization   |
| onName             | rt.issuer\_organiz |                    | name that issued   |
|                    | ationName          |                    | the certificate.   |
+--------------------+--------------------+--------------------+--------------------+
| issuer\_organizati | ssl\_certs.ssl\_ce | string             | The organization   |
| onalUnitName       | rt.issuer\_organiz |                    | unit name that     |
|                    | ationalUnitName    |                    | issued the         |
|                    |                    |                    | certificate.       |
+--------------------+--------------------+--------------------+--------------------+
| issuer\_stateOrPro | ssl\_certs.ssl\_ce | string             | The issuer state   |
| vinceName          | rt.issuer\_stateOr |                    | or province.       |
|                    | ProvinceName       |                    |                    |
+--------------------+--------------------+--------------------+--------------------+
| md5                | ssl\_certs.ssl\_ce | string             | The certificate    |
|                    | rt.md5             |                    | MD5.               |
+--------------------+--------------------+--------------------+--------------------+
| serial\_number     | ssl\_certs.ssl\_ce | float              | The certificate    |
|                    | rt.serial\_number  |                    | serial number.     |
+--------------------+--------------------+--------------------+--------------------+
| sha1               | ssl\_certs.ssl\_ce | string             | The certificate    |
|                    | rt.sha1            |                    | sha1.              |
+--------------------+--------------------+--------------------+--------------------+
| sha\_256           | ssl\_certs.ssl\_ce | string             | The certificate    |
|                    | rt.sha\_256        |                    | sha256.            |
+--------------------+--------------------+--------------------+--------------------+
| sig\_algo          | ssl\_certs.ssl\_ce | string             | The certificate    |
|                    | rt.sig\_algo       |                    | signature          |
|                    |                    |                    | algorithm.         |
+--------------------+--------------------+--------------------+--------------------+
| signature          | ssl\_certs.ssl\_ce | array of string    | Signature split    |
|                    | rt.signature       |                    | into multiple      |
|                    |                    |                    | lines.             |
+--------------------+--------------------+--------------------+--------------------+
| ssl\_version       | ssl\_certs.ssl\_ce | integer            | The SSL version.   |
|                    | rt.ssl\_version    |                    |                    |
+--------------------+--------------------+--------------------+--------------------+
| subject\_commonNam | ssl\_certs.ssl\_ce | string             | The subject name   |
| e                  | rt.subject\_common |                    | that the           |
|                    | Name               |                    | certificate was    |
|                    |                    |                    | issued to.         |
+--------------------+--------------------+--------------------+--------------------+
| subject\_countryNa | ssl\_certs.ssl\_ce | string             | The country the    |
| me                 | rt.subject\_countr |                    | certificate was    |
|                    | yName              |                    | issued to.         |
+--------------------+--------------------+--------------------+--------------------+
| subject\_localityN | ssl\_certs.ssl\_ce | string             | The city where the |
| ame                | rt.subject\_locali |                    | subject company is |
|                    | tyName             |                    | legally located.   |
+--------------------+--------------------+--------------------+--------------------+
| subject\_organizat | ssl\_certs.ssl\_ce | string             | The organization   |
| ionName            | rt.subject\_organi |                    | name that recieved |
|                    | zationName         |                    | the certificate.   |
+--------------------+--------------------+--------------------+--------------------+
| subject\_organizat | ssl\_certs.ssl\_ce | string             | The organization   |
| ionalUnitName      | rt.subject\_organi |                    | unit name that     |
|                    | zationalUnitName   |                    | recieved the       |
|                    |                    |                    | certificate.       |
+--------------------+--------------------+--------------------+--------------------+
| subject\_stateOrPr | ssl\_certs.ssl\_ce | string             | The state or       |
| ovinceName         | rt.subject\_stateO |                    | province name      |
|                    | rProvinceName      |                    | where the subject  |
|                    |                    |                    | company is         |
|                    |                    |                    | located.           |
+--------------------+--------------------+--------------------+--------------------+
| timestamp          | ssl\_certs.ssl\_ce | string             | The certificate    |
|                    | rt.timestamp       |                    | date and time.     |
+--------------------+--------------------+--------------------+--------------------+

### Is this page helpful? {.has-text-weight-semibold .has-margin-top-none .has-margin-bottom-small}

Yes

No

Any additional feedback?

Skip

Submit

Thank you.

Feedback {#feedback .title .is-3 .has-margin-top-large}
--------

Submit and view feedback for

[This
product](https://docs.microsoft.com/connectors/custom-connectors/provide-feedback)
This page

[View all page
feedback](https://github.com/MicrosoftDocs/BusinessApplicationPlatform-Connectors-public/issues)

[](#)

Theme

-   Light
-   Dark
-   High contrast

-   -   [Previous Version
    Docs](https://docs.microsoft.com/en-us/previous-versions/)
-   [Blog](https://docs.microsoft.com/en-us/teamblog)
-   [Contribute](https://docs.microsoft.com/en-us/contribute)
-   [Privacy & Cookies](https://go.microsoft.com/fwlink/?LinkId=521839)
-   [Terms of Use](https://docs.microsoft.com/en-us/legal/termsofuse)
-   [Site Feedback](https://aka.ms/sitefeedback)
-   [Trademarks](https://www.microsoft.com/en-us/legal/intellectualproperty/Trademarks/EN-US.aspx)
-   © Microsoft 2020

### Is this page helpful? {.has-text-weight-semibold .has-margin-top-none .has-margin-bottom-small}

Yes

No

Any additional feedback?

Skip

Submit

Thank you.

### In this article

[](#)

Theme

-   Light
-   Dark
-   High contrast

-   -   [Previous Version
    Docs](https://docs.microsoft.com/en-us/previous-versions/)
-   [Blog](https://docs.microsoft.com/en-us/teamblog)
-   [Contribute](https://docs.microsoft.com/en-us/contribute)
-   [Privacy & Cookies](https://go.microsoft.com/fwlink/?LinkId=521839)
-   [Terms of Use](https://docs.microsoft.com/en-us/legal/termsofuse)
-   [Site Feedback](https://aka.ms/sitefeedback)
-   [Trademarks](https://www.microsoft.com/en-us/legal/intellectualproperty/Trademarks/EN-US.aspx)
-   © Microsoft 2020

