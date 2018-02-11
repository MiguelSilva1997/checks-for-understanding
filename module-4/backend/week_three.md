## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. At a high level, what is Node?

  Node is a server side, JavaScript run time environment which executes code server side.

2. What is Express? What is Express similar to in the Ruby world?

Express is similar to Sinatra in the Ruby world. It is a lightweight framework that allows you to build apis.


3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.

  ```
  var express = require('express');
  var router = express.Router();

  router.get("/user", (req, res) => {

  })
  ```


4. What do we use Knex for?

  Knex is a SQL query builder which allows us to build and setup our database.

5. How could you organize your code to follow the MVC design pattern in your Quantified Self project?

  To follow MVC convention you could create a folder for the routes, a folder for the controllers and a folder for the models.

6. How do you execute raw SQL in node?

  ```
    database.raw(
      'SELECT * FROM foods' +
      ' INNER JOIN meal_foods ON foods.id = meal_foods.food' +
      ' WHERE meal_foods.meal = ?', [id]
    )
  ```

7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?

  The advantages of separating your front end from your back end are:
    * Scalability
    * Easier to implement new changes
    * Release Planning
    * Working on different repos

  cons:
    * You cannot take advantage of built in templating languages(erb)
    * If you are a Start-up speed is f the essence

#### Review  

8. Describe DNS.

  DNS stands for Domain Name Servers and transforms a normal URI or URL into an IP address so the computer can understand what is it looking for. It acts like a computer GPS locator.

9. What does writing clean code mean to you?

  The definition of writing clean code for me is to write code that is maintainable, can be reuse and that is readable.

10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality?

  I will build a Building Class, then a Hotel Class, then a room class and Services Class. Building class will be in charge of what type of building is just in case we want to use the website later on for stuff other than hotels. Hotel class which will include the size, revies, and chain. The Room class will include what type of rooms they offer.
