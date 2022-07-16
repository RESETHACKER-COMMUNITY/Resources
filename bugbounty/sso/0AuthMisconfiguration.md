
## Find OAuth Misconfiguration in SSO(Single Sign-On(SSO) Feature - under development
(For example Log in with Github, Microsfot, Google, Facebook etc)

# 0Auth & 0Auth2 
OAuth, which stands for “Open Authorization,” allows third-party services to exchange 
your information without you having to give away your password.

  
    A little bit of theory:
    
      client_id=
      Redirect_uri or reply URL, is used when a Resource Owner grants Authorization to the OAuth Client. 
    In simple term. 
    is the location where the authorization server sends the user once the app has been successfully authorized and granted an authorization code or access token.
    
    state=?ReturnUrl=
    UtmTerm=null
    csrf-request-id=
    __provider__=google
    dnsamr=true
    ru
    
    flowName=GeneralOAuthFlow
    
      response_type = code is server-side auth flow, should be used when possible, more secure than response_type = token. 
      Provider returns 'code' with User's user-agent and Client sends along with client's credentials the code to obtain 'access_token'. 
      Callback when user is redirected looks like site.com/oauth/callback?code=AQCOtAVov1Cu316rpqPfs-8nDb-jJEiF7aex9n05e2dq3oiXlDwubVoC8VEGNq10rSkyyFb3wKbtZh6xpgG59FsAMMSjIAr613Ly1usZ47jPqADzbDyVuotFaRiQux3g6Ut84nmAf9j-KEvsX0bEPH_aCekLNJ1QAnjpls0SL9ZSK-yw1wPQWQsBhbfMPNJ_LqI

    Reminder, OAuth is all about authorization, not authentication. 
    What's the difference, you might ask. 
    OAuth just gives to Client access to User's resources on Provider.
    But very often Client authenticates you by 'profile_info' resource, thus we can call it authentication framework either.
    OpenID Connect, OAuth 2.0, and MSAL to make sign-in fully secure.
    

## Website can impliments 0Auth for users in two ways either login with OAuth Provider or both.
    
    login with OAuth Provider + ability to add OAuth Provider logins in settings

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
      
      1. Use Burp "find" option in order to find the parameters 
      such as url, red, redirect, redir, orgin, dest, targetURL, checkout_URL etc
      2. Check the value of these parameters which can contain a URL.
      3. Change open redirection for 0auth functionality.
      4. Change the URL value to www.example.com check if gets redirected or not.
      (Most cases it's not that easy due to Security headers such as Referrer Policy strict-origin-when-cross-origin.)
      5. Check if same secret code request can be used multiple times.

3. Check for Broken Authentication and pre-Authentication.
4. 

## Potential impact 

Attack will result in *leaking the user's OAuth code* to an attacker-controlled domain name giving them unauthorized access to properties and data of the user's account.


## Referance: To understand 0auth: 

0.[The OAuth 2.0 Authorization Framework draft-ietf-oauth-v2-27](https://datatracker.ietf.org/doc/html/draft-ietf-oauth-v2-27#section-10.10)

1.[OAuth - What is OAuth really all about](https://youtu.be/t4-416mg6iU)

2.[OAuth terminology and OAuth flow explain ](https://youtu.be/3pZ3Nh8tgTE)

3.[daffainfo - resources to hunt](https://github.com/daffainfo)

4.[six2dez- resources to hunt](https://pentestbook.six2dez.com/)

5.[OAuth 2 support- flow,cheetsheet, Extra](https://sakurity.com/oauth)

6.[Account hijacking using "dirty dancing" in sign-in OAuth-flows](https://labs.detectify.com/2022/07/06/account-hijacking-using-dirty-dancing-in-sign-in-oauth-flows/)

