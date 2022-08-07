A Simple User API build with Laravel 9 REST API Authentication Using Sanctum - CRUD

**This is the link to Heroku [simpleUserAuth-API](https://simple-user-auth-api.herokuapp.com/) Application**
**This is the link to the Postman [Postman documentation](https://documenter.getpostman.com/view/21762181/VUjMnk9D) Application**

Firstly after initializing your application, Update the existing User Model and Migration file to have the following fields

id
Name
Email
Password
Timestamps (which already exist, do not change)

User Controller with the following methods

Register: This takes in the following 
Name
Email | should be unique
Password 
Password repeat

For a user to be registered successfully, validate the all fields, email must be unique, password and password repeat must be same
If the validation passes, register the user. On success return the user that was register as a json
 
Login: Takes in the following
Email
Password

Logs in the user if the email and password correspond to that in the database
If login was successful,create a session for the user and return a json response with the session and success

Update: Does the following
Updates any of the field specified, if success, return a json of the update user

Delete: Does the following
Takes in the user Id and deletes the user, if success, return a json with success

Getuser: returns a json of user by ID

GetUsers: returns all users from the database

NOTE: Use user api.php for routing, with the following endpoints

Register: /user/create

Login: /user/login

Update: /user/update/{id}

Delete: /user/delete/{id}

Getuser: /user

Getusers: /users