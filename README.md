# Cisco ISE  

**Web Resources**

* [Cisco ISE resources](https://cs.co/ise/ise-resources) - ISE Resources on Cisco's site  
* [ISE Getting Started page](https://www.cisco.com/c/m/en_us/products/security/identity-services-engine/getting-started.html) - Every resouce needed to deploy ISE!
* [Cisco Identity Services Engine (ISE) Set Up](https://cs.co/ise-cx)  
* [Cisco ISE 3rd party RADIUS Dictinaries](https://cs.co/ise/ise-resources#DeviceAdmin) - Dictionaries for 3rd party RADIUS servers
* [Cisco ISE community](https://cs.co/ise/ise-community) - The Cisco ISE Community Homepage
* [Cisco ISE Webinars](https://cs.co/ise-webinars) - Upcoming and Recorded Webinars & Training Videos  
* [Cisco ISE Youtube Channel](https://cs.co/ise-videos) - ISE YouTube Channel  
* [Cisco ISE Product Information](https://cisco.com/go/ise) - Cisco Identity Services Engine (ISE) homepage  
* [On-Demand Library Guest talks](https://www.ciscolive.com/global/on-demand-library.html?search=BRKEWN-2014#) - ISE videos for Cisco Live Events  
* [ISE Portal Builder](https://isepb.cisco.com) - An online portal builder for ISE
* [ISE Performance Scaling](https://cs.co/ise-perf-scale) - Performance and Scalability Guide for Cisco Identity Services Engine
* [Cisco ISE Guest & Web Authentication](https:/cs.co/ise-guest) - Landing page for all things guest related  
* [ISE Security Ecosystem Integration Guides](https://www.cisco.com/c/en/us/support/docs/security/identity-services-engine/216120-ise-security-ecosystem-integration-guide.html)  
* [ISE Compatibility Guides](https://cs.co/ise-compatibility) 
* [ISE Design and Integration Guides](https://ise-guides) 
* [ISE Licensiing Guide](https://co.cs/ise-licensing)  
* [Free 90 day ISE Evaluations](https://cs.co/ise-eval)  
* [ISE End of Life Notices](cs.co/ise-eol)  
* [ISE NAC Forum](https://cs.co/nac-community)  

  


## What Supports ISE Guest Access
Platforms  
* AireOS  
* Switching  
* IOS-XE  
* Meraki  

### References
* [ISE Guest Access Prescriptive Deployment Guide](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjup9aJjd77AhWpKUQIHXjQD6AQFnoECB8QAQ&url=https%3A%2F%2Fcommunity.cisco.com%2Ft5%2Fsecurity-knowledge-base%2Fise-guest-access-prescriptive-deployment-guide%2Fta-p%2F3640475&usg=AOvVaw0W3mdwqvYany36BhBGt0e5)  
* [How To: Integrate Meraki Networks with ISE](https://community.cisco.com/t5/security-knowledge-base/how-to-integrate-meraki-networks-with-ise/ta-p/3618650)  
* [ISE and Catalyst 9800 Series Integration Guide](https://community.cisco.com/t5/security-knowledge-base/ise-and-catalyst-9800-series-integration-guide/ta-p/3753060)  
* [Does ISE Support My Network Access Device?](https://community.cisco.com/t5/security-knowledge-base/does-ise-support-my-network-access-device/ta-p/3650231)  
* 

### Guest Portal Scaling
* Up to ~100 concurrent logins/web page requests per second per psn
* 600 portals maximum
* Supports [location based portals](ISE and Location-Based Web Authentication Portals)  

## New Features
[ISE Guest & Web Authentication](cs.co/ise-guest)  
* Guest - Auto Login on Sponsor Approval  
* Guest - Phone Number as a User ID with number validation  
* Guest - Password Recovery  
* Guest - Grace Access for sponsor approval. Up to 30 minute access BEFORE sponsor approves.  
* Secure SMTP Support  




## Profiling
Under Settings, Profiling,  
You can run NMAP scans from the profiling service
[NMAP](https://www.cisco.com/c/en/us/td/docs/security/ise/2-4/admin_guide/b_ISE_admin_guide_24/m_cisco_ise_endpoint_profiling_policies.html#concept_57A4A7ADE3DA429A821900C5CBEA8BF0)  

for NMAP, comma separated of subnets or IPs. 

Field will be cleared on successful, saved change

## PxGrid
* AMP - Advanced Malware Protection
* ANC - Adaptive Network Control (replacement for EPS)
* CTA - Cisco Threat Analytics
* iDP - identity Provider Okta for example. 
* RTC - Rapid Threat Containment
* SGT - Scalable (Security) Group Tag
*  VA - Vulnerability Assessment (Qualys)
* WSA - Cisco Web Security Appliance - Context based Web Filtering


### Authentcation  
* [Self Signed pxGrid Client and pxGrid ISE Node certificates](https://communities.cisco.com/docs/DOC-68286)  
* [CA Signed pxGrid Client and pxGrid ISE Node certificates](https://communities.cisco.com/docs/DOC-68287)  

### Develop PxGrid apps  
pxGrid is based on the ieee XMPP protocol. You can develop your own in house applications using the developer tools.  
[Developer tools](https://developer.cisco.com/site/pxgrid)  

ISE & Infoblox - Use Adaptive Network Contro (ANC) to share info with Infoblox  
ISE & Checkpoint - Use ISE identity/device & TrustSec context  
	* Firewall  
	* Application control  
	* DLP  
	* URL Filtering  
	* antivirus  
ISE & Stealthwatch - provides context to Stealwatch using pxGrid API. Not an automated response. 
ISE & Splunk - uses syslog to provide contextual threat mitigation  


### Threat Detection  
* Industry Time to Detection (TTD) 100 - 200 days.  

**Rapid Threat Containment Overview**  
* Context Exchange (pxGrid / API / Syslog )
* ANC/EPS Mitigation - pxGrid gets policy from subscriber
* Threat Centric NAC - ISE has the policy, gets data from subscriber

**EPS / ANC Mitigation actions**
* Apply ANC with pxGrid reduce TTD to minutes not 100 days.  
* Automated Respnse  
* Deeper Analysis  
* Sensors - AMP / NGIPS / ASA w Firepower  


**Threat Centric NAC**  
 Requires ISE Apex License. Runs on PSN.  
 Collect contextual information and then make a descision.
 
 **Supported Products**  
 * Tenable  
 * Qualys  
 * Cisco Threat Analytics  
 * Rapid7  
 * Cisco AMP
 
**What does it do?**  
* Creates ISE authorization policies based on threat and vulnerability attributes.  
* Use some solution to detect that an endpoint is vulnerable. Let ISE know of the vulnerabilty. Rapid7, Cisco AMP, Qualys, etc. for detecting vulnerabilities.
* Will show comprimised and vulnerable endpoints in ISE  


### References
* [Notes on Okta as SAML IdP](https://community.cisco.com/t5/security-knowledge-base/notes-on-okta-as-saml-idp/ta-p/3644284) 

    


## ISE and Software Defined Access
In SDA it server two broad features:
* User/Device authentication
* Imposing Security Group Tags and enforcement policies (SGACLs)

[TrustSec Troubleshooting Guide](https://community.cisco.com/t5/secuirity-documents/trustsec-troubleshooting-guide/ta-p/3647576/#live_content_id_Counters_on_the_3850_and_3650)

### DNA Center
DNA Center (DNAC) uses pxGrid to integrate with ISE. DNSC is a subscriber.  
   
**Licensing**
* ISE Base
* ISE Plus

**Requires External RESTful Services (ERS) on ISE**
Go to "administration, System, settings, ERS Settings"
* ERS Setting for Primary administration Node - Enable ERS for Read/Write  
* ERS SEttings for All Other Nodes - Enable ERS for Read  

Go to "administration, System, Deployment"  
* Enable pxGrid  

Go to "administration, pxGrid Serivces"
* Verify that pxGrid show connected at the bottom  

### Using Postman to fetch ERS response from ISE to verify Operation  

[Get Postman](https://www.getpostman.com/apps)  

Instructions for seting up postman to invoke ERS:  

[ISE ERS API Examples](https://community.cisco.com/t5/security-documents/ise-ers-api-examples/ta-p/3622623#toc-hld--634300009)

**Certificate requirements between ISE/DNAC**  
[Cisco PKI](https://www.cisco.com/security/pki)  

### Using Kibana in DNAC for viewing logs

On the right side of the DNAC system360 page select Tools, Log Explorer. Kibana will open, then enter the following into the search field.  
```
kubernetes.labels.serviceName:
network-design-service OR kubernets.labels.serviceName:idenitity-mamager-pxgrid-service
```


### Troubleshooting logs from DNAC cli
Use these commands to display pxGrid and Network-Design Logs from the DNAC cli:  

* $ magctl service logs -rf network-design  
	tails the netowork-desing logs  
* $ magctl service logs -rf pxgrid  
	tails the pxGrid logs  
* $ magctl service logs -rf -t 500 network-design  
	Shows last 500 lines of the network-design logs  
* $ magctl service logs -rf -t 500 pxgrid  
	Shows last 500 lines of the pxGrid logs  

### Troubleshooting DNAC Certificate is in ISE Trust store

Go to Administration, System, Certificates, Trusted Certificates
* Verify that the DNAC certificate is listed and enabled.

Enable logs on primary admin node and pxgrid node
Go to Administration, System, Logging, Debug Log Configuration  
* REST API: ERS (Debug)  
* Certificate Exchange Process: Infrastructure )Debug)  
* Cerficates -admin-ca (Debug) and ca-service (Debug)  
* PxGrid Communication -pxgrid (Trace)  

Go to Operatons, Torubleshoot, Download logs
* ise-psc.log

### ISE Password Expires
* THe intergration goes offline since the ERS calls start to fail
* One of the fixes being put in placec is to have a cerificate based authentication on TCP port 9062. Please make sure port 9062 is reachable from DNAC.
* THe work around for now is to go into DNAC > System Settings > Check the Radio Button for ISE > Edit. Update the password and apply.

NOTE: Make sure the ISE CLI and GUI passwords are the same!

### Admin Certificate is Changed on ISE
In order to download the new certificates from ISE, we need to initiate the update workflow usiing the below process:
* DNAC > Sytem Settings > Settings > Check the Radio button for ISE > edit. Input the ISE password and apply.

### SASL Handshake failure inevent of pxgrid certificate change  
Got to ISE Administration, pxGrid Services, All Clients  
* Delete the dna-sub  
* restart the pxgrid service from DNAC  
	magctl service restart pxgrid  


## Context Visibility  
ISE gathers context from devices.   
* Who  
* WHat  
* When 
* Where  
* How  
* Application  
* Threat  
* Vulnerability  

Context is used to populate scalable groups to be used for segmentation.  

Data is communitcated using:  
* pxGrid  
* REST API  
* Syslog  

between ISE and:  
* DNA Center  
* StealthWatch  
* FirepowerServices  
* + 3rd party like Checkpoint, Rapid7, Qualys, etc.  


## Device Visibility with Profiling  

Endpoints send interesting data, that reveal their device identitiy. Need to subscribe to the profiling feed service to get updates from Cisco.  

## ISE Data Collection Methonds  

**Discovery protocols**  
* Netflow  
* DHCP  
* DNS  
* HTTP  
* RADIUS  
* NMAP  
* SNMP  
* AD  

**Device Sensors**  
* CDP
* LLDP  
* DHCP  
* HTTP  
* H323  
* SIP  
* MDNS  

**Anyconnect**  
* ACIDEX  

### Probe Best Practices

* Turn on RADIUS Accounting  
* Do not turn on SNMP traps  
* Use AD - A high fidelity probe for OS, Service Pack and Version  
* Lerverage HTTP probe fro gathering OS specific or Platform information in Mobile Devices and Laptops  
* With Anyconnect, use ACIDEX to gather hardware, Software information.  

[ISE Profiling Design Guide](https://community.cisco.com/t5/security-knowledge-base/ise-profiling-design-guide/ta-p/3739456)  

### Integration with Eco-System Partners  
Platform Exchange Grid (pxGrid)  

Publisher/Subscriber model  

Cisco ISE - Publisher and Subscriber
Eco-Partner - Publisher and Subscriber

**Cisco Indusrial Network Director - IND**  
* Industrial Protocol support for automation asset discovery  
* Security platform integration to proect the industrial network  
* Plug and play server for zero touch switch commissioning  
* Comprehensive network monitoring and lifecycle management  

**Protocols**    
* CIP  
* Profinet  
* Modbus  
* OPC Unified Architecture (OPC-UA)  
* BACnet  
* Siemens S7  
* Others  

[Cisco Industrial Network Director](https://www.cisco.com/go/ind)  

IND uses pxGrid 2.0 - Web sockets over STOMP

**Best Practices**  
* Probes on (2) PSNs for HA  
* Each PSN becomes a pxGrid subsciber to the Endpoint Profile MetaData Topic.  
* Requires RADIUS probefor MAC to IP Binding  


* [Deploying Cisco Industrial Network Director (IND) with Cisco ISE using pxGrid](https://www.cisco.com/c/dam/en/us/td/docs/switches/ind/install/IND_PxGrid_Registration_Guide_Final.pdf)  
* [IOT Eco-system Partners](https://marketplace.cisco.com/catalog)  
* [Custom Profiles](https://community.cisco.com/t5/security-documents/ise-endpoints-profiles/ta-p/3641187)
* [Custom Profiles 1](https://community.cisco.com/t5/security-documents/ise-endpoints-profiles/ta-p/3948463)
* [Device Visibility using MUD](https://datatracker.ietf.org/doc/rfc8520)  
* 


## Reducing Unknowns  
**Option 1** Device Registration Portal  

* Endpoint group - Up to 999 devices  
* 600 portals Supported  
* Admin/User can register device  
* Can use a custom portal on an external server E.I Medical Device Registation Portal.
* Custom Portal uses REST API to communicate
* 

**Option 2**  
* Add Endpoints using File, LDAP, and REST API
* 10,000 devices per import
* No restrictions on Identity Group, Profile, Custom Attribures, etc.

## Viewing Endpoints
For unknown devices
Context Visibility, Endpoints, Endpoint classification  
Use the "Endpoint Profile" filter with "Unknown"  

**Option 3** 
* Create a custom Profile
  

**ISE End Point Analysis Tool (EAT)**  
* Profile Creation and Management - Options to create & share  profiles created by EAT  
* Create, Open, and Customize reports  
* Purge/Delete - Remove data locally stored on teh client desktop  
* Export CSV Report  
* [Download the EAT](https://iseeat.cisco.com) - Account creation required!  

**Review - How to profile Unknown Endpoints**  
* Whitelist (adding MAC addresses to Endpoint Groups)  
* Register the devices using Context visibilyt UI  
* Import the Endpoints - CSV, LDAP, REST API  
* Use Device Registration Portal  
* Custom Profiles  


## Profiling Enhancments  
Impact of Endpoint PRofiling Ownership Changes
Device moves on the network, you end up with ownership contention.  

**What are we solving (ISE 2.7+)**  
Multiple PSNs receive endpoint information from teh network causing endpoint onwership changes leading to contention.  

**How**  
* PSN becomes an owner and announces ownesip to other PSNs. Probe updates are received from PSNs using secure APIs.  
* Using RabbitMQ that enhances reliability and scale (10K to 200K)  
* Block profile cahnges for manually updated endponts.  

Both are enabled by default!  

Stopped at lesson 5 of visiblity and Profiling











[Compatible ISE Vesions](https://www.cisco.com/c/en/us/td/docs/cloud-systems-management/network-automation-and-management/dna-center/1-2/install/b_dnac_install_1_2/b_dnac_install_1_2_chapter_0101.html?bookSearch=true#reference_wtq_lkk_tdb)











