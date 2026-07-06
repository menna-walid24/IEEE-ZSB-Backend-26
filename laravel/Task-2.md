**1-Laravel Gates**

Laravel Gates is like an authorization feature that acts as a boolean function that returns true or false , depending on user's permissions.

**Example**


if we have a bank application system that only admins have access to manage client processes.

The gate main job is to prevent users from that and allow only the admins by checking the user's role.

If admin->allow
else ->403 Forbidden error

---
**2-Sanctum vs Passport**


Sanctum vs Passport are  packages to secure APIs.

instead of using `session()` on laravel code .



**Sanctum:**

laravel give the application something like id called `token` and send this token for each request instead of using session.


**Passport**

Passport is more complex than sanctum.

It gives the app something called `Access Token` that acts like a temporary permission .

**Example**

sign in with google to any app.

---
**XSRF & CSRF**

CSRF:


is a way to prevent hacking ,if a user already logged in and website make use of that by hacking session cookie ,so CSRF is responsible for making a `token` .


Request will be approved only when token match the request token and also the cookie

**the difference**


is only the first character ,there is no difference in technical job.


***
**Defining relationships in Eloquent models**

**1-one to one**


one thing belongs to one thing, one thing has only one sonething.


**For Example**


Each user has an id ,and each id belongs to one user.

**2-One to many**

A user have many telephone numbers ,
these telephone numbers belong only to this user.

**3-Many to Many**

Department has some employees , employees work in more than department
***
