# 1. JavaScript
# 2. JAVASCRIPT for Pentesters and Hackers:

-----------------------------------------------------------------------------------------------------------------------

# 1. [JavaScript](https://github.com/RESETHACKER-COMMUNITY/Resources/blob/main/Developer's/JavascriptForHacker.md) Click me, In case you want to Explore Deeper.
      ✅## What is the role of JS frameworks and libraries ?
      ✅## Does that mean “library” and “framework” two ways of saying the same thing? 
      ✅## Why do we use framework?

      ## Understanding ReactJS (for frontend - dev) - Updating Soon
      ## Understanding NodeJS(for backend - dev) - Updating Soon
      ## Understanding jQuery- [What can jQuery selector injection do?](https://teletype.in/@skavans/6x-dhjRVxjV)
      ✅## Understanding Meteor.js framework (Ahmed Ezzat & Rémi Testa)
          ### Attacking Meteor.JS

      ## Understanding Express (for backend - dev) - Updating Soon
      ## Understanding Ajax - Updating Soon
      ## Understanding Typescript - Updating Soon
      ## Bun(the future in Js) - a fast new JavaScript runtime like Node.js or Deno. 
      ✅## Understanding .Net framework (for backend - dev)
    

**JavaScript** (or JS for short) is a scripting language used by front end developers to implement and manage dynamic content. 
JavaScript was initially used only for the client-side but, in more recent times, it has also been used as a server-side programming language.

## What is the role of JS frameworks and libraries ?
It give developers the ability to use prewritten code for common JavaScript functions, and to create their own functions that can then be reused as needed.

## Does that mean “library” and “framework” two ways of saying the same thing? 
Not really. Yes, both tools have similar uses, but there are significant differences between the scope and scale of the two platforms.
![JS libraray vs framework](https://user-images.githubusercontent.com/25515871/176824106-79f174ba-ec22-406d-831b-5b78419727c8.png)

Examples of JavaScript Libraries:
    
    jQuery : DOM Manipulation
    React JS : User Interface framework
    Data-Driven Documents or D3.js( library to use when you are dealing with data. It manipulates the document based on the content and adds interactivity   with the help of HTML, SVG, and CSS. )
    TaffyDB : Database (JavaScript library that adds database features to our website.)

## Why do we use framework?
So a JavaScript Framework is an application skeleton, a complete structure that provides the programmer with the basic tools of creating a website or a web application. 
They consist of a huge collection of various JavaScript libraries that supplies the programmers with pre-written code and thus allows even those who don’t have a lot of programming knowledge.

### Most popular web frameworks:

![most-popular-web-frameworks-according-to-professional developers](https://user-images.githubusercontent.com/25515871/176917211-3757c0ce-c87f-4426-b8a6-52ad5df6c12c.png)
    
Note: 
Today no one directly uses javascript instead they use a framework especially if you are a company.

-----------------------------------------------------------------------------------------------------------------------

# 2. JAVASCRIPT FOR Pentesters and Hackers:

----------------------------------------------------------------------------------------------

 ## 2.1. Debugging Javascript code:
 	### 1.DevTools for Enumuration
	### 2.Detecting and Merging Splitted Bundles :
 ## 2.2. Understanding Juicy information, Collecting Urls, endpoints etc and Automating things 
   	### 1. Understanding Juicy information in Js files and collecting js files from Urls:
   	### 2. Automating and Enumarating information that might Lead to discovery of security issues and later you can fetch these list of Urs for -> SSTI, XSS, SQLi, SSRF, Open Redirect, IDOR etc 
   
 ## 2.3. Understand JS Code such as  what frameworks are being used, identify dangerous functions and component in the framework and then looking for them in the source code -> can get -> dom xss , Postmessage vulns, Logical Bugs etc
	### 1. Reading all the Js files and find something from Js code are hard so 
	### 2. Understand the places where developers tend to make mistakes that will lead to potential security issues.
	### 3. Automating potential security issues in source code.

## 2.4. Outcome (content discovery):
## 2.5. Bug Bounty — Tips / Tricks / JS (JavaScript Files)
## 2.6. Understanding regex logic in javascripts:
## 2.7 Recommended Links for chrome-devtools, Finding vulnerability in javascript.

----------------------------------------------------------------------------------------------

## 2.1.Debugging Javascript code:

	Idea is to finding vulnerabilty and information in urls and files 
	by understanding "How JavaScript is used in website? then breaking it:
	
  Open DevTools(right click and select inspect) > goto Netowrk 
    
    Select Js in the Options : In case you want to See all the Js files)
    Select XHR(XML HTTP Request or Simply fetching remote file with javascript) : In case you want to See Request made by javascript.
    Click on the Global listner from threads and you can see all the POST request that has been made within JS files.
    
    
  Detecting and Merging Splitted Bundles :
  	
	Why do website devide js file in multple Bundle and how to detect it during Enumuration?
	
	From an Developers standpoint, It save time by loading website elements faster.  
	for Example, If you have one giant file, it would take a long time to download that will cause the delay in websites loding rather than sending the whole file from server to your browser at once server will just send the part which the browser needs thus reducing the downloading time and loding time of webisite.
	
		Note:
		For bounty hunters we need to access the full source code at once as it may contain sensitive pieces of information and
		 .map files could have a lot of information and it’s exactly the same source code at the original developer's box. 
		 Depending on the situation this could be considered as source code disclosure (CWE-200) 
		 So don't just go reporting map files as source code disclosure understand your target and 
		 understand how this would affect them before reporting it.
    	
	Enumurating Splitted Bundles (Credit: Ahmed Ezzat (BitTheByte))
    	First, We need to detect the bootstrap code. this could be done easily by using 
	
	Chrome’s DevTools Search “Three dots > More Tools > select "Search” and Search for “Loading Chunk”.
	
	Loading Chunk will lools like main-[hash].js or has a different name and sometime you would not find any so 
	Use Chrome’s Dev tools Console but we need to edit the bootstrap function to return the full URL of the hosted file. 
	
	
![image](https://user-images.githubusercontent.com/25515871/177983439-7222f2af-8927-48a9-abdd-0209b807a5b6.png)
	
	Did you Notice inside the code	Ahmed Ezzat also added .map extension to the file URL.
	To decode the .map js bundle we can’t use the built-in source map decoder here instead we will use an awesome tool called [unwebpack-sourcemap](https://github.com/rarecoil/unwebpack-sourcemap)
	python3 unwebpack_sourcemap.py --make-directory https://example.com/assets/UserNameComplete-d6c0c7fc8bc309d9b022.js.map output
	After running the above command on every map file we will be able to access the full frontend source code.
	
	After getting the Most of the source code you can try ####Enumurating Juicy information in Js*  
	eg By just adding a breakpoint on the redirect condition and changing it to the other branch 
	you may able to access the UI revealing that it doesn’t have any server-side protection 
	allowing anyone to access the internal log with some other juicy stuff :)

## 2.2. Understanding Juicy information, Collecting Urls, endpoints etc and Automating things :
  
  ### Identifying and gathering JavaScript files in an application.
     
     'BurpSuite' > proxy > HTTP history and use the display filters to only display the Js files used by the application > copy the URLs for all the JavaScript files displayed.
     Export all the scripts. Under Target > Site map right click on the site of interest and select Engagement tools > Find scripts . Using this feature you  can export all the scripts in that application and also copy URLs.

  ### Understanding Juicy information in Js files and collecting js files from Urls:
      
   #### Identifying secrets in source code files using either regex or entropy. 
        
        Regex search will be able to identify credentials that are set by users such as usernames and passwords.
	[List of regex for scraping API and juicy information](https://github.com/h33tlit/secret-regex-list)
	[thehackerish - JavaScript Enumeration in practice with a live example](https://www.youtube.com/watch?v=G2pWVBgCjvg)

        Entropy based search is effective in identifying sufficiently random secrets such as API keys and tokens.
    
   #### Enumurating Juicy information in Js* 
	such as interesting url, hidden paths, old version(or vulnerable) js library/framework , subdomain, Sensitive API keys found at comments,DOM Based XSS with 		parameter such as redirect etc, credentials, hardcoded secrets, internal api, ports or portals and their creds -> port scan on internal domains, token, passowrd, 	  admin, src strict ,csrf, session, database cred, logs, , .map js files , credentials leak, endpints, etc
	
	##### 
		  
	Tools to Enumurate Js Urls-> 
	Waymore + xnLinkFinder, jsscanner , linkfinder, jsfinder, relative-url-extractor and lots of one liner commands , getjs etc
-------------------------------------------------------------------------------------------------------
 ### Colecting Js Script Files in target.
		//#### 1. Manual - Colecting Js Script Files in target//

	
	
   #### Automation - Colecting Js Script Files in target:

     This One liner will collect all known URLs for our target from the AlienVault’s Open Threat Exchange (OTX), the Wayback Machine and Common Crawl, fetch them using httpx and then display only javascript files.
     
        echo target.com | gau | grep '\.js$' | httpx -status-code -mc 200 -content-type | grep 'application/javascript'
       https://github.com/projectdiscovery/httpx
       https://github.com/lc/gau
      
----------------------------------------------------------------------------------------------------------------
	    In case you want to only collect the Js files from 'waybackurls' :

	      waybackurls target.com | grep "\.js" | uniq | sort
	      go get github.com/tomnomnom/waybackurls

	   To avoide the 'false potive' or dead server/ pages.

	      cat js_files_url_list.txt | parallel -j50 -q curl -w 'Status:%{http_code}\t Size:%{size_download}\t %{url_effective}\n' -o /dev/null -sk

	   Using 'curl or hakcheckurl' to check for the status of the JavaScript files on the server could be cumbersome. 

	      go install github.com/hakluke/hakcheckurl@latest
	      cat lyftgalactic-js-urls.txt | hakcheckurl

	      //hakcawler - To grep things like, subdomain,url,form,javascript,robots etc//



   ### Automating and Identifying information that might Lead to discovery of security issues -> SSTI, XSS, SQLi, SSRF, Open Redirect, IDOR etc 
   
   *Sometime Just looking through code can give plenty of information as i have mentioned in 
   *Enumurate Juicy information* but let's focous on fetching full URLs, relative URL/Paths, 
   endpoints, etc. that potentially lead to admin access file/page/endpoints.*
      
      You can automate this process: 
      
         Using relative-url-extractor to extract relative paths from remote JS file
         LinkFinder by Gerben Javado is quite handy in identifying all the endpoints and their parameters in JavaScript files.
         python linkfinder.py -i https://example.com -d -o cli
         
       Extract API endpoints from javascript files:
         cat file.js | grep -aoP "(?<=(\"|\'|\`))\/[a-zA-Z0-9_?&=\/\-\#\.]*(?=(\"|\'|\`))" | sort -u
         
         
       Find hidden GET parameters in javascript files:
          1. If see  javascript files for variable names, e.g.: var test = "xxx" or var page=" in JS File or page source .
          2. Try each of them as a GET parameter to uncover hidden parameters, e.g.: https://example.com/?test=”xsstest
          
         One Liner to finds all variable names and appends them as parameters:
          assetfinder example.com | gau | egrep -v '(.css|.png|.jpeg|.jpg|.svg|.gif|.wolf)' | while read url; do vars=$(curl -s $url | grep -Eo "var [a-zA-Z0-9]+" | sed -e 's,'var','"$url"?',g' -e 's/ //g' | grep -v '.js' | sed 's/.*/&=xss/g'); echo -e "\e[1;33m$url\n\e[1;32m$vars"; done
          
          From Js request checkout the Api endpoint then search the keyword
	  (for eg Api/hello hello is the keyword here) in Js files or code.To understand the Js behavior.
   
          You can brute force endpoints.(but If you understand the Js code then You'll potentially 
	  have more success finding endpoints that matter and create your own wordlist or add it to the existing Wordlists.)
   
   
       Try reading the js file/code by seaching sensative keywords(api, token, http, https://,key, //# sourceMappingURL=*.js.map etc). 
       Burp-suite Extension(https://github.com/BitTheByte/BitMapper) For finding .map files inside Javascripts.
    
        DumpsterDiver, Repo-supervisor and truffleHog are some fantastic tools to search for secrets in source code files.
        
        https://github.com/securing/DumpsterDiver
        python DumpsterDiver -p ~/jsfiles
        [How to use DumpsterDiver to find hardcoded secrets](https://latesthackingnews.com/2018/07/10/dumpsterdiver-the-tool-for-finding-hardcoded-secrets/)
     
## 2.3 Understand JS Code such as  what frameworks are being used, identify dangerous functions and component in the framework and then looking for them in the source code -> can get -> dom xss , Postmessage vulns, Logical Bugs etc

	Many researchers may opt out of deep diving into Google's JavaScript because of their heavy obfuscation and optimization. 
	This could be an ideal location for hackers or security researchers to find undiscovered DOM based vulnerabilities.

### Reading all the Js files and find something from Js code are hard so 

       Click on the Global listner from threads and you can see all the POST request that has been made within JS files.
     		To Understand about listner and How to use it find vulnerabilty in JS code :
     		Recommand you to play here (https://public-firing-range.appspot.com and /dom/index.html)
     
       Reading gathered, Deobfuscated or Minify JavaScript using deobfuscatedjavascript.com , UglifyJS, JSBeautifier, Vs code etc 
   	    To 'Install Js Beautifier' using PIP : pip install jsbeautifier
 		To use it : 
      		jsbeautifier -o output.txt javascriptfiles.txt 
      		Search juicy keyword on output.txt (after using Jsbeautifier on javascriptfiles.txt ) using GREP : 
      		grep -color -i JUICYKEYWORD output.txt
      		Here -color : to highlight "JUICYKEYWORD" and -i to support Upper and lower letter.
      		JUICYKEYWORD Such as : token, session api, key, csrf etc

       Google important Js file in different framework/Libraries for example important Js files in Reac Js 
       are /authProvider.js, config.js, App.js, users.js, /MyUrlField.js, /posts.js, Dashboard.js  etc then only check selected Js files.
     
       Privious CVE and Outdated component,Outdated framework and Outdated librabey could lead to vulenrability.
       ( Retire.js is a tool that can identify outdated JavaScript frameworks.
       Although RetireJS can report some false positives and not everything reported by RetireJS is vulnerable).
	
       You can also goto the wayback machine of page and check the 1st version of code to understand the changes. 
       or Use jsmon(API key needed to push the notification) with corn jobs on daily/weekly/monthy basis 
       to [track the changes in Js code](https://github.com/robre/jsmon)
     

### Understand the places where developers tend to make mistakes that will lead to potential security issues.

        a. Usage of innerHTML indicates that there might be possible XSS issue. 
	In the modern client-side JavaScript frameworks innerHTML equivalents do exist 
	such as the aptly named dangerouslytSetInnerHTML in React framework and 
	they did result in serious security vulnerabilities in the past .
	
        b.eval function is another place where things can go wrong both on client-side and server side.
	
       c.Improper usage of bypassSecurityTrustX methods in Angular can also lead to XSS issues.
        

List of bypassSecurityTrustX methods in Angular:
        ![Getting deeper with JS code review](https://user-images.githubusercontent.com/25515871/176961444-9cd0b727-897e-4c15-b7cf-cd971fb956e7.png)
        
        **postMessage** API is an alternative to JSONP, XHR with CORS headers and 
	other methods enabling sending data between origins by bypassing Same Origin Policy(SOP). 
	The idea of bypassing SOP and communicating with different origin should be of interest to attackers. 
	There are various security pitfalls when using postMessage. 
	Once you understand the possible security issues associated with postMessage, 
	you can look for the implementation in JavaScript files. On the message sender side, 
	look for window.postMessage and on the receiver end look for a listener window.addEventListener . 
	You’ll have to keep in mind that a lot of frameworks implement wrappers around postMessage
        
        **localStorage and sessionStorage** are HTML Web Storage Objects. 
	With web storage, web applications can store data locally within the user’s browser. 
	It is important to identify what is being stored using the Web Storage 
	especially storing anything sensitive can lead to potential security issues. 
	In the JavaScript, you can look for window.localStorage and window.sessionStorage.

### Automating the potential security issues in source code.

	*Using security linters [ESLint (https://github.com/LewisArdern/eslint-plugin-angularjs-security-rules)
	- easily customisable by adding custom security rules] 

	*static security scanners(**JSPrime**) will make it easy to identify low hanging vulnerabilities
	in JavaScript code but the project hasn’t been updated in a while.

[List of regex for scraping API and juicy information.](https://github.com/h33tlit/secret-regex-list)
[Hacktrick - Steal Information in JS](https://book.hacktricks.xyz/pentesting-web/xss-cross-site-scripting/steal-info-js)
	
	
## 2.4 Outcome (content discovery):
    
    1. Information Leakage such as API, key ,token, passowrd, admin, src strict,
    	csrf, session, secret, database, logs, , .map , endpints,credentials leak, etc.
    2. Vulnerably in Javascript code such as DOM XSS(or client side XSS).(To the DOM XSS reports site:hackerone.com intext:dom XSS )
    3. you can extract endpoints to automate XSS, SQL, RCE, open redirectory etc or for manual purpose.
    4. Create your own wordlist with endpoint and bruteforce the end points.
    5. Misconfiguration , Js version recent vulnerabilty and exploits. 
    6. If you know of an endpoint which returns 403 since it’s an admin endpoint 
    	but have you ever imagined knowing the correct directories and parameters sometimes can
	turn 403 into 200 (because of misconfigurations) and then into a SQLi? ;)
      

## 2.5 Bug Bounty — Tips / Tricks / JS (JavaScript Files)
 #[snyk - Javascript security vulenrability](https://snyk.io/learn/javascript-security/)
![Javascript-vulnerability](https://user-images.githubusercontent.com/25515871/176843087-1e7a5d83-144d-4148-967c-b0425900aacd.jpg)

## 2.6 Understanding regex logic in javascripts:
[List of regex for scraping API and juicy information](https://github.com/h33tlit/secret-regex-list)

Senario : [Mobile Feedback URL Redirect Regex/Validation Flaw](https://buer.haus/2015/02/03/google-com-mobile-feedback-url-redirect-regexvalidation-flaw/#more-34)
	
	The normal flow of the application:

    	Load this URL:https://www.google.com/tools/feedback/mobile_feedback?hl=en&url=http://www.myexample.com/&redirect=true&authuser=0&pi=17&hl=en
   	 Write in some feedback and click the submit button.
    	Click the close button.
   	 ---> You are redirected to myexample.com.

	 Here logic was being handled by JavaScript and to dive into the obfuscated script (for URL it was mobile_submitter__en.js). 
	 After using a beautifier(to get a better understanding the code) and using breakpoints in Firebug, Few keypoints to note
	
Regex in code :

	var Tb = /^(?:([^:/?#.]+):)?(?:\/\/(?:([^/?#]*)@)?([^/#?]*?)(?::([0-9]+))?(?=[/#?]|$))?([^?#]+)?(?:\?([^#]*))?(?:#(.*))?$/;

    	Google were parsing the URL(myexample.com) you sent in the url request var with regex.
    	then it was checking if the protocol section was null. http, or https before redirecting URL it was using window.location.href.

	This was important to know because:

    	If the protocol is null, it assumes that you are being redirected to a relative path.
    	window.location.href can be vulnerable to Cross-Site Scripting if redirected to "javascript:".

This is what the code looked like:

	Redirect logic in js code:

	if ("http" == a || "https" == a || "" == a) {
	window.location.href = this.d;
	return
	}

The Flaw:

	After the URL gets parsed and right before redirecting it will validate that the URL's protocol is either http, https, or blank. 
	Where "http" == a, a is the second position in the array. 
	In the window.location script, d is the first position of the array, which is the original unparsed URI.
	
	
	Example:
	https://www.google.com/tools/feedback/mobile_feedback?hl=en&url=http://login:pass@www.google.com:80/1/2%3F3=4&5=6%237=8&redirect=true&authuser=0&pi=17&hl=en

	Redirect URI:
	http://login:pass@www.google.com:80/1/2?3=4&5=6#7=8
	
	Regex results:
	0: "http://login:pass@www.google.com:80/1/2?3=4&5=6#7=8" [0, 51]
	1: "http" [0, 4]
	2: "login:pass" [7, 17]
	3: "www.google.com" [18, 32]
	4: "80" [33, 35]
	5: "/1/2" [35, 39]
	6: "3=4&5=6" [40, 47]
	7: "7=8" [48, 51]
	
	As you can see, there are a lot of parts in the URL that the regex is looking for. Not every URL is going to have this data, 
	so they are using question marks to state that the capture group is optional. 
	

The Fix

	The new version of mobile_submitter__en.js with the changes:
	https://www.gstatic.com/feedback/js/asil0m973whx/mobile_submitter__en.js

	Changes:

	if ("http" == a || "https" == a) {
	window.location.href = this.d;
	return
	}

This did not change the regex flaw, but it requires that the request variable that you send contain a full path URL with a protocol of http or https.


      
## 2.7 Recommended Links for chrome-devtools, Finding vulnerability in javascript
 
      https://howtodoinjava.com/ (This is one of intresting webiste that i have came across still need to explore)
      https://developers.google.com/web/tools/chrome-devtools
      https://developers.google.com/web/tools/chrome-devtools/javascript
      https://youtu.be/44D-FSAj3PQ
      https://youtu.be/FTeE3OrTNoA
      https://www.youtube.com/watch?v=NjJ_f1y7Kz4
      https://blog.appsecco.com/static-analysis-of-client-side-javascript-for-pen-testers-and-bug-bounty-hunters-f1cb1a5d5288
      
      Performing JavaScript Static Analysis by Lewis Ardern [Video]
      https://statuscode.ch/2015/05/static-javascript-analysis-with-burp/
      http://blog.blueclosure.com/2017/10/javascript-dangerous-functions-part-2_29.html
      https://reverseengineering.stackexchange.com/questions/4561/how-to-deobfuscate-an-obfuscated-javascript-file-like-this
      https://labs.detectify.com/2016/12/08/the-pitfalls-of-postmessage/
      https://angular.io/guide/security
      https://blog.jse.li/posts/marveloptics-malware/
      https://thehackerblog.com/i-too-like-to-live-dangerously-accidentally-finding-rce-in-signal-desktop-via-html-injection-in-quoted-replies/index.html
      https://medium.com/@alex.birsan/the-bug-that-exposed-your-paypal-password-539fc2896da9
      https://www.infosecmatter.com/bug-bounty-tips-4-aug-03/#2_find_javascript_files_using_gau_and_httpx
      https://github.com/robre/jsmon (a javascript change monitoring tool for bugbounties )
      [Difference between variable declaration syntaxes in Javascript (including global variables)?]
      (https://stackoverflow.com/questions/4862193/difference-between-variable-declaration-syntaxes-in-javascript-including-global)
      
## If you have any suggestion, or have ideas for improvements, please feel free to raise an issue on Github. 
