# 0Auth 
OAuth, which stands for “Open Authorization,” allows third-party services to exchange 
your information without you having to give away your password.

OpenID Connect, OAuth 2.0, and MSAL to make sign-in fully secure

Redirect_uri or reply URL, is used when a Resource Owner grants Authorization to the OAuth Client. 
In simple term. 
is the location where the authorization server sends the user once the app has been successfully authorized and granted an authorization code or access token.

## Find OAuth Misconfiguration in SSO(Single Sign-On(SSO) Feature
(For example Log in with Github, Microsfot, Google, Facebook etc)


## How to exploit OAuth Misconfiguration in SSO feature:
1. OAuth token stealing : Changing redirect_uri to attacker.com([Use IDN Homograph](https://hackerone.com/reports/861940) or common bypasses).
  
2. OAuth Token Re-use.

  To get oAuth tokens manually, 
   
    open Chrome dev tools (Ctrl + Shift +I ), head over to the Network tab, 
    follow any SSO feature account(in video we have twitch account), 
    inspect the http post request (gql) , 
    and check the 'Authorization' header for the token. 
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

## Potential impact re oAuth token leakage.

Attack will result in leaking the user's OAuth code to an attacker-controlled domain name giving them unauthorized access to properties and data of the user's account.


## Referance: To understand 0auth: 

1.[OAuth - Something to do with Autherization.](https://youtu.be/t4-416mg6iU)
2.[OAuth terminology and OAuth flow explain ](https://youtu.be/3pZ3Nh8tgTE)
3.[daffainfo](https://github.com/daffainfo)
4.[six2dez](https://pentestbook.six2dez.com/)


