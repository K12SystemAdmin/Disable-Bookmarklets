# Disable-Bookmarklets
-------------------------------------------------------------------------------------------------------------------------------------

### Bookmarklets or bookmarks are what most students use to bypass school restrictions. This can include disabling extensions that are installed on school computers or browsers. By utilizing bookmarklets or bookmarks, students can bypass the limitations imposed by certain extensions that might block or restrict access to specific websites or content. They can simply click on a bookmark or bookmarklet that disables these extensions temporarily, granting them access to restricted resources without being detected. However, it's important to remember that such actions go against the school's policies and are considered non-ethical. It's crucial for students to respect and abide by the rules set by their educational institution to maintain a safe and fair learning environment for everyone.

-------------------------------------------------------------------------------------------------------------------------------------

**_Here is an image for reference..._**

![image](https://github.com/K12SystemAdmin/Disable-Bookmarklets/assets/133791743/8d5cd597-6e2a-4b8a-9a13-7e9909f962d9)
-------------------------------------------------------------------------------------------------------------------------------------

So here is an easy way to patch this and disable from students from using Bookmarklets **(Please keep in mind that you need Google Admin Console Access for this to work :-)**

-------------------------------------------------------------------------------------------------------------------------------------
## Step 1 - GAC Access (Google Admin Console)

Head on to Google [Admin](https://admin.google.com/) and from there you will see **Devices** > **Chrome** > **Settings** > and to **Users & Browsers** _(This may or may not show up differently for you)_

*__(This is what you should see)__*

![image](https://github.com/K12SystemAdmin/Disable-Bookmarklets/assets/133791743/1dd1531e-1699-49ea-ace8-48297754dafb)

-------------------------------------------------------------------------------------------------------------------------------------
## Step 2 - URL/Wildcard Blocking

Go to where is says **Url Blocking** and there should be 2 sections. One for _**Blocked URL's**_ and _**Blocked URL Exceptions**_. and what you want to put for both of them is to block this -> _**javascript://***_ | What this will do is it will prevent from any Javascript trying to run because you are blocking a _**Wildcard**_, which means it will continue to block Javascript for all of the code trying to be executed

(This is what it should look like)

![image](https://github.com/K12SystemAdmin/Disable-Bookmarklets/assets/133791743/86e6ca41-ab88-455a-acc2-0f94412226b0)

-------------------------------------------------------------------------------------------------------------------------------------
## Step 3 - Testing/Finishing Results

Once you have saved the changes in GAC, go to _**chrome://policy**_ and scroll over to **URLBlocklist** _(or just search the policy using CTRL + F)_ 

And once you see _**javascript://***_ on that list that means you got it! So now you can test a [bookmarklet](https://github.com/search?q=bookmarklets&type=repositories) using the ones listed by the skiddies on github, just search up [_**Bookmarklets**_](https://github.com/search?q=bookmarklets&type=repositories) and you will find tons of them

(this is what the policy is supposed to look like)

![image](https://github.com/K12SystemAdmin/Disable-Bookmarklets/assets/133791743/174c8e82-196e-4e5e-bf07-865ebe63b553)

Once you have found a Bookmarklet to test out, when testing it, nothing is supposed to happen when trying to use/click the bookmarklet, that is the whole reason why they don't work, it won't give you a **Blocked Site** error since Javascript itself is not a website but more of code trying to be ran once clicked on

-------------------------------------------------------------------------------------------------------------------------------------
## Finalizing

Thank you to all of the people who have came across this repository and found this helpful, and apologies in advance for the skiddies who come across this :-)
