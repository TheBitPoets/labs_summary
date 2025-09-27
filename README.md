# TPSI Labs 
A brief summary about last labs

* [lab1](https://github.com/kinderp/lab1)
  A simple HTML & CSS static site
  * [Slides](https://drive.google.com/drive/folders/1hn9WS82YY85AEk96P37Dk3oHnd7bYMdi?usp=sharing)

| Data          | Codice        |
| ------------- | ------------- |
| 1) 08/09/2025 |   [lab1.zip](https://github.com/user-attachments/files/22309538/lab1.zip) |
| 2) 15/09/2025 |   [lab1.zip](https://github.com/user-attachments/files/22359803/lab1.zip) |
| 3) 22/09/2025 |   [lab1.zip](https://github.com/user-attachments/files/22571307/lab1.zip) |




* [lab2](https://github.com/kinderp/lab2)
  A more sophisticated HTML & CSS site (with local and session storage)

* [lab3](https://github.com/kinderp/lab3)
  All javascript you need for this year. Use this lab as reference!

* [lab4](https://github.com/kinderp/lab4)
  Tic tac toe game in HTML + CSS + Javascript 

* [lab5](https://github.com/kinderp/lab5):
  
  This lab contains a first and simple example about server side code using express.js. We expose a `get` method on a `/` route to the clients. This route just returns a `hello world` message in a json format. It contains a front-end as well that uses a `fetch` call in order to contact exposed route on the server side.
  
  **Note** Here we use cors lib instead of serving pages on our own.
    1. [client.html](https://github.com/kinderp/lab5/blob/master/client.html)
    2. [client.js](https://github.com/kinderp/lab5/blob/master/client.js)
    3. [index.js](https://github.com/kinderp/lab5/blob/master/index.js)
 
  **What will we learn?**
    1. **How to send data from client to server** via `fetch` call.
    2. **How to expose a route** over a `GET` method on the server
    3. **How to use cors** headers
       
* [lab6](https://github.com/kinderp/lab6):

  In lab6 we'll learn how to send data from an html page using `form` tag without using any javascript code (in plain html). Form data will be sent via a `post` method to an exposed `/comment` route on the server. Data coming from client will be just printed out from server (until now we don't know how to save data in a database, we'll see that in the following labs). To make our example more realistic our server will come back a `success.html` page to the client after receiving and printing data. 

  ```html
  <form action="comment" method="post">
  ```
  1. [client.html](https://github.com/kinderp/lab6/blob/master/client.html)
  2. [server.js](https://github.com/kinderp/lab6/blob/master/server.js)
  3. [success.html](https://github.com/kinderp/lab6/blob/master/success.html)
 
  **What will we learn?**
    1. **How to send data from client to server** via a `form` html tag.
    2. **How to receive data** via post on the server
    3. **How to return back a success page** to the client
       
* [lab7](https://github.com/kinderp/lab7):

  In this lab we'll see all the differnt ways to send data (parameters) from client to server (at least the three most used ones)
  
  a) Data over **query string** using `GET`
     ```
     http://localhost:3333/users?id=1234&token=abc
     ```
  b) Data inside a **route** using `GET`
     ```
     http://localhost:3333/users/5678/def
     ```
  c) Data in a **body form** request over `POST`
  
  We have an html frontend with three buttons each one sending data to the server in a diffent way (see above for a list of the three different used methods). This time we don't use plain html to send data but we manage communications with javascript (in `client.js`) via `fetch` calls.

    1. [client.html](https://github.com/kinderp/lab7/blob/master/client.html)
    2. [client.js](https://github.com/kinderp/lab7/blob/master/client.js)
    3. [server.js](https://github.com/kinderp/lab7/blob/master/server.js)

  **What will we learn?**
    1. **How to send data from client to server** via `form` using a `fetch` call over `POST` method. You send data via `fetch` call over `GET` method as we've already dove in lab5. 
    2. **How to send data** inside a route using a `fetch` call over a `GET` method
    3. **How to send data** as a query string using a `fetch` call over a `GET` method 
    4. **How to receive data** coming in these three different ways

* [lab8](https://github.com/kinderp/lab8):

  Here we finally learn how to interact with a database. We have an html frontend with three buttons, each one for a different type of database relationship (N:N, 1:N, 1:1). Clicking on these buttons a `fetch` call to the server will be executed from client. After receiving a frontend call, server's code will run a corresponding sql statement in order to create the selected relationhip from the user.

  **Note** We're using [`sqlite3` lib](https://www.npmjs.com/package/sqlite3) in order to interact with sqlite dbs  
    1. [index.html](https://github.com/kinderp/lab8/blob/master/index.html)
    2. [index.js](https://github.com/kinderp/lab8/blob/master/index.js)
    3. [server.js](https://github.com/kinderp/lab8/blob/master/server.js)
 
    **What will we learn?**
    1. **How to interact with a databse from server side**

* [lab9](https://github.com/kinderp/lab9)

  In lab9 we'll use an already prepared db containing a single table (named `utenti`) in order to create two html pages: `register.html` and `login.html`. The first one `register.html` contains an html form used to register a new user in our db; please take care here that even if we set `action` and/or `method` form parameters:
  
   ```html
    <form action="" method="post">
   ```
  
  we manage client/server communication with javascript inside `register.js` just adding there following line

   ```js
     e.preventDefault(); // Prevent default form submission behavior
   ```

    Form data will be sent as body of a `post` method call. After receiving a success response from server a **redirect to the login page** will be executed by the client.
  In the second one (`login.html`) we just try to send our new credential created in the previous step. **TODO** In case of a login success response from server we need to be redirected to some sort of user's homepage. We can't to do that so far because we aren't able to create dynamic html page on the fly. We'll learn it in the next lab.
  
    From a server side point of view either for login or for register we need to receive parameters from a fetch call over a post method and the use these parameters to create a new row in the `utenti` table. We'll use what we've learnt in the previous lab to do that. Server shows how to expose `GET`, `POST`, `PUT` and `DELETE` methods on different routes as well.

   1. [register.html](https://github.com/kinderp/lab9/blob/master/register.html)
   2. [register.js](https://github.com/kinderp/lab9/blob/master/register.js)
   3. [register_success.html](https://github.com/kinderp/lab9/blob/master/register_success.html)
   4. [login.html](https://github.com/kinderp/lab9/blob/master/login.html)
   5. [login.js](https://github.com/kinderp/lab9/blob/master/login.js)
   6. [index.js](https://github.com/kinderp/lab9/blob/master/index.js)
   7. [test.db](https://github.com/kinderp/lab9/blob/master/test.db)

   **What will we learn?**
 
  1. **How to expose whatever kind of http method on the server** 
  2. **How to manage a regiser and/or a login process** 
    
* [lab10](https://github.com/kinderp/lab10):
  
  **Note** Before begin this lab, please take a look at this [nunjucks intro](https://github.com/kinderp/nunjucks_lab)

  In this lab we'll how to generate (from server) some dynamic html pages on the fly using parameters coming from client as input query parameters for our internal database.
  **Note** We'll use [nunjucks](https://mozilla.github.io/nunjucks/) as template engine
  This time we won't use an already prepared db but istead we'll create from scrath our db using two javascript files (`create_db.js`, `populate_db.js`).

   1. [create_db.js](https://github.com/kinderp/lab10/blob/master/create_db.js)
   2. [populate_db.js](https://github.com/kinderp/lab10/blob/master/populate_db.js)
   3. [server.js](https://github.com/kinderp/lab10/blob/master/server.js)
   4. [elenco_missive.html](https://github.com/kinderp/lab10/blob/master/elenco_missive.html)
   5. [elenco_transita.html](https://github.com/kinderp/lab10/blob/master/elenco_transita.html)

  **What will we learn?**
    1. **How to generate dynamic html pages on the server**

 * [lab11](https://github.com/TheBitPoets/websocket-node)

   In this lab we'll see websocket communication. We don't use a plain raw websocket but in order to make it simpler we're gonna use [socket.io](https://socket.io/) lib that's just a wrapper around websockets

   1. [index.html](https://github.com/TheBitPoets/websocket-node/blob/main/index.html)
   2. [index.js](https://github.com/TheBitPoets/websocket-node/blob/main/index.js)
     
  **What will we learn?**
    1. **How to make real time bidirectional communication over websocket instead of using html protocol**
  
