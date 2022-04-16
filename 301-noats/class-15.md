# Class 03 *Reading Notes*

## O Auth

What is OAuth?

- OAuth is an open-standard authorization protocol that allows authenticated access to specific assests

Give an example of what using OAuth would look like.

- Logging in to unrelated sites through a personal Google account is an example of O Auth

How does OAuth work? What are the steps that it takes to authenticate the user?

- O auth works by allowing a use to log into 3rd party sites after authenting through a particular unrelated service.
 The steps are as follows:

1. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
2. The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
3. The first site gives this token and secret to the initiating user’s client software.
4. The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
5. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the  authorization transaction to the second website.
6. The user approves (or their software silently approves) a particular transaction type at the first website.
7. The user is given an approved access token (notice it’s no longer a request token).
8. The user gives the approved access token to the first website.
9. The first website gives the access token to the second website as proof of authentication on behalf of the user.
10. The second website lets the first website access their site on behalf of the user.

What is OpenID?

## Authorization and Authentication flows

What is the difference between authorization and authentication?

- Authentication is the process of a user/subject proving its ownership whereas a uthorization is the process of letting a subject access resources after a successful authentication

What is Authorization Code Flow?

- The user clicks Login within the regular web application.

- Auth0's SDK redirects the user to the Auth0 Authorization Server (/authorize endpoint)
- Your Auth0 Authorization Server redirects the user to the login and authorization prompt
- The user authenticates using one of the configured login options
- Your Auth0 Authorization Server redirects the user back to the application with an authorization code, which is good for one use.
- Auth0's SDK sends this code to the Auth0 Authorization Server (/oauth/token endpoint) along with the application's Client ID and Client Secret.
- Your Auth0 Authorization Server verifies the code, Client ID, and Client Secret.
- Your Auth0 Authorization Server responds with an ID Token and Access Token (and optionally, a Refresh Token).
- Your application can use the Access Token to call an API to access information about the user.
- The API responds with requested data

What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?

- The user clicks Login within the application.

- Auth0's SDK creates a cryptographically-random code_verifier and from this generates a code_challenge.
- Auth0's SDK redirects the user to the Auth0 Authorization Server (/authorize endpoint) along with the code_challenge.
- Your Auth0 Authorization Server redirects the user to the login and authorization prompt.
- The user authenticates using one of the configured login options and may see a consent page listing the permissions Auth0 will give to the application.
- Your Auth0 Authorization Server stores the code_challenge and redirects the user back to the application with an authorization code, which is good for one use.
- Auth0's SDK sends this code and the code_verifier (created in step 2) to the Auth0 Authorization Server (/oauth/token endpoint).
- Your Auth0 Authorization Server verifies the code_challenge and code_verifier.
- Your Auth0 Authorization Server responds with an ID Token and Access Token (and optionally, a Refresh Token).
- Your application can use the Access Token to call an API to access information about the user.
- The API responds with requested data.

What is Implicit Flow with Form Post?

- Implicit Flow is an alternative in which OAuth 2.0 provides the Implicit Flow, which is intended for Public Clients, or applications which are unable to securely store Client Secrets.

- The user clicks Login in the app.
- Auth0's SDK redirects the user to the Auth0 Authorization Server (/authorize endpoint) passing along a response_type parameter of id_token that indicates the type of requested credential. It also passes along a response_mode parameter of form_post to ensure security.
- Your Auth0 Authorization Server redirects the user to the login and authorization prompt.
- The user authenticates using one of the configured login options and may see a consent page listing the permissions Auth0 will give to the app.
- Your Auth0 Authorization Server redirects the user back to the app with an ID Token.

What is Client Credentials Flow?

- Client Credentials Flow allows the system authenticates and authorizes the app rather than a user

What is Device Authorization Flow?

- Device Authorization Flow prompts the user's device asks the user to go to a link authorize the device.

What is Resource Owner Password Flow?

- Resource Owner Password Flow requests that users provide credentials such as username and password
