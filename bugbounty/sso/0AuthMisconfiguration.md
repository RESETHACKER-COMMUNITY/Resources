# 0Auth 
OAuth, which stands for “Open Authorization,” allows third-party services to exchange 
your information without you having to give away your password.

OpenID Connect, OAuth 2.0, and MSAL to make sign-in fully secure

## Find OAuth Misconfiguration in SSO(Single Sign-On(SSO) Feature
(For example Log in with Github, Microsfot, Google, Facebook etc)

Credit: https://github.com/daffainfo
## How to exploit OAuth Misconfiguration in SSO feature:
1. OAuth token stealing :
  To get oAuth tokens manually, 
    
    open Chrome dev tools (Ctrl + Shift +I ), head over to the Network tab, 
    follow any twitch account, inspect the http post request (gql) , 
    and check the Authorization header for the token. 
    Copy the whole text after OAuth.

![get oauth](https://user-images.githubusercontent.com/75003671/112411090-45f09d00-8d57-11eb-8922-188876cc00ad.gif)

2. Test 0auth login functionality for [Open Redirect](https://pentestbook.six2dez.com/enumeration/web/open-redirects)
  
  Eg:
      
      1. Use Burp "find" option in order to find the parameters such as url, red, redirect, redir, orgin, dest, targetURL, checkout_URL etc
	    2. Check the value of these parameters which can contain a URL.
	    3. Change open redirection for 0auth functionality.
	    4. Change the URL value to www.chintan.com and check if gets redirected or not.
	    5. Check if same secret code request can be used multiple times.

3. Check for Broken Authentication and pre-Authentication.
4. 
## Impact 


## Referance: To understand 0auth: 

1.[OAuth - Something to do with Autherization.](https://youtu.be/t4-416mg6iU)
2.[OAuth terminology and OAuth flow explain ](https://youtu.be/3pZ3Nh8tgTE)


