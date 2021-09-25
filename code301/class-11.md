# Authentication

## What is OAuth

1. What is OAuth?

    * OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential.
[source](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)

2. Give an example of what using OAuth would look like.

    * The most basic example of OAuth is when you want to log onto a website and it provides one or more options to log on using the login credentials of another website or service. You then click the link to the other website, which authenticates you, and the website you were originally connecting to logs you on using the authorization granted by the second website.

3. How does OAuth work? What are the steps that it takes to authenticate the user?

    1. The user's confirmed identity is provided by the first website, which connects to the second website on their behalf using OAuth.

    2. The second site creates a one-time token and a one-time secret that are only valid for the transaction and the people involved.

    3. The initiating user's client software receives this token and secret from the initial site.

    4. The request token and secret are presented to the authorization provider by the client's software (which may or may not be the second site).

    5. The client may be requested to authenticate if they haven't already done so with the authorisation provider. The consumer is requested to approve the authorisation transaction to the second website after authentication.

    6. At the first website, the user approves (or their program quietly approves) a specific transaction type.

    7. The user is given an access token that has been approved (note that it is no longer a request token).

    8. The user gives the approved access token to the first website.

    9. The first website gives the access token to the second website as proof of authentication on behalf of the user.

    10. The second website lets the first website access their site on behalf of the user.

    11. The user sees a successfully completed transaction occurring.

4. What is OpenID?
    * OpenID is about authentication. rather than having multiple logins for multiple websites, OpenID would serve as a single sign-in, vouching for the identities of users.

    ---

## Authorization and Authentication flows

[source](https://auth0.com/docs/authorization/flows)

1. What is the difference between authorization and authentication?

    * Authentication confirms that users are who they say they are. Authorization gives those users permission to access a resource.

2. What is Authorization Code Flow?

    * Authorization code flow is used to obtain an access token to authorize API requests

3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?

    * The Authorization Code Flow + PKCE is an OpenId Connect flow specifically designed to authenticate native or mobile application users. This flow is considered best practice when using Single Page Apps (SPA) or Mobile Apps. PKCE, pronounced “pixy” is an acronym for Proof Key for Code Exchange.

4. What is Implicit Flow with Form Post?

    * The implicit flow is a browser only flow. It is less secure than the Code Flow since it doesn't authenticate the client. But it is still a useful flow in web applications that need access tokens and cannot make use of a backend.

5. What is Client Credentials Flow?

    * The Client Credentials flow is a server to server flow.

6. What is Device Authorization Flow?

    * is an OAuth 2.0 extension that enables devices with no browser or limited input capability to obtain an access token.

7. What is Resource Owner Password Flow?

    * The Resource Owner Password Credentials flow allows exchanging the username and password of a user for an access token.

## Things I want to know more about

* Nothing so far
