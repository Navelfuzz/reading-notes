# CF301 Reading Notes Class 14: Diversity & Inclusion in the Tech Industry

## Reading

[What is OAuth](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)

### Questions

1. What is OAuth?
2. Give an example of what using OAuth would look like.
3. How does OAuth work? What are the steps that it takes to authenticate the user?
4. What is OpenID?

### Answers

1. OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential.
2. The simplest example of OAuth is when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon. You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permission gained from the second website.
3. The user then initiates a feature/transaction that needs to access another unrelated site or service. The following happens (greatly simplified):
    1. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
    2. The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
    3. The first site gives this token and secret to the initiating user’s client software.
    4. The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
    5. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
    6. The user approves (or their software silently approves) a particular transaction type at the first website.
    7. The user is given an approved access token (notice it’s no longer a request token).
    8. The user gives the approved access token to the first website.
    9. The first website gives the access token to the second website as proof of authentication on behalf of the user.
    10. The second website lets the first website access their site on behalf of the user.
    11. The user sees a successfully completed transaction occurring.
    12. OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).
4. OpenID is an open standard and decentralized authentication protocol that is built on top of OAuth. It allows users to use their existing accounts to authenticate themselves to multiple websites or applications without the need for separate usernames and passwords. OpenID provides a way for users to prove their identity to relying parties (websites or applications) using an authentication token issued by an OpenID provider (such as Google, Facebook, or other identity providers). It simplifies the authentication process by leveraging OAuth's authorization capabilities while also adding identity verification features.

[Authorization and Authentication flows](https://auth0.com/docs/get-started/authentication-and-authorization-flow)

### Questions

1. What is the difference between authorization and authentication?
2. What is Authorization Code Flow?
3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
4. What is Implicit Flow with Form Post?
5. What is Client Credentials Flow?
6. What is Device Authorization Flow?
7. What is Resource Owner Password Flow?

### Answers

1. Authentication refers to the process of verifying the identity of a user or entity. Authorization deals in granting or denying permissions and access rights.
2. Authorization Code Flow is an OAuth 2.0 flow that is commonly used for server-side web applications and native/mobile applications. The flow involves the following steps:
    1. The client application initiates the flow by redirecting the user to the authorization server.
    2. The user authenticates with the authorization server.
    3. After successful authentication, the authorization server redirects the user back to the client application with an authorization code.
    4. The client application exchanges the authorization code with the authorization server for an access token.
    5. The authorization server verifies the code and issues an access token to the client application.
    6. The client application can then use the access token to make authorized API requests on behalf of the user.
3. Authorization Code Flow with Proof Key for Code Exchange (PKCE) is an extension to the Authorization Code Flow that adds an extra layer of security for public clients, such as native or mobile applications. It mitigates the risk of authorization code interception attacks. The main difference is that PKCE requires the client to generate a random secret (known as the code verifier) and create a derived value (known as the code challenge) from it. The code challenge is sent to the authorization server, which associates it with the authorization code. When exchanging the authorization code for an access token, the client also sends the original code verifier. The authorization server verifies the code challenge and code verifier match, providing enhanced security.
4. Implicit Flow with Form Post is an older OAuth 2.0 flow primarily used by single-page applications (SPAs) that run in a web browser. In this flow:
    1. The client application initiates the flow by redirecting the user to the authorization server.
    2. The user authenticates with the authorization server.
    3. After successful authentication, the authorization server redirects the user back to the client application, including the access token and other response parameters in the URL fragment.
    4. The client application receives the token by extracting it from the URL fragment using JavaScript.
    5. The client application can then use the access token to make authorized API requests.
5. Client Credentials Flow is an OAuth 2.0 flow used when the client application (typically a server or backend service) wants to authenticate itself rather than an end-user. It is suitable for scenarios where the client application needs to access protected resources under its own authorization. The flow involves the client application directly exchanging its credentials (client ID and client secret) with the authorization server for an access token. The access token can then be used to access protected resources on behalf of the client application.
6. Device Authorization Flow (also known as Device Flow) is an OAuth 2.0 flow designed for devices with limited input capabilities, such as smart TVs, gaming consoles, or IoT devices. In this flow:
    1. The device initiates the flow by displaying a user code and instructing the user to visit a specific authorization URL on another device.
    2. The user visits the URL on a separate device (e.g., smartphone or computer) and enters the user code provided by the device.
    3. The user is then prompted to authenticate with the authorization server.
    4. After successful authentication, the authorization server issues an access token to the device.
    5. The device can then use the access token to access protected resources.
7. Resource Owner Password Flow (also known as Password Grant Type) is an OAuth 2.0 flow where the client application directly requests the user's username and password and exchanges them for an access token. This flow is typically used when the client application is highly trusted and there is a direct relationship between the client application and the user. It should be used with caution, as it requires the client application to handle and securely store user credentials, which may introduce additional security risks.
