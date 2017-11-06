1. How do we make flash messages display on a page?
  We add erb tags in our application layout and declare them inside the action method.

2. Where is cart information/temporary information usually stored?
  The temporary cart information is temporary stored in a session.

3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?
  We do not want to store the cart in our database because, we only want to store the ones that are submitted.


4. What is the purpose of the asset pipeline?
  The asset pipeline keeps our styling in one place so we do not have to require many files.

5. Why do we precompile our assets?
  We precompile our assets so our images and our assets file in general run faster.

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```
Stylesheet tag loads our css.
Javascript tag loads our js files.
Image tag loads our images folder.  

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
A great read me has a brief explanation of the project and also tells the person how to run the app. By updating a readme we let them know what the app is about or what step are we in.

8. What are the top four accessibility issues that we as developers should be aware of?
  I really have no idea.

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
  Before save is an example of a callback. We will find it in our models or controller.

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
scope :active, where(active: true)

11. What is the difference between a scope and a class method?
  Scopes are easier to use than class methods.
