# cheeseBlog-5
Link: https://www.hackxpert.com/cheeseBlog-5/index.php <br>

- In the cheeseblog types of challenges, our main goal is to change the posts that are made by other people. 
- In order to do that, you have to first login - **Username: test | Password: test**
- Then try editing any random post, this is where the challenge is.
- In most of the challenges there is a CSRF Token which checks the request, bypassing is the challenge.

## Exploitation
Fortunately this is an vulnerable challenge such that even if we don't change the CSRF token this will work since the webserver is not checking for the CSRF token in the first place.<br>

![image](https://user-images.githubusercontent.com/73820496/215308230-7b9c7849-1fa9-4915-95c5-7d7d9571ece7.png)


