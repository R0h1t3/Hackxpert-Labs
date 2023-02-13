# CAPTCHA Bypass Checklist
- [ ]  Simply not sending the captcha along with the request or leaving it empty. The developers might have forgotten to implement the verification.
- [ ]  Changing the request from GET to POST and vice versa while leaving the captcha out of the request
- [ ]  Trying to re-use captcha tokens as this might enable an attacker to simply request a captcha code and enter it along with every request (The captcha is not request-bound)
- [ ]  Trying to predict the next captcha code
- [ ]  Using an OCR to solve them. This is why the captcha is not as good as they used to be, OCR’s can solve the text-based captchas
