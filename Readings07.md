# Bearer Authorization

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
    
 ## Preview
    - Which 3 things had you heard about previously and now have better clarity on?
      - Payload
      - Signature
      - Bearer
    - Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
      - Ways to secure tokens
      - How hash-ing works
      - How does the front end compare information to authorize a user?
   
    
    
    
