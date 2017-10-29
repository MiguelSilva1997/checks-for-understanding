# Miguel Silva
## Week Four Recap

### Questions

* What is a cookie?
   Is a piece of data stored on the user's computer by the user's web browser while the user is browsing.

* What’s the difference between a session and a cookie?
  The main difference is that a session data is stored in a server and a cookie is stored on the client side.

* What’s a flash and when do you want to use flashes?
  A flash is a local shared object. It is a text file that is a sent by a Web browser.

* Why do people say “HTTP is stateless”?
  Because the connection between the browser and the server ends after       the transaction ends.

* What’s authentication? Explain.
  Authentication is the process of identifying the client and making sure they are who they say they are.

* What’s the difference between authentication and authorization?
  Authentication is the process of giving different clients access to some pages and authorization is making sure the client is the person they claim to be.

* What’s a before filter?
  A before filter is when we want to run a certain block of code before other methods are called.

* How do we keep track of a user once they’ve logged in?
  We keep track of a user by making a session for them.

* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  Namespace is more to separate two different objects like admin and users. Nested resources we use them when we the same object has the same use but we want to separate them.

* At a high level, what tools can you use to implement authorization? How would you use them?
  To implement authorization you can use bcrypt or use other apps authorization API. Like Twitter, Github, and Facebook.

* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
An enum is a way of giving different objects a role and a form of authorization. One of the advantages that it offers is that allows you to create a different amount of levels of authorization. An integer needs to be put in our database in order for it to work. You declare an enum in the controller.

* What are some strategies you can use to keep your views DRY?
  We can make methods in our model to make sure that we do not repeat ourselves.
