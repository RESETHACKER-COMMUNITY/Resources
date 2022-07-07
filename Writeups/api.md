![FW_LgLZXwAIZYF1](https://user-images.githubusercontent.com/25515871/177757917-a1691979-a1ae-4c68-b02a-b5c69ac098e5.jpg)

[What is an API? by Katie Paxton-Fear](https://twitter.com/@InsiderPhD)
     
   - Tl;dr
   
      - Software designed to talk to other software
      - But still has to allow humans to debug it
      - Usually outputs some structured plain text e.g. JSON or XML
      - JSON {"key" : "value" ...}
      - XML <object><key>value</key>...

  - Types of APIs (what kinds of APIs are out there>?
     
      - External APIs APIs are designed to be public but are designed for use by a single org
      - Public APIs for developers to add integration from their app to an existing service
      - Internal APIs completely inaccessible from outside an organisation, may be aggregated to an external API

  - API use cases
       
      - Single interface, many devices
      - Many tools allow APIs to be automatically created from a database or framework
      - Language independent even if you change later an API will always work

  - API terminology
      
      - Endpoint - a URL which does something e.g. doesn't 404
      - Parameter - the data you input into an API
      - API call - when an app makes a request to the API it is calling it
      - Stateless - the server doesn't know anything about the client's state we need to tell it each time
      - API keys - provides authentication to APIs - when you log in you are given an API key which you send with all future requests
      - CORS - stands for cross-origin resource sharing, can an API endpoint be accessed from another domain?
 
  - RESTful APIs
      
      - API standard for the web enforced consistency. between APIs based on CRUD and the URL
      - Create a new resource -> POST /api/resource
      - Read an existing resource -> GET /api/resource/1
      - Read all resources -> GET /api/resource/
      - Update a resource -> PUT /api/resource/1
      - Delete a resource -> DELEETE /api/resource/1
      - Very few APIs enforce true RESTful APIs so the term usually refers to APIs with this structure

  - Resources can be anything
      
      - Depends on the business logic
      - Forum: posts, users, replies
      - Twitter: tweers, users, bookmarks
      - Twitter and forums are similar but endpoints will be custom + use different terminology
