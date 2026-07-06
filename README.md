# MEN STACK NOTES

| CRUD Action | RESTful Action | HTTP Method | Definition |
| ----------- | -------------- | ----------- | ------------------------ |
|  | `new` | `GET` | Show a form to create a new item |
| Create | `create` | `POST` | Add a new item to the database |
| Read | `index` | `GET` | Show all items |
| Read | `show` | `GET` | Show one specific item |
|  | `edit` | `GET` | Show a form to edit an existing item |
| Update | `update` | `PUT` | Save changes to an existing item |
| Delete | `delete` | `DELETE` | Remove an item from the database |


## SETUP

- create a directory
- create server file `touch server.js`
- initialize a node project with `npm init -y`
- install express `npm i express`

### Write Server Boilerplate

Server.js
```js
const express = require('express') // this imports the express package into our server
const app = express() // this creates an express app to actully use it

app.listen(3000, function(){
    console.log("Listening on port 3000 🙌🙌😔")
})
```

Run the server with `nodemon server.s`


rendering EJS

- install ejs with `npm i ejs`
- create a `views` directory
- create an `.ejs` file like `home.ejs`
- add html boilerplate with "!"

home.ejs
  ```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home</title>
</head>
<body>
    <h1>We are rendering an EJS page!</h1>
    
</body>
</html>
  ```

- render `ejs` page using a controller like this one:

```js
app.get("/", function(req, res) {
    res.render("home.ejs")
})
```
