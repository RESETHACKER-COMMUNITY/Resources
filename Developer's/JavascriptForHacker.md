# 1. JavaScript
      ✅ ## What is the role of JS frameworks and libraries ?
      ✅ ## Does that mean “library” and “framework” two ways of saying the same thing? 
      ✅ ## Why do we use framework?
      
		    Angular :  Pros. Cons. Open Source. Single page applications. ...
		    React : Pros. Cons. Easy to learn. Reusable components. ...
		    Vue. js : Pros. Cons. ...
		    Ember. js : Pros. Cons. ...
		    Meteor : Pros. Cons. Offers several conveniences. ...
		    Mithril : Pros. Cons. Lightweight. ...
		    Node. js : Pros. Cons. ...
		    Polymer : Pros. Cons. Good for single-page applications.
	  
	  ## understanding SolidJs (fastest UI designing) - Updating Soon
          ## Understanding ReactJs (UI designing for frontend - dev) - Updating Soon
          ## Understanding NodeJS(for backend - dev) - Updating Soon
	  ## Understanding NestJS(for backend - dev) - Updating Soon
	  ## Understanding Flutter(UI software development kit created by Google. It is used to develop cross platform applications for Android, iOS, Linux, macOS, Windows, Google Fuchsia, and the web from a single codebase.) - Updating Soon
          ## Understanding jQuery- [What can jQuery selector injection do?](https://teletype.in/@skavans/6x-dhjRVxjV)
      ✅ ## Understanding Meteor.js framework (Ahmed Ezzat & Rémi Testa)
          	### Attacking Meteor.JS

          ## Understanding Express (for backend - dev) - Updating Soon
          ## Understanding Ajax - Updating Soon
          ## Understanding Typescript - Updating Soon
          ## Bun(the future in Js) - a fast new JavaScript runtime like Node.js or Deno. 
      ✅ ## Understanding .Net framework (for backend - dev)
      



# 1. JAVASCRIPT 

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
    
Note: 
Today no one directly uses javascript instead they use a framework especially if you are a company.

![most-popular-web-frameworks-according-to-professional developers](https://user-images.githubusercontent.com/25515871/176917211-3757c0ce-c87f-4426-b8a6-52ad5df6c12c.png)

[Why do we have so many framework?  To Understand this you need to know about pro's and con's of all the framework](https://hackr.io/blog/best-javascript-frameworks)


## Understanding ReactJS (for frontend - dev)
Updating Soon

## Understanding NodeJS(for backend - dev)
Updating Soon

## Understanding jQuery
- [What can jQuery selector injection do?](https://teletype.in/@skavans/6x-dhjRVxjV)

##  Understanding Meteor.js framework (Ahmed Ezzat & Rémi Testa)
	
	Meteor is an open source platform for web, mobile, and desktop used by over half a million developers around the globe 
	to make shipping javascript applications simple, efficient, and scalable.
	
	Prerequisite(s):
		NoSQL Injection
    		Socket based communication
	
	What Meteor Does For You ?
	Many of these are care of Dan Dascalescu comprehensive answer on Quora referenced below.

		1. The publish/subscribe mechanism limits the data that can be retrieved from the server. 
		   Operations on client-side collections are by default restricted.
		2. Meteor doesn’t use session cookies, which makes Cross-Site Request Forgeries (CSRF) impossible.
		3. All user input is HTML-escaped when being displayed back to the client, thanks to the Handlebars-like {{…}} templates. A first defence against XSS.
		4. Meteor uses the best crypto to store hashed passwords — bcrypt
		5. Content Security Policy support is provided by the browser-policy-*core packages.
		6. For the paranoid, a full-database encryption layer that runs on top of Meteor exists, calledMylar. 
		It stores only encrypted data on the server, and decrypts data only in users’ browsers.

	NOTE: Same as ReactJS Meteor applications will be bundled and minified however it may not has the map file by default However we don’t need it.

   ### Attacking Meteor.JS

	In Meteor.js based applications you just need your browser debugger and You can then try to call or search server methods () from your client.  
	An example to search js sources for ‘Meteor.call’.
	Just know we are interested in everyMeteor.call() function as this invokes real functions at the server using sockets.
	![meteror call functions](https://user-images.githubusercontent.com/25515871/178000804-94df1575-4bd4-4fc0-b7ff-bed0d1eb9df4.png)
	
	We can also Enumurate juicy informations. such as
		
		Meteor informations
			// Meteor version 
				Meteor.release;
			// Get settings.json public data (maybe juicy informations)
				Meteor.settings;
			// Production environment
				Meteor.isProduction;
			// Get current user informations
				Meteor.user();
			// Maybe get informations about other users
			Meteor.users.find().fetch();
			// Get meteor data
			this;

		Session variables

			// List session variables 
				Session.keys
			// Insert/Update variable 
				Session.set(‘theVariableName’, ‘newValue’);
			// Get value of a specific variable
				Session.get(‘theVariableName’);
			// Delete variable
				delete Session.keys.theVariableName;
		
		Collections 
			List collections data
				const subscriptions = _.map( Meteor.default_connection._subscriptions, sub => sub.name );
				_.each(subscriptions, sub => {
				    if ( Meteor.Collection.get(sub.toLowerCase()) ) {
					console.log(sub, Meteor.connection._stores[sub.toLowerCase()]._getCollection().find().fetch());
				    }
				});
				
			List local collections data

				_.forIn(this, (value, key) => {
				    if (this[key] && typeof this[key] === 'object' && this[key].hasOwnProperty('_collection') && this[key]._connection === null) {
					console.log(key, this[key].find().fetch());
				    };
				});

			Play with collections

				TheCollectionName.insert({ key: value, key2: value2 }); // Insert
				TheCollectionName.remove({ _id: theEntryId }); // Remove
				TheCollectionName.update({ _id: theEntryId }, {$set: { // Update
				    key: value,
				    key2: value2
				}});
				
		Templates

			List all templates

				Template.forEach(value => {
				    if (_.isObject(value)) {
					console.log(value.viewName);
				    }
				});

			Render a template

				Blaze.render(Template[templateName], document.body);

				Get template informations

				// Get template events list
				Template.TheTemplateName.__eventMaps;// Display the event code
				Template.TheTemplateName.__eventMaps.get('TheEvent');// Get template helpers list
				Template.TheTemplateName.__helpers;// Display the helper code
				Template.TheTemplateName.__helpers.get('TheHelper');// Get template creation callback
				Template.TheTemplateName._callbacks.created;// Get template rendering callback
				Template.TheTemplateName._callbacks.rendered;// Get template destruction callback
				Template.TheTemplateName._callbacks.destroyed;	

		Routes
			Get routes names and paths
			_.each(Router.routes, route => console.log(route.getName(), route.path()));
	
	#### NoSQL Injection at MeteorJS apps
	MeteorJS is not only a frontend library it also has its own backend engine to manage the communications. 
	Running the following commands at Chrome’s Devtools will help us to extract some useful information about the server and the working environment.
	server-side code is vulnerable to NoSQL Injections attacks https://resources.infosecinstitute.com/what-is-nosql-injection/
	
	
Ref :
[Javascript security Basics and understanding the web](https://www.youtube.com/watch?v=tKuFYD-rrCM)
[Meteor-security-tips](https://medium.com/meteor-js/meteor-security-tips-6fdc28560895)
[javascript-for-bug-bounty-hunters](https://bitthebyte.medium.com/javascript-for-bug-bounty-hunters-part-3-3b987f24ab27)


## Understanding Express (for backend - dev)
Updating Soon

# Understanding Ajax
Updating Soon

# Understanding Typescript
Updating Soon

# Bun - a fast new JavaScript runtime like Node.js or Deno. Explore the core features of Bun.js and how they might affect fullstack web developers in the future. 

	🔗 Resources

			Bun.js Announcement https://bun.sh
			Bun on Github https://github.com/Jarred-Sumner/bun
			How JavaScript Works https://youtu.be/FSs_JYwnAdI

## Understanding .Net framework (for backend - dev)
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


