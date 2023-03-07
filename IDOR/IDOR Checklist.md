### IDOR

**Conditions for IDOR:**

- [ ]  An object identifier exists in the request, either as a GET or POST parameter
- [ ]  A Broken Access Control issue has to exist to allow the user access to data
they should not be able to access

- [ ]  Open 2 browsers and Try copying the URLs from one to another to check whether they work
- [ ]  Try changing the ID(or any similar parameter in the request)
- [ ]  Execute JavaScript in the developer console

**Using Burp Suite:**

- [ ]  In the repeater - replace the authentication methods that are expected by
the server with some valid authentication tokens.
- [ ]  JWT in the authorisation header might need to be replaced
- [ ]  Replace Session cookies with relatively similar ones

### Semi-Automated way using Burp

- [ ]  Use Authorize for testing
- [ ]  Use Match and replace for testing
