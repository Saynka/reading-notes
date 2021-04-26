# Bearer Authorization

## refrences

- https://www.youtube.com/watch?v=926mknSW9Lo
- https://jwt.io/introduction/
- https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure
- https://www.npmjs.com/package/jsonwebtoken

## Review, Research, and Discussion

1. Write the following steps in the correct order:

- Register your application to get a client_id and client_secret
- Ask the client if they want to sign in via a third party
- Redirect to a third party authentication endpoint
- Receive authorization code
- Make a request to the access token endpoint
- Receive access token
- Make a request to a third-party API endpoint

2. What can you do with an authorization code?

- The only thing you can do with the authorization code is to make a request to get an access token.

3. What can you do with an access token?

- are the thing that applications use to make API requests on behalf of a user.

4. What’s a benefit of using OAuth instead of your own basic authentication?

- Managing an API program without access tokens can provide you with less control, and there is zero chance of implementing an access token strategy with Basic authentication.J

## Term

- Client ID - represents a unique browser/device and is created and assigned by Universal Analytics cookie \_ga. Client ID is assigned to each unique user of your website.

- Client Secret - is a secret known only to your application and the authorization server. It protects your resources by only granting tokens to authorized requestors. Protect your client secrets and never include them in mobile or browser-based apps.

- Authentication Endpoint - Endpoint authentication is a security mechanism designed to ensure that only authorized devices can connect to a given network, site or service.

- Access Token Endpoint - A token endpoint is an HTTP endpoint that micropub clients can use to obtain an access token given an authorization code.

- API Endpoint - is the point of entry in a communication channel when two systems are interacting. It refers to touchpoints of the communication between an API and a server.

- Authorization Code - is an alphanumeric password that authorizes its user to purchase, sell or transfer items, or to enter information into a security-protected space

- Access Token - are the thing that applications use to make API requests on behalf of a user.

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?

- basic apir modulazation with middleware and basic authentication

2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

- more about the modularity of how to properly put things in the flow

3. What are you most excited about trying to implement or see how it works?

- how all this back end looks in the front end
