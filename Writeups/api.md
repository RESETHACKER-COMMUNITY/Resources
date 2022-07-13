![FW_LgLZXwAIZYF1](https://user-images.githubusercontent.com/25515871/177757917-a1691979-a1ae-4c68-b02a-b5c69ac098e5.jpg)

# [What is an API?]
[Credit - Katie Paxton](https://twitter.com/@InsiderPhD)
     
    
   **Tl;dr**
   
                - Software designed to talk to other software
                - But still has to allow humans to debug it
                - Usually outputs some structured plain text e.g. JSON or XML
                - JSON {"key" : "value" ...}
                - XML <object><key>value</key>...

     
  **Types of APIs (what kinds of APIs are out there>?**
     
               - External APIs APIs are designed to be public but are designed for use by a single org
               - Public APIs for developers to add integration from their app to an existing service
               - Internal APIs completely inaccessible from outside an organisation, may be aggregated to an external API

  **API use cases**
       
               - Single interface, many devices
               - Many tools allow APIs to be automatically created from a database or framework
               - Language independent even if you change later an API will always work

  **API terminology**
      
               - Endpoint - a URL which does something e.g. doesn't 404
               - Parameter - the data you input into an API
               - API call - when an app makes a request to the API it is calling it
               - Stateless - the server doesn't know anything about the client's state we need to tell it each time
               - API keys - provides authentication to APIs - when you log in you are given an API key which you send with all future requests
               - CORS - stands for cross-origin resource sharing, can an API endpoint be accessed from another domain?
 
  **RESTful APIs**
      
               - API standard for the web enforced consistency. between APIs based on CRUD and the URL
               - Create a new resource -> POST /api/resource
               - Read an existing resource -> GET /api/resource/1
               - Read all resources -> GET /api/resource/
               - Update a resource -> PUT /api/resource/1
               - Delete a resource -> DELEETE /api/resource/1
               - Very few APIs enforce true RESTful APIs so the term usually refers to APIs with this structure

  **Resources can be anything**
      
               - Depends on the business logic
               - Forum: posts, users, replies
               - Twitter: tweers, users, bookmarks
               - Twitter and forums are similar but endpoints will be custom + use different terminology
               

## Check out the meantioned list of website(in free/trail API section) for OSINT. 
[Incase want to automates OSINT for threat intelligence and mapping your attack surface. ](https://github.com/smicallef/spiderfoot)

  | Use cases  | Descriptions | purpose   |
|:---------| :-----------|:-------|
Account Finder|Look for possible associated accounts on nearly 200 websites like Ebay, Slashdot, reddit, etc.|Internal
Base64 Decoder|Identify Base64-encoded strings in URLs, often revealing interesting hidden information.|Internal
Binary String Extractor|Attempt to identify strings in binary content.|Internal
Bitcoin Finder|Identify bitcoin addresses in scraped webpages.|Internal
Company Name Extractor|Identify company names in any obtained data.|Internal
Cookie Extractor|Extract Cookies from HTTP headers.|Internal
Country Name Extractor|Identify country names in any obtained data.|Internal
Credit Card Number Extractor|Identify Credit Card Numbers in any data|Internal
Cross-Referencer|Identify whether other domains are associated ('Affiliates') of the target by looking for links back to the target site(s).|Internal
Custom Threat Feed|Check if a host/domain, netblock, ASN or IP is malicious according to your custom feed.|Internal
DNS Brute-forcer|Attempts to identify hostnames through brute-forcing common names and iterations.|Internal
DNS Common SRV|Attempts to identify hostnames through brute-forcing common DNS SRV records.|Internal
DNS Look-aside|Attempt to reverse-resolve the IP addresses next to your target to see if they are related.|Internal
DNS Raw Records|Retrieves raw DNS records such as MX, TXT and others.|Internal
DNS Resolver|Resolves hosts and IP addresses identified, also extracted from raw content.|Internal
DNS Zone Transfer|Attempts to perform a full DNS zone transfer.|Internal
E-Mail Address Extractor|Identify e-mail addresses in any obtained data.|Internal
Error String Extractor|Identify common error messages in content like SQL errors, etc.|Internal
Ethereum Address Extractor|Identify ethereum addresses in scraped webpages.|Internal
File Metadata Extractor|Extracts meta data from documents and images.|Internal
Hash Extractor|Identify MD5 and SHA hashes in web content, files and more.|Internal
Hosting Provider Identifier|Find out if any IP addresses identified fall within known 3rd party hosting ranges, e.g. Amazon, Azure, etc.|Internal
Human Name Extractor|Attempt to identify human names in fetched content.|Internal
IBAN Number Extractor|Identify International Bank Account Numbers (IBANs) in any data.|Internal
Interesting File Finder|Identifies potential files of interest, e.g. office documents, zip files.|Internal
Junk File Finder|Looks for old/temporary and other similar files.|Internal
Page Information|Obtain information about web pages (do they take passwords, do they contain forms, etc.)|Internal
PGP Key Servers|Look up e-mail addresses in PGP public key servers.|Internal
Phone Number Extractor|Identify phone numbers in scraped webpages.|Internal
Port Scanner - TCP|Scans for commonly open TCP ports on Internet-facing systems.|Internal
Similar Domain Finder|Search various sources to identify similar looking domain names, for instance squatted domains.|Internal
Social Network Identifier|Identify presence on social media networks such as LinkedIn, Twitter and others.|Internal
SSL Certificate Analyzer|Gather information about SSL certificates used by the target's HTTPS sites.|Internal
Strange Header Identifier|Obtain non-standard HTTP headers returned by web servers.|Internal
Subdomain Takeover Checker|Check if affiliated subdomains are vulnerable to takeover.|Internal
TLD Searcher|Search all Internet TLDs for domains with the same name as the target (this can be very slow.)|Internal
Web Analytics Extractor|Identify web analytics IDs in scraped webpages and DNS TXT records.|Internal
Web Framework Identifier|Identify the usage of popular web frameworks like jQuery, YUI and others.|Internal
Web Server Identifier|Obtain web server banners to identify versions of web servers being used.|Internal
Web Spider|Spidering of web-pages to extract content for searching.|Internal
Whois|Perform a WHOIS look-up on domain names and owned netblocks.|Internal

# Get a free/trail API to intergrate with Recon/OSINT tools & modules.   
[Credit -  Steve Micallef](https://github.com/smicallef/spiderfoot))
               
  | Use cases    | Description | API   |
|:---------| :-----------|:-------|
[AbstractAPI](https://app.abstractapi.com/)|Look up domain, phone and IP address information from AbstractAPI.|Tiered API
[abuse.ch](https://www.abuse.ch)|Check if a host/domain, IP address or netblock is malicious according to Abuse.ch.|Free API
[AbuseIPDB](https://www.abuseipdb.com)|Check if an IP address is malicious according to AbuseIPDB.com blacklist.|Tiered API
[Abusix Mail Intelligence](https://abusix.org/)|Check if a netblock or IP address is in the Abusix Mail Intelligence blacklist.|Tiered API
Account Finder|Look for possible associated accounts on nearly 200 websites like Ebay, Slashdot, reddit, etc.|Internal
[AdBlock Check](https://adblockplus.org/)|Check if linked pages would be blocked by AdBlock Plus.|Tiered API
[AdGuard DNS](https://adguard.com/)|Check if a host would be blocked by AdGuard DNS.|Free API
[Ahmia](https://ahmia.fi/)|Search Tor 'Ahmia' search engine for mentions of the target.|Free API
[AlienVault IP Reputation](https://cybersecurity.att.com/)|Check if an IP or netblock is malicious according to the AlienVault IP Reputation database.|Free API
[AlienVault OTX](https://otx.alienvault.com/)|Obtain information from AlienVault Open Threat Exchange (OTX)|Tiered API
[Amazon S3 Bucket Finder](https://aws.amazon.com/s3/)|Search for potential Amazon S3 buckets associated with the target and attempt to list their contents.|Free API
[Apple iTunes](https://itunes.apple.com/)|Search Apple iTunes for mobile apps.|Free API
[Archive.org](https://archive.org/)|Identifies historic versions of interesting files/pages from the Wayback Machine.|Free API
[ARIN](https://www.arin.net/)|Queries ARIN registry for contact information.|Free API
[Azure Blob Finder](https://azure.microsoft.com/en-in/services/storage/blobs/)|Search for potential Azure blobs associated with the target and attempt to list their contents.|Free API
[Bad Packets](https://badpackets.net)|Obtain information about any malicious activities involving IP addresses found|Commercial API
Base64 Decoder|Identify Base64-encoded strings in URLs, often revealing interesting hidden information.|Internal
[BGPView](https://bgpview.io/)|Obtain network information from BGPView API.|Free API
Binary String Extractor|Attempt to identify strings in binary content.|Internal
[BinaryEdge](https://www.binaryedge.io/)|Obtain information from BinaryEdge.io Internet scanning systems, including breaches, vulnerabilities, torrents and passive DNS.|Tiered API
[Bing (Shared IPs)](https://www.bing.com/)|Search Bing for hosts sharing the same IP.|Tiered API
[Bing](https://www.bing.com/)|Obtain information from bing to identify sub-domains and links.|Tiered API
Bitcoin Finder|Identify bitcoin addresses in scraped webpages.|Internal
[Bitcoin Who's Who](https://bitcoinwhoswho.com/)|Check for Bitcoin addresses against the Bitcoin Who's Who database of suspect/malicious addresses.|Tiered API
[BitcoinAbuse](https://www.bitcoinabuse.com/)|Check Bitcoin addresses against the bitcoinabuse.com database of suspect/malicious addresses.|Free API
[Blockchain](https://www.blockchain.com/)|Queries blockchain.info to find the balance of identified bitcoin wallet addresses.|Free API
[blocklist.de](http://www.blocklist.de/en/index.html)|Check if a netblock or IP is malicious according to blocklist.de.|Free API
[BotScout](https://botscout.com/)|Searches BotScout.com's database of spam-bot IP addresses and e-mail addresses.|Tiered API
[botvrij.eu](https://botvrij.eu/)|Check if a domain is malicious according to botvrij.eu.|Free API
[BuiltWith](https://builtwith.com/)|Query BuiltWith.com's Domain API for information about your target's web technology stack, e-mail addresses and more.|Tiered API
[C99](https://api.c99.nl/)|Queries the C99 API which offers various data (geo location, proxy detection, phone lookup, etc).|Commercial API
[CallerName](http://callername.com/)|Lookup US phone number location and reputation information.|Free API
[Censys](https://censys.io/)|Obtain host information from Censys.io.|Tiered API
[Certificate Transparency](https://crt.sh/)|Gather hostnames from historical certificates in crt.sh.|Free API
[CertSpotter](https://sslmate.com/certspotter/)|Gather information about SSL certificates from SSLMate CertSpotter API.|Tiered API
[CINS Army List](https://cinsscore.com/)|Check if a netblock or IP address is malicious according to Collective Intelligence Network Security (CINS) Army list.|Free API
[CIRCL.LU](https://www.circl.lu/)|Obtain information from CIRCL.LU's Passive DNS and Passive SSL databases.|Free API
[CleanBrowsing.org](https://cleanbrowsing.org/)|Check if a host would be blocked by CleanBrowsing.org DNS content filters.|Free API
[CleanTalk Spam List](https://cleantalk.org)|Check if a netblock or IP address is on CleanTalk.org's spam IP list.|Free API
[Clearbit](https://clearbit.com/)|Check for names, addresses, domains and more based on lookups of e-mail addresses on clearbit.com.|Tiered API
[CloudFlare DNS](https://www.cloudflare.com/)|Check if a host would be blocked by CloudFlare DNS.|Free API
[CoinBlocker Lists](https://zerodot1.gitlab.io/CoinBlockerListsWeb/)|Check if a domain appears on CoinBlocker lists.|Free API
[CommonCrawl](http://commoncrawl.org/)|Searches for URLs found through CommonCrawl.org.|Free API
[Comodo Secure DNS](https://www.comodo.com/secure-dns/)|Check if a host would be blocked by Comodo Secure DNS.|Tiered API
Company Name Extractor|Identify company names in any obtained data.|Internal
Cookie Extractor|Extract Cookies from HTTP headers.|Internal
Country Name Extractor|Identify country names in any obtained data.|Internal
Credit Card Number Extractor|Identify Credit Card Numbers in any data|Internal
[Crobat API](https://sonar.omnisint.io/)|Search Crobat API for subdomains.|Free API
Cross-Referencer|Identify whether other domains are associated ('Affiliates') of the target by looking for links back to the target site(s).|Internal
[CRXcavator](https://crxcavator.io/)|Search CRXcavator for Chrome extensions.|Free API
Custom Threat Feed|Check if a host/domain, netblock, ASN or IP is malicious according to your custom feed.|Internal
[CyberCrime-Tracker.net](https://cybercrime-tracker.net/)|Check if a host/domain or IP address is malicious according to CyberCrime-Tracker.net.|Free API
[Darksearch](https://darksearch.io/)|Search the Darksearch.io Tor search engine for mentions of the target domain.|Free API
[Debounce](https://debounce.io/)|Check whether an email is disposable|Free API
[Dehashed](https://www.dehashed.com/)|Gather breach data from Dehashed API.|Commercial API
[Digital Ocean Space Finder](https://www.digitalocean.com/products/spaces/)|Search for potential Digital Ocean Spaces associated with the target and attempt to list their contents.|Free API
DNS Brute-forcer|Attempts to identify hostnames through brute-forcing common names and iterations.|Internal
DNS Common SRV|Attempts to identify hostnames through brute-forcing common DNS SRV records.|Internal
[DNS for Family](https://dnsforfamily.com/)|Check if a host would be blocked by DNS for Family.|Free API
DNS Look-aside|Attempt to reverse-resolve the IP addresses next to your target to see if they are related.|Internal
DNS Raw Records|Retrieves raw DNS records such as MX, TXT and others.|Internal
DNS Resolver|Resolves hosts and IP addresses identified, also extracted from raw content.|Internal
DNS Zone Transfer|Attempts to perform a full DNS zone transfer.|Internal
[DNSDB](https://www.farsightsecurity.com)|Query FarSight's DNSDB for historical and passive DNS data.|Tiered API
[DNSDumpster](https://dnsdumpster.com/)|Passive subdomain enumeration using HackerTarget's DNSDumpster|Free API
[DNSGrep](https://opendata.rapid7.com/)|Obtain Passive DNS information from Rapid7 Sonar Project using DNSGrep API.|Free API
[DroneBL](https://dronebl.org/)|Query the DroneBL database for open relays, open proxies, vulnerable servers, etc.|Free API
[DuckDuckGo](https://duckduckgo.com/)|Query DuckDuckGo's API for descriptive information about your target.|Free API
E-Mail Address Extractor|Identify e-mail addresses in any obtained data.|Internal
[EmailCrawlr](https://emailcrawlr.com/)|Search EmailCrawlr for email addresses and phone numbers associated with a domain.|Tiered API
[EmailFormat](https://www.email-format.com/)|Look up e-mail addresses on email-format.com.|Free API
[EmailRep](https://emailrep.io/)|Search EmailRep.io for email address reputation.|Tiered API
[Emerging Threats](https://rules.emergingthreats.net/)|Check if a netblock or IP address is malicious according to EmergingThreats.net.|Free API
Error String Extractor|Identify common error messages in content like SQL errors, etc.|Internal
Ethereum Address Extractor|Identify ethereum addresses in scraped webpages.|Internal
[Etherscan](https://etherscan.io)|Queries etherscan.io to find the balance of identified ethereum wallet addresses.|Free API
File Metadata Extractor|Extracts meta data from documents and images.|Internal
[Flickr](https://www.flickr.com/)|Search Flickr for domains, URLs and emails related to the specified domain.|Free API
[Focsec](https://focsec.com/)|Look up IP address information from Focsec.|Tiered API
[FortiGuard Antispam](https://www.fortiguard.com/)|Check if an IP address is malicious according to FortiGuard Antispam.|Free API
[Fraudguard](https://fraudguard.io/)|Obtain threat information from Fraudguard.io|Tiered API
[F-Secure Riddler.io](https://riddler.io/)|Obtain network information from F-Secure Riddler.io API.|Commercial API
[FullContact](https://www.fullcontact.com)|Gather domain and e-mail information from FullContact.com API.|Tiered API
[FullHunt](https://fullhunt.io/)|Identify domain attack surface using FullHunt API.|Tiered API
[Github](https://github.com/)|Identify associated public code repositories on Github.|Free API
[GLEIF](https://search.gleif.org/)|Look up company information from Global Legal Entity Identifier Foundation (GLEIF).|Tiered API
[Google Maps](https://cloud.google.com/maps-platform/)|Identifies potential physical addresses and latitude/longitude coordinates.|Tiered API
[Google Object Storage Finder](https://cloud.google.com/storage)|Search for potential Google Object Storage buckets associated with the target and attempt to list their contents.|Free API
[Google SafeBrowsing](https://developers.google.com/safe-browsing/v4/lookup-api)|Check if the URL is included on any of the Safe Browsing lists.|Free API
[Google](https://developers.google.com/custom-search)|Obtain information from the Google Custom Search API to identify sub-domains and links.|Tiered API
[Gravatar](https://secure.gravatar.com/)|Retrieve user information from Gravatar API.|Free API
[Grayhat Warfare](https://buckets.grayhatwarfare.com/)|Find bucket names matching the keyword extracted from a domain from Grayhat API.|Tiered API
[Greensnow](https://greensnow.co/)|Check if a netblock or IP address is malicious according to greensnow.co.|Free API
[grep.app](https://grep.app/)|Search grep.app API for links and emails related to the specified domain.|Free API
[GreyNoise](https://greynoise.io/)|Obtain IP enrichment data from GreyNoise|Tiered API
[HackerOne (Unofficial)](http://www.nobbd.de/)|Check external vulnerability scanning/reporting service h1.nobbd.de to see if the target is listed.|Free API
[HackerTarget](https://hackertarget.com/)|Search HackerTarget.com for hosts sharing the same IP.|Free API
Hash Extractor|Identify MD5 and SHA hashes in web content, files and more.|Internal
[HaveIBeenPwned](https://haveibeenpwned.com/)|Check HaveIBeenPwned.com for hacked e-mail addresses identified in breaches.|Commercial API
Hosting Provider Identifier|Find out if any IP addresses identified fall within known 3rd party hosting ranges, e.g. Amazon, Azure, etc.|Internal
[Host.io](https://host.io)|Obtain information about domain names from host.io.|Tiered API
Human Name Extractor|Attempt to identify human names in fetched content.|Internal
[Hunter.io](https://hunter.io/)|Check for e-mail addresses and names on hunter.io.|Tiered API
[Hybrid Analysis](https://www.hybrid-analysis.com)|Search Hybrid Analysis for domains and URLs related to the target.|Free API
IBAN Number Extractor|Identify International Bank Account Numbers (IBANs) in any data.|Internal
[Iknowwhatyoudownload.com](https://iknowwhatyoudownload.com/en/peer/)|Check iknowwhatyoudownload.com for IP addresses that have been using torrents.|Tiered API
[Instagram](https://www.instagram.com/)|Gather information from Instagram profiles.|Free API
[IntelligenceX](https://intelx.io/)|Obtain information from IntelligenceX about identified IP addresses, domains, e-mail addresses and phone numbers.|Tiered API
Interesting File Finder|Identifies potential files of interest, e.g. office documents, zip files.|Internal
[Internet Storm Center](https://isc.sans.edu)|Check if an IP address is malicious according to SANS ISC.|Free API
[ipapi.co](https://ipapi.co/)|Queries ipapi.co to identify geolocation of IP Addresses using ipapi.co API|Tiered API
[ipapi.com](https://ipapi.com/)|Queries ipapi.com to identify geolocation of IP Addresses using ipapi.com API|Tiered API
[IPInfo.io](https://ipinfo.io)|Identifies the physical location of IP addresses identified using ipinfo.io.|Tiered API
[IPQualityScore](https://www.ipqualityscore.com/)|Determine if target is malicious using IPQualityScore API|Tiered API
[ipregistry](https://ipregistry.co/)|Query the ipregistry.co database for reputation and geo-location.|Tiered API
[ipstack](https://ipstack.com/)|Identifies the physical location of IP addresses identified using ipstack.com.|Tiered API
[JsonWHOIS.com](https://jsonwhois.com)|Search JsonWHOIS.com for WHOIS records associated with a domain.|Tiered API
Junk File Finder|Looks for old/temporary and other similar files.|Internal
[Keybase](https://keybase.io/)|Obtain additional information about domain names and identified usernames.|Free API
[Koodous](https://koodous.com/apks/)|Search Koodous for mobile apps.|Free API
[LeakIX](https://leakix.net/)|Search LeakIX for host data leaks, open ports, software and geoip.|Free API
[Leak-Lookup](https://leak-lookup.com/)|Searches Leak-Lookup.com's database of breaches.|Free API
[Maltiverse](https://maltiverse.com)|Obtain information about any malicious activities involving IP addresses|Free API
[MalwarePatrol](https://www.malwarepatrol.net/)|Searches malwarepatrol.net's database of malicious URLs/IPs.|Tiered API
[MetaDefender](https://metadefender.opswat.com/)|Search MetaDefender API for IP address and domain IP reputation.|Tiered API
[Mnemonic PassiveDNS](https://www.mnemonic.no)|Obtain Passive DNS information from PassiveDNS.mnemonic.no.|Free API
[multiproxy.org Open Proxies](https://multiproxy.org/)|Check if an IP address is an open proxy according to multiproxy.org open proxy list.|Free API
[MySpace](https://myspace.com/)|Gather username and location from MySpace.com profiles.|Free API
[NameAPI](https://www.nameapi.org/)|Check whether an email is disposable|Tiered API
[NetworksDB](https://networksdb.io/)|Search NetworksDB.io API for IP address and domain information.|Tiered API
[NeutrinoAPI](https://www.neutrinoapi.com/)|Search NeutrinoAPI for phone location information, IP address information, and host reputation.|Tiered API
[numverify](http://numverify.com/)|Lookup phone number location and carrier information from numverify.com.|Tiered API
[Onion.link](https://onion.link/)|Search Tor 'Onion City' search engine for mentions of the target domain using Google Custom Search.|Free API
[Onionsearchengine.com](https://as.onionsearchengine.com)|Search Tor onionsearchengine.com for mentions of the target domain.|Free API
[Onyphe](https://www.onyphe.io)|Check Onyphe data (threat list, geo-location, pastries, vulnerabilities)  about a given IP.|Tiered API
[Open Bug Bounty](https://www.openbugbounty.org/)|Check external vulnerability scanning/reporting service openbugbounty.org to see if the target is listed.|Free API
[OpenCorporates](https://opencorporates.com)|Look up company information from OpenCorporates.|Tiered API
[OpenDNS](https://www.opendns.com/)|Check if a host would be blocked by OpenDNS.|Free API
[OpenNIC DNS](https://www.opennic.org/)|Resolves host names in the OpenNIC alternative DNS system.|Free API
[OpenPhish](https://openphish.com/)|Check if a host/domain is malicious according to OpenPhish.com.|Free API
[OpenStreetMap](https://www.openstreetmap.org/)|Retrieves latitude/longitude coordinates for physical addresses from OpenStreetMap API.|Free API
Page Information|Obtain information about web pages (do they take passwords, do they contain forms, etc.)|Internal
[PasteBin](https://pastebin.com/)|PasteBin search (via Google Search API) to identify related content.|Tiered API
PGP Key Servers|Look up e-mail addresses in PGP public key servers.|Internal
[PhishStats](https://phishstats.info/)|Check if a netblock or IP address is malicious according to PhishStats.|Free API
[PhishTank](https://phishtank.com/)|Check if a host/domain is malicious according to PhishTank.|Free API
Phone Number Extractor|Identify phone numbers in scraped webpages.|Internal
Port Scanner - TCP|Scans for commonly open TCP ports on Internet-facing systems.|Internal
[Project Honey Pot](https://www.projecthoneypot.org/)|Query the Project Honey Pot database for IP addresses.|Free API
[ProjectDiscovery Chaos](https://chaos.projectdiscovery.io)|Search for hosts/subdomains using chaos.projectdiscovery.io|Commercial API
[Psbdmp](https://psbdmp.cc/)|Check psbdmp.cc (PasteBin Dump) for potentially hacked e-mails and domains.|Free API
[Pulsedive](https://pulsedive.com/)|Obtain information from Pulsedive's API.|Tiered API
[PunkSpider](https://punkspider.io/)|Check the QOMPLX punkspider.io service to see if the target is listed as vulnerable.|Free API
[Quad9](https://quad9.net/)|Check if a host would be blocked by Quad9 DNS.|Free API
[ReverseWhois](https://www.reversewhois.io/)|Reverse Whois lookups using reversewhois.io.|Free API
[RIPE](https://www.ripe.net/)|Queries the RIPE registry (includes ARIN data) to identify netblocks and other info.|Free API
[RiskIQ](https://community.riskiq.com/)|Obtain information from RiskIQ's (formerly PassiveTotal) Passive DNS and Passive SSL databases.|Tiered API
[Robtex](https://www.robtex.com/)|Search Robtex.com for hosts sharing the same IP.|Free API
[searchcode](https://searchcode.com/)|Search searchcode for code repositories mentioning the target domain.|Free API
[SecurityTrails](https://securitytrails.com/)|Obtain Passive DNS and other information from SecurityTrails|Tiered API
[Seon](https://seon.io/)|Queries seon.io to gather intelligence about IP Addresses, email addresses, and phone numbers|Commercial API
[SHODAN](https://www.shodan.io/)|Obtain information from SHODAN about identified IP addresses.|Tiered API
Similar Domain Finder|Search various sources to identify similar looking domain names, for instance squatted domains.|Internal
[Skymem](http://www.skymem.info/)|Look up e-mail addresses on Skymem.|Free API
[SlideShare](https://www.slideshare.net)|Gather name and location from SlideShare profiles.|Free API
[Snov](https://snov.io/)|Gather available email IDs from identified domains|Tiered API
[Social Links](https://sociallinks.io/)|Queries SocialLinks.io to gather intelligence from social media platforms and dark web.|Commercial API
[Social Media Profile Finder](https://developers.google.com/custom-search)|Tries to discover the social media profiles for human names identified.|Tiered API
Social Network Identifier|Identify presence on social media networks such as LinkedIn, Twitter and others.|Internal
[SORBS](http://www.sorbs.net/)|Query the SORBS database for open relays, open proxies, vulnerable servers, etc.|Free API
[SpamCop](https://www.spamcop.net/)|Check if a netblock or IP address is in the SpamCop database.|Free API
[Spamhaus Zen](https://www.spamhaus.org/)|Check if a netblock or IP address is in the Spamhaus Zen database.|Free API
[spur.us](https://spur.us/)|Obtain information about any malicious activities involving IP addresses found|Commercial API
[SpyOnWeb](http://spyonweb.com/)|Search SpyOnWeb for hosts sharing the same IP address, Google Analytics code, or Google Adsense code.|Tiered API
SSL Certificate Analyzer|Gather information about SSL certificates used by the target's HTTPS sites.|Internal
[StackOverflow](https://www.stackexchange.com)|Search StackOverflow for any mentions of a target domain. Returns potentially related information.|Tiered API
[Steven Black Hosts](https://github.com/StevenBlack/hosts)|Check if a domain is malicious (malware or adware) according to Steven Black Hosts list.|Free API
Subdomain Takeover Checker|Check if affiliated subdomains are vulnerable to takeover.|Internal
[Sublist3r PassiveDNS](https://api.sublist3r.com)|Passive subdomain enumeration using Sublist3r's API|Free API
[SURBL](http://www.surbl.org/)|Check if a netblock, IP address or domain is in the SURBL blacklist.|Free API
[Talos Intelligence](https://talosintelligence.com/)|Check if a netblock or IP address is malicious according to TalosIntelligence.|Free API
[TextMagic](https://www.textmagic.com/)|Obtain phone number type from TextMagic API|Tiered API
[ThreatCrowd](https://www.threatcrowd.org)|Obtain information from ThreatCrowd about identified IP addresses, domains and e-mail addresses.|Free API
[ThreatFox](https://threatfox.abuse.ch)|Check if an IP address is malicious according to ThreatFox.|Free API
[ThreatMiner](https://www.threatminer.org/)|Obtain information from ThreatMiner's database for passive DNS and threat intelligence.|Free API
TLD Searcher|Search all Internet TLDs for domains with the same name as the target (this can be very slow.)|Internal
[Tool - CMSeeK]([https://github.com/Tuhinshubhra/CMSeeK](https://github.com/Tuhinshubhra/CMSeeK))|Identify what Content Management System (CMS) might be used.|Tool
[Tool - DNSTwist]([https://github.com/elceef/dnstwist](https://github.com/elceef/dnstwist))|Identify bit-squatting, typo and other similar domains to the target using a local DNSTwist installation.|Tool
[Tool - nbtscan]([http://www.unixwiz.net/tools/nbtscan.html](http://www.unixwiz.net/tools/nbtscan.html))|Scans for open NETBIOS nameservers on your target's network.|Tool
[Tool - Nmap]([https://nmap.org/](https://nmap.org/))|Identify what Operating System might be used.|Tool
[Tool - Nuclei]([https://nuclei.projectdiscovery.io/](https://nuclei.projectdiscovery.io/))|Fast and customisable vulnerability scanner.|Tool
[Tool - onesixtyone]([https://github.com/trailofbits/onesixtyone](https://github.com/trailofbits/onesixtyone))|Fast scanner to find publicly exposed SNMP services.|Tool
[Tool - Retire.js]([http://retirejs.github.io/retire.js/](http://retirejs.github.io/retire.js/))|Scanner detecting the use of JavaScript libraries with known vulnerabilities|Tool
[Tool - snallygaster]([https://github.com/hannob/snallygaster](https://github.com/hannob/snallygaster))|Finds file leaks and other security problems on HTTP servers.|Tool
[Tool - testssl.sh]([https://testssl.sh](https://testssl.sh))|Identify various TLS/SSL weaknesses, including Heartbleed, CRIME and ROBOT.|Tool
[Tool - TruffleHog]([https://github.com/trufflesecurity/truffleHog](https://github.com/trufflesecurity/truffleHog))|Searches through git repositories for high entropy strings and secrets, digging deep into commit history.|Tool
[Tool - WAFW00F]([https://github.com/EnableSecurity/wafw00f](https://github.com/EnableSecurity/wafw00f))|Identify what web application firewall (WAF) is in use on the specified website.|Tool
[Tool - Wappalyzer]([https://www.wappalyzer.com/](https://www.wappalyzer.com/))|Wappalyzer indentifies technologies on websites.|Tool
[Tool - WhatWeb]([https://github.com/urbanadventurer/whatweb](https://github.com/urbanadventurer/whatweb))|Identify what software is in use on the specified website.|Tool
[TOR Exit Nodes](https://metrics.torproject.org/)|Check if an IP adddress or netblock appears on the Tor Metrics exit node list.|Free API
[TORCH](https://torchsearch.wordpress.com/)|Search Tor 'TORCH' search engine for mentions of the target domain.|Free API
[Trashpanda](https://got-hacked.wtf)|Queries Trashpanda to gather intelligence about mentions of target in pastesites|Tiered API
[Trumail](https://trumail.io/)|Check whether an email is disposable|Free API
[Twilio](https://www.twilio.com/)|Obtain information from Twilio about phone numbers. Ensure you have the Caller Name add-on installed in Twilio.|Tiered API
[Twitter](https://twitter.com/)|Gather name and location from Twitter profiles.|Free API
[UCEPROTECT](http://www.uceprotect.net/)|Check if a netblock or IP address is in the UCEPROTECT database.|Free API
[URLScan.io](https://urlscan.io/)|Search URLScan.io cache for domain information.|Free API
[Venmo](https://venmo.com/)|Gather user information from Venmo API.|Free API
[ViewDNS.info](https://viewdns.info/)|Identify co-hosted websites and perform reverse Whois lookups using ViewDNS.info.|Tiered API
[VirusTotal](https://www.virustotal.com/)|Obtain information from VirusTotal about identified IP addresses.|Tiered API
[VoIP Blacklist (VoIPBL)](https://voipbl.org/)|Check if an IP address or netblock is malicious according to VoIP Blacklist (VoIPBL).|Free API
[VXVault.net](http://vxvault.net/)|Check if a domain or IP address is malicious according to VXVault.net.|Free API
Web Analytics Extractor|Identify web analytics IDs in scraped webpages and DNS TXT records.|Internal
Web Framework Identifier|Identify the usage of popular web frameworks like jQuery, YUI and others.|Internal
Web Server Identifier|Obtain web server banners to identify versions of web servers being used.|Internal
Web Spider|Spidering of web-pages to extract content for searching.|Internal
[WhatCMS](https://whatcms.org/)|Check web technology using WhatCMS.org API.|Tiered API
[Whoisology](https://whoisology.com/)|Reverse Whois lookups using Whoisology.com.|Commercial API
Whois|Perform a WHOIS look-up on domain names and owned netblocks.|Internal
[Whoxy](https://www.whoxy.com/)|Reverse Whois lookups using Whoxy.com.|Commercial API
[WiGLE](https://wigle.net/)|Query WiGLE to identify nearby WiFi access points.|Free API
[Wikileaks](https://wikileaks.org/)|Search Wikileaks for mentions of domain names and e-mail addresses.|Free API
[Wikipedia Edits](https://www.wikipedia.org/)|Identify edits to Wikipedia articles made from a given IP address or username.|Free API
[XForce Exchange](https://exchange.xforce.ibmcloud.com/)|Obtain IP reputation and passive DNS information from IBM X-Force Exchange.|Tiered API
[Yandex DNS](https://yandex.com/)|Check if a host would be blocked by Yandex DNS.|Free API
[Zetalytics](https://zetalytics.com/)|Query the Zetalytics database for hosts on your target domain(s).|Tiered API
[Zone-H Defacement Check](https://zone-h.org/)|Check if a hostname/domain appears on the zone-h.org 'special defacements' RSS feed.|Free API
