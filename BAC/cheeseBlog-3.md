# cheeseBlog-3
Link: https://www.hackxpert.com/cheeseBlog-3<br>

![image](https://user-images.githubusercontent.com/73820496/218440866-1a25f9d6-bee6-4de1-bdf9-6100a795fe67.png)<br>

So the motive of this challenge is to find a functionality that an unauthenicated user can execute as same as the logged in user. Let's go

## Exploitation 
- So in order to find the functionalities for an an unauthenicated user to execute, we need to understand what are the functionalities that are available when logged in.
- When logged in a as test user we can see 3 functionalities.
  - Edit
  - Create
  - Delete<br>

![image](https://user-images.githubusercontent.com/73820496/218441562-0312e158-edca-4638-b2b6-e51bab943c72.png)<br>

- Let's Apply some logic:
  - We can't delete a post with authentication, capture the request and try to delete an already deleted post since only one is here. But you can try this if you have multiple posts to go on with.
  - We can try to edit a post. <br>
  
    ![image](https://user-images.githubusercontent.com/73820496/218442106-57c99948-64ac-4b4d-b560-c0c959d3a3cf.png)<br>
    When we try that, it won't work with an unauthenicated user because there is **id** parameter that is required to edit posts. So this cannot be exploited.<br>
 
  - We can try to create a new post.<br>
  
    ![image](https://user-images.githubusercontent.com/73820496/218442475-ce3074e7-3eb0-4b69-93c7-8529b0f82cc6.png)<br>
    Unlike the edit option there is no parameter requirement so this works even with unauthenticated user.<br>
 
 Hence exploited.
