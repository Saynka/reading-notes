# Access Control (ACL)

## Refrences

- https://www.youtube.com/watch?v=C4NP8Eon3cA
- https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html
- https://en.wikipedia.org/wiki/Role-based_access_control

## Review, Research, and Discussion

1. When is Basic Authorization used vs. Bearer Authorization?

- The Basic and Digest authentication schemes are dedicated to the authentication using a username and a secret (see RFC7616 and RFC7617). The Bearer authentication scheme is dedicated to the authentication using a token and is described by the RFC6750.

2. What does the JSON Web Token package do?

- is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed.

3. What considerations should we make when creating and storing a SECRET?

- Restrict API access and permissions. Never store unencrypted secrets in .git repositories. Avoid git add \* commands on git. Add sensitive files in .gitignore. Don't rely on code reviews to discover secrets

## Terms

- encryption - is the method by which information is converted into secret code that hides the information's true meaning. The science of encrypting and decrypting information is called cryptography. In computing, unencrypted data is also known as plaintext, and encrypted data is called ciphertext.

- token - is an Internet proposed standard for creating data with optional signature and/or optional encryption whose payload holds JSON that asserts some number of claims. The tokens are signed either using a private secret or a public/private key.

- bearer - is a cryptic string, usually generated by the server in response to a login request. The client must send this token in the Authorization header when making requests to protected resources:

- secret - The secret value contained within an authenticator.

- JSON Web Token - are an open, industry standard RFC 7519 method for representing claims securely between two parties.

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?

- web tokens make more sense i think i understood the concept jsut not actual practice of them

2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

- not sure right now lab 6 has me pissed off lol

3. What are you most excited about trying to implement or see how it works?

- front end to tie all this together and give a visual to the things we are doing in the back
