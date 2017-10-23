## Miguel Silva

### Questions

1. What is the entry at the command line to create a new rails app?
  rails new <filename>

2. What do Models generally inherit from in rails?
  Application Record

3. What do Controllers generally inherit from in a rails project?
  Application Controller

4. How would I create a route if I wanted to see a specific horse in my
 routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  get '/horses/:id', to: 'horses#show'

5. What rake task is useful when looking at routes, and what information does it give you?
  rake routes, and it gives you a table of all the routes. The table has all the prefixes, verbs, URI's, and actions.

6. What is an example of a route helper? When would you use them?
  Namespace is an example of a route helper and we will want to use it when we want to separate out resources to differinciate them.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  path are for views because ahrefs are implicitly linked to the current URL. So it’d be a waste of bytes to repeat it over and over. In the controller, though, url is needed for redirect_to because the HTTP specification mandates that the Location: header in 3xx redirects is a complete URL.

8. What are strong params and why are the necessary?
  Strong params protects your apps from users passing anything else than what you want into your database.

9. What role does `form_for` play in helping us create our forms?
  form_for helps us collect information from the user and sends the information to the correct verb.

10. How does `form_for` know where to submit the user's input?
  We pass form_for an argument to let it know where to submit the user information.
11. Create a form using a `form_for` helper to create a new `Horse`.
```
  <%= form_for @horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name%>

  <%= f.submit%>
  <% end %>
```  
12. Why do we want to validate our models?
  We want to validate our models so our database is consistent and that way we have control of what goes in the database.
