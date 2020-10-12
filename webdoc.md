# Farsight Security

![Farsight](https://www.farsightsecurity.com/assets/media/svg/farsight-logo.svg "Farsight")

Farsight integration to Microsoft Azure Sentinel provides direct, high volume access to Passive DNS data. It enables investigators and analysts to understand and defend against cyber adversaries and their infrastructure.

<br>

 This connector is available in the following products and regions:

 | Service | Class | Regions |
 | ------ | ------ | ------ |
 | Logic Apps | Standard | All [Logic Apps regions](https://azure.microsoft.com/en-us/global-infrastructure/services/?products=logic-apps&regions=all) except the following:<br>-Azure Government regions<br>-Azure China regions |
 | Power Automate | Premium | All [Power Automate regions](https://docs.microsoft.com/en-us/power-automate/regions-overview) except the following:<br>-US Government (GCC)<br>-US Government (GCC High)<br>-China Cloud operated by 21Vianet |
 | Power Apps | Premium | All [Power Apps regions](https://docs.microsoft.com/en-us/power-platform/admin/regions-overview#what-regions-are-available) except the following:<br>-US Government (GCC)<br>-US Government (GCC High)<br>-China Cloud operated by 21Vianet |

<br>

## Pre-requisites
You will need the following to proceed:
* A Microsoft Power Apps or Power Automate plan with custom connector feature
* An Azure subscription
* Farsight API Key

<br>

## Support and documentation: 
For all the support requests and general queries you can contact support@farsightsecurity.com or visit [contact-us](https://www.farsightsecurity.com/about-farsight-security/contacts/)

<br>

## Creating a connection
To connect your account, you will need the following information:

| Name | Type | Description
 | ------ | ------ | ------ |
 | X-API-Key | securestring | The X-API-Key for DNSDB API |
  
<br>

 ## Throttling Limits
 | Name | Calls | Renewal Period
 | ------ | ------ | ------ |
 | API calls per connection | 1000 | 1 Second |
 
<br>

  
 ## Actions:
 | Action Name | Description
  | ------ | ------ |
  | [Retrieve Passive DNS Information for Domain](#retrieve-passive-dns-information-for-domain) |  Retrieve on demand Passive DNS enrichment data for Domain |

<br>

### Retrieve Passive DNS Information for Domain

Operation ID: DOMAIN_PASSIVE_DNS

Retrieve on demand Passive DNS enrichment data for Domain

#### Parameters

 | Name | Key | Required | Type | Description
 | ------ | ------ | ------ | ------ | ------ |
 | Domain | domain | True  | string | Domain you want to enrich |


#### Returns
##### **Body** : [PassiveDNSResults](#passivednsresults)

<br>



### PassiveDNSResults

| Name | Path | Type | Description
| ------ | ------ | ------ | ------ |
| cert_name | cert_name | string | The certificate provider name |
|count | count | number | The passive dns count |
|domain| domain | string | The domain of the passive dns information requested |
|first_seen | first_seen | string | The first time this domain was seen | 
|city_name | ip.geo.city_name | string | City of the ip organization |
|country_iso_code | ip.geo.country_iso_code | string | Country ISO code of the ip organization |
|country_name | ip.geo.country_name | string | Country name of the ip organization |
|location_latitude | ip.geo.location_latitude | string | The latitude of the ip organization |
|location_longitude | ip.geo.location_longitude | string | The longitude of the ip organization |
|postal_code | ip.geo.postal_code | string | The postal code of the ip organization |
|ip | ip.ip | string | IP of the organization |
|autonomous_system_number | ip.isp.autonomous_system_number | string | The ASN of the ip |
|autonomous_system_organization | ip.isp.autonomous_system_organization | string | The ASO of the ip |
|ip_address | ip.isp.ip_address | string | The IP |
|isp | ip.isp.isp | string | The Internet Service Provider |
|organization | ip.isp.organization | string | The ISP organization |
|ipv4 | ipv4 | string | The ipv4 address of the passive dns record |
|ipv6 | ipv6 | string | The ipv6 address of the passive dns record |
|last_seen | last_seen | string | The last time this domain was seen |
|sha1 | sha1 | string | The sha1 Information |
|sources | sources | string array | A list of pDNS providers which the data came from |

<br>
