# JAVASCRIPT FOR HACKER

**JavaScript** (or JS for short) is a scripting language used by front end developers to implement and manage dynamic content. 
JavaScript was initially used only for the client-side but, in more recent times, it has also been used as a server-side programming language.

NOTE: 
1. Dynamic content includes animated graphics, interactive forms, photo carousels, etc.—anything you see when you’re visiting a website or using an app that “changes” on screen without you having to do a manual refresh.
The autocomplete feature that happens when you’re entering search terms into Google’s search bar? That’s JavaScript in action.
 
2. In terms of websites and web applications, UIs are the collection of on-screen menus, search bars, buttons, and anything else someone interacts with to USE a website or app.

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

Eg: We can easily understand a framework with the example of a collage maker. 

    These applications have some photo frame ideas that you can choose from.
    You just have to sit and decide which frame you like the most. 
    You don’t have to position them all by yourself which provides faster results. But they have limited choices to select from.
    
 Examples of some Popular Js frameworks:

    Angular :  Pros. Cons. Open Source. Single page applications. ...
    React : Pros. Cons. Easy to learn. Reusable components. ...
    Vue. js : Pros. Cons. ...
    Ember. js : Pros. Cons. ...
    Meteor : Pros. Cons. Offers several conveniences. ...
    Mithril : Pros. Cons. Lightweight. ...
    Node. js : Pros. Cons. ...
    Polymer : Pros. Cons. Good for single-page applications.
    
NotE: 
Today no one directly uses javascript instead they use a framework especially if you are a company.

[Why do we have so many framework?  To Understand this you need to know about pro's and con's of all the framework](https://hackr.io/blog/best-javascript-frameworks)


### Understanding ReactJS

## .Net framework (for backend - dev)
.NET is a software development framework and ecosystem designed and  to allow for easy desktop and web application engineering. it provides the programming environment for most software development phases. .NET best suits businesses that look for a wide range of features like web-based services, desktop software, and cloud infrastructure support.

The .NET Framework released back in 2002 is the first and oldest implementation of the platform. It includes three main application models – WPF, Windows Forms, ASP.NET Forms – and Base Class Library.
.NET best suits businesses that look for a wide range of features like web-based services, desktop software, and cloud infrastructure support.

![asp net Mvc](https://user-images.githubusercontent.com/25515871/176917424-8c1593cc-1e29-4eb8-a254-71e85f1ba3b6.png)
  
   ASP.NET MVC is a web application framework developed by Microsoft that allows software developers to build a web application as a composition of three roles: Model, View and Controller. It is no longer in active development. It provides a distinct separation between the HTML view, the C# model, and the server-based controller. 
  
   Windows Presentation Foundation (WPF) is a UI framework used for creating graphical interfaces primarily for desktop client applications on Windows OS. WPF uses the capabilities of Extensible Application Markup Language (XAML).

   Windows Forms is a GUI class library within .NET Framework. Windows Forms are used to develop desktop applications with rich graphics that are easy to update and deploy.

   ASP.NET. While the previous two components are designed for desktop engineering ASP.NET is used to develop dynamic websites and web applications. There is the Common Language Runtime (CLR) in its core that gives developers the opportunity to write ASP.NET code using different .NET languages that we discuss below.

The newest .NET 6 version(in November 2021) delivered a unified platform for building projects across cloud, browser, IoT, mobile, and desktop environments, enabling all to use the same .NET libraries, SDK, and runtime.
![the-net-6-unified-development-platform](https://user-images.githubusercontent.com/25515871/176915446-82b5a414-3df0-466f-83d6-534b76c03bae.png)


REF: 
https://www.ptsecurity.com/upload/corporate/ru-ru/webinars/ics/V.Kochetkov_breaking_ASP.NET.pdf
[Still need to review this PDF](https://owasp.org/www-pdf-archive/ASDC12-Hacking_NETC_Applications_The_Black_Arts.pdf)

### Most popular web frameworks:
![most-popular-web-frameworks-according-to-professional developers](https://user-images.githubusercontent.com/25515871/176917211-3757c0ce-c87f-4426-b8a6-52ad5df6c12c.png)

## Debugging Javascript code:
 
  Open DevTools(right click and select inspect) > goto Netowrk 
    
    Select Js in the Options : In case you want to See all the Js files)
    Select XHR(XML HTTP Request or Simply fetching remote file with javascript) : In case you want to See Request made by javascript.

### Do a Stactic Analysis (Idea is finding vulnerabilty in Js code by understanding the how website is using javascripts then breaking it with payloads):
  
   Try reading the code by seaching keywords(api, token, http, https:// etc). Sometime Just looking through code can give you endpoints that has admin access.
   
   You can also goto the wayback machine of page and check the 1st version of code to understand the changes.
   
   From Js request check out the Api endpoint then search the keyword(for eg Api/hello hello is the keyword here) in Js files or code.
   
   You can brute force endpoints.(but If you understand the Js code then You'll potentially have more success finding the endpoints and creating your own wordlist beacuse Bruteforec use Wordlist and there is highter chance that endpint is not availabe in wordlists.)

### Reading all the Js files and find something from Js code are hard so 

     Click on the Global listner from threads and you can see all the POST request that has been made within JS files.
     To Understand about listner and How to use it find vulnerabilty in JS code :
     Recommand you to play here (https://public-firing-range.appspot.com and /dom/index.html)

 Impact:

    Vulnerably in Javascript code could lead you DOM XSS(or client side XSS).(To the DOM XSS reports site:hackerone.com intext:dom XSS )
    You can also use open source tools to fetch all the Js link/file from waybackurl and use automated tools to chaeck for vulenerabilty.

Recommended Links for chrome-devtools, Finding vul in javascript
      
      https://developers.google.com/web/tools/chrome-devtools
      https://developers.google.com/web/tools/chrome-devtools/javascript
      https://youtu.be/44D-FSAj3PQ
      https://youtu.be/FTeE3OrTNoA

# Bug Bounty — Tips / Tricks / JS (JavaScript Files)
 #[Javascript security vulenrability](https://snyk.io/learn/javascript-security/)
![Javascript-vulnerability](https://user-images.githubusercontent.com/25515871/176843087-1e7a5d83-144d-4148-967c-b0425900aacd.jpg)


[Steal Info JS](https://book.hacktricks.xyz/pentesting-web/xss-cross-site-scripting/steal-info-js)

If you know of an endpoint which returns 403 since it’s an admin endpoint but have you ever imagined knowing the correct directories and parameters sometimes can turn 403 into 200 (because of misconfigurations) and then into a SQLi? ;)
