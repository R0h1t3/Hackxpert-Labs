# CSRF Checklist
- [ ] Check if the token is present on any form it should be - ONLY Create, Update and Delete forms should have CSRF tokens
- [ ] Remove the CSRF Token
- [ ] Replace the CSRF Token with a Random Value
- [ ] Replace the CSRF Token with a Token of the Same kind(Regex)
- [ ] Use previously used CSRF Token
- [ ] Leave CSRF Parameter’s value empty
- [ ] See if you can request a CSRF by executing the call manually and using that token for the request
- [ ] Change the Request Method Used Burp (Reference: [20.md](https://github.com/R0h1t3/Hackxpert-Labs/blob/main/CSRF/20.md))

# Useful Links:
- https://security.love/CSRF-PoC-Genorator/
- https://portswigger.net/burp/documentation/desktop/functions/generate-csrf-poc
- https://owasp.org/www-community/attacks/csrf
- https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html

