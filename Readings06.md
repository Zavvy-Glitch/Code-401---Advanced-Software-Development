# Authentication

## Basic Access Authentication
    - A method for an HTTP user using a username / password to make a request.
    - Header field Authorization: Basic <credentials> (Base64)
    - Simplest technique for controlling access to web applications / resources.
        - Does not require cookies, session identifiers, or login pages.

### Cheat Sheet (Implementing a Proper Password)
    - Password length:
        - Minimum length should be enforced.
        - Maximum length should not be set too low. Commonly allowed up to 64 characters.
    - Allow usage of all characters including unicode and whitespace. No composition rules limiting the type of characters used ina password
    - Implement a Credential rotation when a password leak occurs, or when compromise has been identified.
    - Implement Secure Password Recovery Mechanism
    - Store Passwords in a Secure Fashion
    - Compare Password Hashes Using Safe Functions
    - Implement Change Password Feature
        - Verify current password before allowing access to change password.
### bcrypt
    - password hashing function
    - based on Blowfish cipher
        -  The input to the bcrypt function is the password string (up to 72 bytes), a numeric cost, and a 16-byte (128-bit) salt value. The salt is typically a random value. The bcrypt function uses these inputs to compute a 24-byte (192-bit) hash.
