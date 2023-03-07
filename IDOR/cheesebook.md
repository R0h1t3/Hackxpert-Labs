# chessbook
Link: https://hackxpert.com/cheesebook/<br>

![image](https://user-images.githubusercontent.com/73820496/223347318-9186ac1f-3bd5-4060-8233-e1c377a558d3.png)

### Given Information:
You have a user;
admin/test

and you can self-register for cheesebook
Can you find the IDOR?

There are least 4 BAC issues, can you find them <br>

What are we waiting for, let's hack!


## Exploitaion
So from the given information we know that: <br>
- There is the highest user - admin who can view user data and have control over all the post and their functions<br>
- Then there is our normal user who can create, edit and delete his own posts.

So the possible IDORs in this  situation are horizontal - changing other user's post, ability to access admin functions as a normal user.<br>
In order to achieve this we will changing the URLs while performing the attack.<br>


Before getting into the exploitaion part of it, there are 3 users here used for testing:<br>
- admin - highest privilage
- user_a - Attacker
- user_v - Victim

## Editing other user's posts
- Initially open user_a account in one browser and user_v account in another browser.<br>

![image](https://user-images.githubusercontent.com/73820496/223381993-3f6c7aba-cd5d-4c0a-8478-b2de10c4101e.png)<br>

- Then click on "Create a new post", create a post in user_v and publish the post.<br>

![image](https://user-images.githubusercontent.com/73820496/223382374-ef3ef958-784a-430a-b1eb-62f1182442bb.png)<br>

- Click on the edit option on the screen to edit the post.<br>

![image](https://user-images.githubusercontent.com/73820496/223383337-5ddf60c4-1c13-4561-8c0f-53ac27ebaeb8.png)<br>

- Now just copy and paste the URL in the browser winndow with which you havve logged in with user_a's account. And you will be able to edit the post even though you haven't created it. This is an IDOR(1).<br>

## Deleting other user's posts
- Now in the user panel of the user_v's account you can see 2 options - Edit and Delete. This time let's play with the Delete option.
- Now, don't left-click on the delete option but right-click on it and copy the Delete link to delete user_v's post.
- And the paste in the user_a's browser window.
- After that when you revisit the user_v's account and refresh it, the post will be deleted.This is an IDOR(2).<br>

![image](https://user-images.githubusercontent.com/73820496/223384855-58cb3fbb-7bc9-4572-92dc-b480ba79af09.png)<br>

## Accessing admin's page
- Now we will try to get into the admin account. Instead of user_v, login with admin account in the  browser window.

![image](https://user-images.githubusercontent.com/73820496/223386636-4c8a1793-910b-4dd4-8030-a3ae6dad712b.png)<br>

- Now copy the admin panel's URL into the browser of the user_a's browser window. This will open up the admin's panel in the user_a's logged in page. This is an IDOR(3).<br>

![image](https://user-images.githubusercontent.com/73820496/223387204-79035326-ecaf-41f3-89f2-73f192688a83.png)<br>

Then we can do the same to "View users" in the user_a's window - IDOR(4). We can also create new users with the admin option of "Create new user" - IDOR(5) and "Create new post" as admin in the user_a logged in browser window - IDOR(6). 

**Note** - Deleting/Editing of other user's posting can be done by changing the ID of each post that is created. Since all the posts are cronological order in this platform, we can easily delete it. Try it on your own.



