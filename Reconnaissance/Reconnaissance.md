### Sub domains (Search engine, archive data github, shodan, domains/subdomains from Js source code, brute force subdomains, wordlist to enumurate subdomains (you'll find it on github ) and manual explore)
		
    ○  Horizontal 
		
    ○  Vertical subdomains
    
			§ Sub domains Enumurations
			
				□ Chaos.project discovery.io
				□ Sublister
				□ Amass
				□ Aquatone
				□ Knockpy
				□ Assetfinder
				□ Findomain
				
				
			§ Subdomains Brute forcing
			Sometimes, passive DNS data simply doesn’t provide us with all of the subdomains associated with an entity — which is a problem 
			if your goal is to perform all-encompassing vertical domain enumeration. Plus, there could also be newer subdomains — new enough 
			that they still haven’t been spotted by Internet crawlers.
			In these scenarios, subdomain brute-forcing can be beneficial. In this process, a large list that contains common subdomain names
			is used, and by appending the target domain to them and sending an HTTP request, new subdomains can be discovered.
			
				□ Subfinder - Brute force subdomains +wordlists.
				□ Subbrute/ gobuster
				□ Alt-DNS (Sub-subdomains)
				
			§ Historical/archive data
				□ Web = Gau, waybackurls  
				□ DNS = Sectrails , Recondev
				
			§ Virtual Host discovery
			( A virtual host includes a name and set of domains that get routed to it based on the incoming request's host header.)
			
				□ Vhost-brute, virtual-host-discovery,virustotal_subdomains_enum.py, vhostbrute
			
			§ Scrap domains from JS/source code (Still need to verify)
			Gospider

			§ Find Domains from already discovered subdomains,By examining A records, CNAME of public DNS server of each discovered subdomains.
		
			Turbolist3r queries public DNS servers for each discovered subdomain. If the subdomain exists (i.e. the resolver replied with an address),
			the answer is categorized as CNAME or A record. By examining A records, it is possible to discover potential penetration testing targets
			for a given domain. Likewise, the process of looking for subdomain takeovers is simple; view the discovered CNAME records and investigate
			any that point to applicable cloud services.
			
			
			§ Find hidden subdomains using of Natural Language Processing and the Keras LSTM RNN API (Python-based, deep learning API that runs on top
			of the TensorFlow machine learning platform, and fully supports GPUs.) It will read in a file of already discovered subdomains for the 
			target and generate its own list of potential subdomains the target may have. 
			
			It then verifies the existence of those subdomains with a quick DNS lookup and will ultimately tell you if it has made any discoveries.
			
			 https://github.com/JetP1ane/Affinis.git
			python3 ~/Affinis/Affinis.py xyz.com 500 ~/xyzSubAll.txt
			
			Or also check https://www.wolframalpha.com it uses natural language and computation to find details and only show the popular subdomain.


### Certificate Transparency
		○ Crt.sh, certspotter, certificatetransperency.org, facebook CT,


### Once you already know the IP space of your target, you can reverse query all the IP addresses and locate the valid domains. 
	
	IP and Ports
	(Open Port & services version to find out later vulnerabilities and exploits)
	#### ACTIVE SCANNING:
		
		○ IP range
				□ Recon-ng(Tool), ARN, APNIC, ICANN , RPE
		○ Port  Services : 
				□ Masscan, nmap, nabu
		○ Passive DNS monitoring
				□ Sublert
		○ DNS permutation
				□ shuffleDNS,dnsgen,altdns
		○ DNS resolvers
				□ Dnsprobe, massdns
	
	#### PASSIVE SCANNING(Use 3rd party resources to learn about a machine ports without interacting with with the server)
	
		○ Shodan, censys and project sonar etc
Login Brute Forcing  endpoints, parameters (Check out this folders or google dork)
