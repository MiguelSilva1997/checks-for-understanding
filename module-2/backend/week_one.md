## Week One - Module 2 Recap
Note: When you're done, submit a PR.

1. List the five common HTTP verbs and what the purpose is of each verb.
 get => request a page, it only retrieves data.
 post => is used to submit a form and often changes the database.
 put => changes an existing entity or element with the users input.
 patch => is used to make partial changes to a resource.
 delete => deletes a specific item.

2. What is Sinatra?
  Sinatra is a DSL to quickly build an app and is built in ruby.
4. What is MVC?
  MVC stands for models, views, and controllers. It is a framework that allow us to build an app that divides it parts in three.
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  We follow conventions so the internet does not become a mess and so other developers can understand better our code.
6. What types of variables are accessible in our view templates without explicitly passing them?
  Instance variables are accessible in our view templates without explicitly passing them.
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = '1'
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
```ruby
get '/horses' do
  @count = '1'
  name = 'Mr. Ed'
  erb :index, :locals => {name: name}
end
```
9. What's the purpose of ERB?
  The purpose of ERB is to be able to add ruby code into our html file.
10. Why do I need a development AND test database?
  We need a development database to use the real data and check if it will work. We need a test database so we do not add things to our database that we do not need and test our code.
11. What is CRUD and why is it important?
  CRUD refers to all the major functions that belong to a relational database application.
12. What does HTTP stand for?
  HyperText Transfer Protocol.
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  <%=%> prints to the screen.
  <%%> does not print to the screen.
14. What's an ORM?
  An ORM is an object relational mapping and acts like an translator between the app framework and the database.
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  The most commonly use ORM is ActiveRecord.
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
VERB PATH          CONTROLLER  ACTION   USED for
GET	/restaurants	restaurant	index	display a list of all restaurants
GET	/restaurants/new	restaurant	new	return an HTML form for creating a new photo
POST	/restaurants	restaurant	create	create a new restaurant
GET	/restaurants/1	restaurant	show	display a specific restaurant
GET	/restaurants/1/edit	restaurant	edit	return an HTML form for editing a restaurant
PUT	/restaurants/1	restaurant	update	update a specific restaurant
DELETE	/restaurants/1	restaurant	destroy	delete a specific restaurant

17. What's a migration?
  The process of transferring data between computer storage to a database.
18. When you create a migration, does it automatically modify your database?
  No, when you create a migration you just tell the computer the instructions on how to build it.
19. How does a model relate to a database?
  A model extracts the information from a database to add functionality to the app.
20. What is the difference between `#new` and `#create`?
  New does not saves the row into the database and create saves it automatically.
