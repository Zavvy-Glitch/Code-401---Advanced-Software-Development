# Application State with Redux

- What are the advantages of storing tokens in "Cookies" vs "Local Storage"?
  - It's just less convenient for the attacker because they can't read the content of the token although they rarely have to. It might also be more advantageous for the attacker to attack using victim's browser (by just sending that HTTP Request) rather than using the attacker's machine. [src: DEV](https://dev.to/cotter/localstorage-vs-cookies-all-you-need-to-know-about-storing-jwt-tokens-securely-in-the-front-end-15id)
- Explain 3rd party cookies
  - Third-party cookies are created by domains that are not the website (or domain) that you are visiting. These are usually used for online-advertising purposes and placed on a website through adding scripts or tags. A third-party cookie is accessible on any website that loads the third-party server's code. [src: CookiePro](https://www.cookiepro.com/knowledge/what-is-a-third-party-cookie/#:~:text=Third%2Dparty%20cookies%20are%20created,the%20third%2Dparty%20server's%20code.)
- How do pixel tags work? 
  - Pixel tags, or web beacons as they are also known, attach to a browser and collect information about an anonymous user's movements on the Internet. These little beacons allow sites to provide users with ads for services and products that are relevant to them. 

## Terminology

|Cookies|Authorization|Access Control|Conditional Rendering|
|-------|-------------|--------------|---------------------|
|Cookies are text files with small pieces of data — like a username and password — that are used to identify your computer as you use a computer network. Specific cookies known as HTTP cookies are used to identify specific users and improve your web browsing experience|Authorization refers to the process of verifying what a user has access to. While often used interchangeably with authentication, authorization represents a fundamentally different function|The idea of assigning permissions to users based on their role within an organization. It offers a simple, manageable approach to access management that is less prone to error than assigning permissions to users individually|A term to describe the ability to render different user interface (UI) markup if a condition is true or false. In React, it allows us to render different elements or components based on a condition|
