# lab_summary
A brief summary about last labs

* [lab1](https://github.com/kinderp/lab1)

* [lab2](https://github.com/kinderp/lab2)

* [lab3](https://github.com/kinderp/lab3)

* [lab4](https://github.com/kinderp/lab4)

* [lab5](https://github.com/kinderp/lab5):
  
  This lab contains a first and simple example about server side code using express.js. We expose a `get` method on a `/` route to the clients. This route just returns a `hello world` message in a json format. It contains a front-end as well that uses a `fetch` call in order to contact exposed route on the server side.
  
  **Note** Here we use cors lib instead of serving pages on our own.
    1. [client.html](https://github.com/kinderp/lab5/blob/master/client.html)
    2. [client.js](https://github.com/kinderp/lab5/blob/master/client.js)
    3. [index.js](https://github.com/kinderp/lab5/blob/master/index.js)
 
  **What We will learn?**
    1. **How to send data from client to server** via `fetch` call.
    2. **How to expose a route** over a `GET` method on the server
    3. **How to use cors** headers
* [lab6](https://github.com/kinderp/lab6)

  In lab6 we'll learn how to send data from an html page using `form` tag without using any javascript code (in plain html). Form data will be sent via a `post` method to an exposed `/comment` route on the server. Data coming from client will be just printed out from server (until now we don't know how to save data in a database, we'll see that in the following labs). To make our example more realistic our server will come back a `success.html` page to the client after receiving and printing data. 

  ```html
  <form action="comment" method="post">
  ```
  1. [client.html](https://github.com/kinderp/lab6/blob/master/client.html)
  2. [server.js](https://github.com/kinderp/lab6/blob/master/server.js)
  3. [success.html](https://github.com/kinderp/lab6/blob/master/success.html)
 
  **What We will learn?**
    1. **How to send data from client to server** via a `form` html tag.
    2. **How to receive data** via post on the server
    3. **How to return back a success page** to the client
       
* [lab7](https://github.com/kinderp/lab7)

* [lab8](https://github.com/kinderp/lab8)

* [lab9](https://github.com/kinderp/lab9)

* [lab10](https://github.com/kinderp/lab10)
