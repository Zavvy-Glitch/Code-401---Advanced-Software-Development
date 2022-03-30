# Bearer Authorization

## JWT (JSON Web Token)
   - What is it?
        - JWT is an open standard(anyone can use it) defining a compact and self-contained way to securily transmit information.
        - JWT's can be signed with a secret(HMAC algorithm) or public/private key pair using RSA or ECDSA
   - When should you use JWT's?
        - Information Exhange: when you need to securely transmit information between parties.
        - Authorization: when you only need a single user to access specific routes, services, content, resources.
   - JWT Structure:
        - Header: consists of 2 parts (typically) : the type of token and the signing algorithm
             - ```javascript
               {
                "alg":"HS256,
                "typ":"JWT"
               } 
               ``` 
        - Payload: consists of the claims. Claims are statements about an entity(user) and other additional data.
            - Three Types:
            - Registered
            - Public
            - Private 
        - Signature: will take an encoded header, the encoded payload, a secret, which ever algorithm specified in the header, and then sign it.
            - This is used to verify the message sent wasn't changed in transmission and, in the case of tokens signed with a private party it can verify the sender of the JWT to ensure they are who they say they are.

Steps:
    - Ask the client if they want to sign in via a third party
    - Make a request to a third-party API endpoint
    - Register your application to get a client_id and client_secret
    - Redirect to a third party authentication endpoint
    - Make a request to the access token endpoint
    - Receive access token
    - Receive authorization code
    
    TERMS                   | Definitions
    ----------------------- | -----------
    Client ID               | The Client ID (cid) is a unique identifier for a browser–device pair 
    ----------------------- | -----------            
    Client Secret           | A client secret is a secret known only to your application and the authorization server. It protects your resources by only granting tokens to authorized requestors.
    ----------------------- | -----------
    Authentication Endpoint | Endpoint authentication is a security mechanism designed to ensure that only authorized devices can connect to a given network, site or service.
    ----------------------- | -----------
    Access Token Endpoint   | The token endpoint is where apps make a request to get an access token for a user
    ----------------------- | -----------
    API Endpoint            | An endpoint is one end of a communication channel. When an API interacts with another system, the touchpoints of this communication are considered endpoints.
    ----------------------- | -----------
    Authorization Code      | Auth0 Authorization Server redirects the user back to the application with an authorization code , which is good for one use. Auth0's SDK sends this code to the Auth0 Authorization Server ( /oauth/token endpoint) along with the application's Client ID and Client Secret.
    ----------------------- | -----------
    Access Token            | Access tokens are used in token-based authentication to allow an application to access an API
    

   
    
    
    
