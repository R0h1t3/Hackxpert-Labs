# BAC Checklist
## Conditions for BAC:
- [ ]  We need to be able to create different users OR need to be assigned different
users
- [ ]  The users need to be of different privilege levels if we want to test for
vertical privilege escalation. For example an admin and a normal user
- [ ]  There need to be functions that our low-privilege user is not authorised to
execute, either with the given data or at all

--- 

- [ ]  Sometimes if the user can not execute the function, front end button is just
hidden<br>
 The Javascript function might still work<br>
 We can execute the JavaScript function via the developer console
- [ ]  We can just log in as admin and copy & paste the URL of the functions we
should not execute as low priv user
- [ ]  We can execute the request as admin and capture it in burp, then send
to repeater and paste in low priv user authorization header
