# Web Servers,Database and CMS Basic Hacking
NOTE: 
Before you read this you should know the basics and  
difference between WWW, HTTP protocol, TCP connection, ports, URLS, URI, webpage, website, search engine, Static website, Dynamic websites, VPS hosting and dedicated hosting? 

**A server is a central repository or the part of web hosting infrastructure that hosts websites**

  Front End (Web UI) <-> BackEnd (API) <-> Web server (web page and graphics files) <-> Load Balancer  <-> Application Server(Templete pages code & data)  <->  DataBase (Couch DB + MySql + Elasstic DB + MongoDB + Firebase )

## 1. Web Server: Web server will receive all the requests from sent by visitors visiting your website and also forward only the business requests to application server. The static assets (like CSS, JS components , Web components eg Common images, resources files and html components) will be served from your web server itself. 
Web server runs on Microsoft IIS:ASP(.NET), Apache: Php/CGI, Apache Tomcat: Servlet, Nginx, HTTPD ,Jetty: Servlet
or even Python's Simple HTTPServer etc.
Web servers primarily respond to HTTP / HTTPS requests however isn't restricted to simply communications protocol. It may be provided alternative protocol support like RMI/RPC.

## 2. Application server: Application server is the server that works between Web server and database server and basically Generate (dynamic content/assets by executing server side code eg JSP, servlet or EJB), manages(
â€¢ Transaction Support, Messaging support etc), processes the data(connection Pooling, object pooling etc) and host application etc and application server will be responsible for only business requests (like Login, Fetching details and etc,. )
		â—‹ MTS: COM+
		â—‹ Email server
		â—‹ WAS: EJB
		â—‹ JBoss: EJB
		â—‹ WebLogic Application Server: EJB
		â—‹ Google maps servers
		â—‹ Google search servers
		â—‹ Google docs servers
		â—‹ Microsoft 365 servers
		â—‹ Microsoft computer vision servers for AI.
â€¢ Application servers 
Application Server can do whatever Web Server is capable and respond to any number of protocols depending on the application business logic.

## 3. Database Server: Database server handles database queries and It can only accessed by application server. It runs on MySQL, PostgreSQL, MariaDB, etc.
Database servers use protocols ODBC, JDBC, etc.
--------------------------------------------------------------------------------
Please note:
	â€¢ Web Server is designed to serve HTTP static Content like HTML, images etc. and for the dynamic content have plugins to support scripting languages like Perl, PHP, ASP, JSP etc
	â€¢ Web container is a part of Web Server and the Web Server is a part of Application Server.
	â€¢ A Web Server in java is also known as a web container or a servlet container which has a limited set of Java EE features like Servlets, JSP etc. Ex: Apache Tomcat.
	â€¢ An Application Server has a web container in it as well as full java EE features like Java Mail Service, JPA, JSF etc.
	Ex:Glassfish, Apache TomEE, JBoss or Wildfly(new name ), IBM websphere etc.
	
	â€¢ If you have a Java application with just JSP and Servlet to generate dynamic content then you need web containers like Apache Tomcat or Jetty. While, if you have Java EE application using EJB, distributed transaction, messaging and other fancy features than you need a full fledged application server like JBoss, WebSphere or Oracle's WebLogic.
	â€¢ The use of Load Balancer is to distribute the load between multiple application servers. 
	â€¢ Application server can only accessed via web server, database server can only accessed by application server. 
	â€¢ If you want to solve web server and application server  purposes in one server, I would like to prefer you VPS hosting servers and dedicated hosting servers. It is because they host volumes of web projects and applications with a higher uptime.

Credit: <https://www.quora.com/Whats-the-diference-between-an-application-server-and-a-web-server> 
 https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Pages_sites_servers_and_search_engines
 

### Common Features Of web servers:
		a. HTTP 
		support for one or more versions of HTTP protocol in order to send versions of HTTP responses compatible with versions of client HTTP requests, e.g. HTTP/1.0, HTTP/1.1 plus.
		b. Authentication and store information about client's requests and server request regarding security and statistical purpose.
		
### Web Server availability:
	
		a. Apache- 34%  (compatible with Linux, Windows, FreeBSD, Mac and several other platforms. 
		b. NGINX 33%  is a different example because it works as a proxy server, together with another web server application like Apache.
		Large web sites with too much traffic generally use NGINX.
		c. Cloudflare web Server (17.6%)
		d. LiteSpeed Web Server (LSWS) (8%) It is a great software to be used as a local web server, or for small web hosting projects.)
		e. IIS by Microsoft (7.2%)
		f. Apache tomcat (
		Apache Tomcat had more market in the past, as Java Containers are not very used nowadays.
		g. GWS(by Google)
		h. Node.js (1.1%)

	Note:
		a. A website may use more than one web server.
		b. Nowadays almost all web server software is executed in *user mode* (because many of 
		Kernel-mode small disadvantages have been overcome by faster hardware, new OS versions and new web server software).
	


### Loads Control or load balancer
	A web server (program installation) usually has pre-defined load limits, because it can handle only a limited number of concurrent client connections (usually between 1 and several tens of thousands for each active web server process.)and it can serve only a certain maximum number of requests per second depending on: 
	
		â—‹ its own settings,
		â—‹ the average HTTP request type,
		â—‹ whether the requested content is static or dynamic,
		â—‹ whether the content is cached, or compressed,
		â—‹ the average network speed between clients and web server,
		â—‹ the number of active TCP connections,
		â—‹ the hardware and software limitations or settings of the OS of the computer(s) on which the web server runs.
	
	
#### Causes Of overload and high traffic
	Excess legitimate web traffic, DDOS, Computer worms, XXS worms, internet bots, network slowdown due to packages lost, web server's partial unavailability. Due to maintains or upgrade, failure etc.


### Website respond in case of overloads:
	web server returns an HTTP error code, such as 500, 502,[5] 503,[6] 504,[7] 4JUdGzvrMFDWrUUwY3toJATSeNwjn54LkCnKBPRzDuhzi5vSepHfUckJNxRL2gjkNrSqtCoRUrEDAgRwsQvVCjZbRyFTLRNyDmT1a1boZVinterrupts) TCP connections before returns any contacts. 


### Protection and Anti-overload Technique's 
		a. Managing network traffic, by using: 
			Â§ Firewalls to block unwanted traffic coming from bad IP sources or having bad patterns;
			i. HTTP traffic managers to drop, redirect or rewrite requests having bad HTTP patterns;
			ii. Bandwidth management and traffic shaping, in order to smooth down peaks in network usage.
		b. Deploying web cache techniques.
		c. Using different domain names or IP addresses to serve different (static and dynamic) content by separate web servers, e.g.: 
		http://images.example.com
		http://example.com
		d. Using different domain names or computers to separate big files from small and medium-sized files; the idea is to be able to fully cache small and medium-sized files and to efficiently serve big or huge (over 10 â€“ 1000 MB) files by using different settings.
		
		e. Using many web servers (programs) per computer, each one bound to its own network card and IP address.
		
		f. Using many web servers (computers) that are grouped together behind a load balancer so that they act or are seen as one big web server.
		g. Adding more hardware resources (i.e. RAM, disks) to each computer.
		h. Tuning OS parameters for hardware capabilities and usage.
		i. Using more efficient computer programs for web servers, etc.
		j. Using other programming workarounds, especially if dynamic content is involved.
		Using latest efficient versions of HTTP (e.g. beyond using common HTTP/1.1)
		
## Basic Hacking CMS:
	
	1. WORDPRESS (60%):
		As of right now over a quarter (25%) of the internet is built using WordPress. This is useful to know because that means a single exploit has the potential to impact a large portion of your targetâ€™s assets. There are in fact hundreds of exploits and misconfigurations impacting WordPress and its associated plugins. One common tool to scan for these vulnerabilities is wpscan: 
		
		â— https://github.com/wpscanteam/wpscan 
		â— wpscan --URL https://example.com
	
		Vast majority of the sites you scan are going to be patched. So do check out
		Index of â€œ/wp- content/uploads/â€ 
	
	2. Drupal is the third most popular CMS yet I seem to run into Drupal sites more than Joomla.
		This scanner also has the ability to scan additional CMSs as well: 
		
		â— https://github.com/droope/droopescan 
		â— python3 droopescan scan Drupal -u -t 32
	
	3. Joomla comes in second so you can expect to run into this CMS as well.
		Unlike WordPress sites who seem to be fairly locked down Joomla is a mess. If you want to scan for vulnerabilities the most popular tool is Joomscan: 
		
		â— https://github.com/rezasp/joomscan 
		â— perl joomscan.pl -u 
		
	4. If you ever run into the Adobe AEM CMS 
		you're about to find a whole bunch of vulnerabilities. 99% of the time this is an instant win! This CMS is riddled with public vulnerabilities and Iâ€™m 100% positive there are hundreds more zero days. Seriously this is one of the worst CMSs I have ever seen. If you want to scan an AEM application for vulnerabilities use the tool aemhacker:
		
		â— https://github.com/0ang3el/aem-hacker 
		â— python aem_hacker.py -u --host 
		
		There are Hundred's of different CMS to know about all 
		â— https;//wappalyzer.com/technologies
		
	### Conclusion:
		When you do find a CMS, you donâ€™t want to waste time manually testing the endpoint, you want to test for known CVEs and misconfigurations. The best way and 1st step to do this is to find some sort of CMS specific vulnerability scanner. If you can find that you can try searching exploit-db and google for known CVEs.
		
		
		Database server deals with the storing and managing the data of a computer or computer programs while web server is used to save the static and dynamic content and pages of websites.
		
## Basic Hacking Databases
	(Sensitive information such as passwords, tokens, private messages, and everything else and A lot of databases are missing authentication by default!):
	
			A database is an organized collection of sensitive data, generally stored and publicly accessible by users available most often interact directly with application server. 
		
			Front End (Web UI) -> BackEnd (API) -> Web server (web page and graphics files) ->  DataBase (Couch DB + MySql + Elasstic DB + MongoDB + Firebase )
			
			Front End (Web UI) <-> BackEnd (API) <-> Web server (web page and graphics files) <-> Load Balancer  <-> Application Server(Templete pages code & data)  <->  DataBase (Couch DB + MySql + Elasstic DB + MongoDB + Firebase )
			
			A website may use more than one web server, application and database.
			
			Compromising these databases normally involves exploiting an sql injection vulnerability but sometimes it can be much easier. These databases are often exposed to the internet without authentication leaving them open for hackers  as discussed in the following sections.
		
	### a. Google Firebase:
			The Firebase Realtime Database is a cloud-hosted database stored as JSON and synchronized in realtime to every connected clientâ€. An Vulnerability can arise in firebase due to database misconfiguration, when developers fail to enable authentication. Leaving a database exposed to the world unauthenticated is an open invite for malicious hackers
			
			Tips: 
			Identify: keep an eye out for the â€œ*.firebaseio.comâ€ url, if you see this then you know your target is utilizing Google's firebase DB.
				 â— Vuln-domain.firebaseio.com
			Exploit: You can easily view the database by appending a â€œ/.jsonâ€ to the url as shown below:
				 â— vuln-domain.firebaseio.com/.json
				
			Summary: 
				1) An attacker could then leverage these credentials to perform additional attacks on the application. 
				2) Finding and exploiting this misconfiguration is extremely easy and requires zero technical skills to pull off. All you need to do is find an application using firebase, append â€œ/.jsonâ€ to the url, and if there isn't authentication you can export the entire DB!
				3) Use google Dorks to find Juicy Information on Vuln-domain.firebaseio.com eg API, dashboard etc
				
	### 	b. ElasticSearch DB:(Port:9200 )
			You have probably heard of the popular relational database called MySQL. Elastic search is similar to MySQL, is a database used to hold and query information. However, elastic search is typically used to perform full text searches on very large datasets. Another thing to note is that ElasticSearch is unauthenticated by default which can cause a lot of security problems as described in the following sections. 
			
			ElasticSearch Basics :
			â€œElasticSearch is a document- oriented database designed to store, retrieve, and manage document-oriented or semi-structured data. When you use Elasticsearch, you store data in JSON document form. Then, you query them for retrieval.â€ Unlike MySQL which stores its information in tables, elastic search uses something called types. Each type can have several rows which are called documents. Documents are basically a json blob that hold your data as shown in the example below: 
			
			â— {"id":1, "name":"ghostlulz", "password":"SuperSecureP@ssword"} 
			
			In MySQL we use column names but in Elasticsearch we use field names. The field names in the above json blob would be id, name, and password. In MySQL we would store all of our tables in a database.
			In Elastic Search we store our documents in something called an index. An index is basically a collection of documents.
			
	### 	Unauthenticated ElasticSearch DB :
			Elastic search has an http server running on port 9200 that can be used to query the database. The major issue here is that a lot of people expose this port to the public internet without any kind of authentication. This means anyone can query the database and extract information. 
			A quick Shodan search will produce a tun of results as shown below:
			Port: "9200" elastic
			
			Once you have identified that your target has port 9200 open you can easily check if it is an Elasticsearch database by hitting the root directory with a GET request. 
			Once you know an endpoint has an exposed Elastic Search db try to find all the indexes(Databases) that are available. This can be done by hitting the â€œ/_cat/indices?vâ€ endpoint with a GET request. 
			
			This information along with other details about the service can also be found by querying the 
			â€œ/_stats/?pretty=1â€ endpoint.
			 To perform a full text search on the database you can use the following command 
			â€œ/_all/_search?q=emailâ€. This will query every index for the word â€œemailâ€. There are a few words that I like to search for which include: â— Username â— Email â— Password â— Token â— Secret â— Key 
			If you want to query a specific index you can replace the word â€œ_allâ€ with the name of the index you want to search against. 
			
			Another useful technique is to list all of the field names by making a GET request to the 
			â€œ/INDEX_NAME_HERE/_mapping?pretty=1â€ endpoint.
			 I typically search for interesting field names such as: â— Username â— Email â— Password â— Token â— Secret â— Key
			
			To query all values that contain a specific field name use the following command 
			â€œ/_all/_search?q=_exists:email&pretty=1â€ . This will return documents that contain a field name(column) named email.
			
			Again you can replace â€œ_allâ€ with the name of an index to perform searches specifically against that endpoint. 
			
			Summary:
			ElasticSearch is just another database where you can store and query information. The major problem is that people expose the unauthenticated web service to the public. With unauthenticated access to the web service attackers can easily dump the entire database. Always be on the lookout for port 9200.
			
	###	c. Mongo Database :(Port:27017 )
			Like Elasticsearch MongoDB is a nosql database that uses JSON-like documents to store data. Also similar to the rest of the databases we have talked about Mongo DB fails to implement authentication by default. This means it's up to the user to enable this which they often forget.
			
			Tips: 
			Identify: If you're searching for MongoDB instances, be on the lookout for port 27017 becuse authentication enabled by default so to test for this vulnerability just try to login.
			 To do this I normally just use the mongo cli just install it and run the cammand: 
				â— mongo ip-address-here 
			
			Exploit: Once logged into the database try issuing a command, if you get an â€œunauthorizedâ€ error message prompting for authentication then the endpoint has authentication enabled. However, if you can run arbitrary commands against the system then authentication has not been set up and you can do whatever you want. 
			
	  Summary:
			 If you see port 27017 open or any other MongoDB associate port make sure to test the endpoint to see if its missing authentication. Exploiting this misconfiguration is as easy as connecting to the database and extracting the data. This is as easy as it gets folks. 
			
	### d. CouchDB :(Port: 5985,6984) 
	###	e. CassandraDB: (Port:9042,9160)
  
  # This project is under development. anyway if you have suggestion for improvements or want to contribute feel free to raise a issue on Github. Thankyou :)
