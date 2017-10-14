## Week Two - Module 2 Recap

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  ActiveRecord is a ruby library that allows you to use methods that talk to my database. In other words it translates ruby code to SQL queries.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

  Some methods that you can call on '`Team` are all, average, group, find and any other ActiveRecord method.  We have access to them because, we are inheriting from ActiveRecord.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

  * find(4).name
  * find(4).owner_id

  Comments:
  Not sure if you want the name of the owner or the id.

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

* find(4).owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
  A student has many teachers and teachers has many students.
  Teacher
  | :------------- | :------------- |
  | string      | name       |

  Student
  | :------------- | :------------- |
  | string       | name     |

  teacher_students
  | :------------- | :------------- |
  | integer       | teacher_id      |
  | integer       | student_id      |

6. Define foreign key, primary key, and schema.
  Foreign key is the key that connects two tables in a database. Primary keys are the keys that belong to one table that are unique and helps identify a specific row of that table. A schema is the blueprint of the instruction given by every migration made.
  

7. Describe the relationship between a foreign key on one table and a primary key on another table.
  The foreign key in one table helps you identify the relationship between tables. The foreign key refers to the primary key     of another table. Since the primary key is always unique it helps to point at a specific row.

8. What are the parts of an HTTP response?
  Response code
  Header
  Body

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
  * find() = finds the id
  * find_by() = finds by any method you want ActiveRecord to look for.
  * group = groups data by whatever you tell it too.
  * pluck = extracts an specific column from the database.
  * order = orders the queries by whatever you wanted to.

2. Name your three favorite ActiveRecord rake tasks and describe what they do.
  * rake db:drop = drops your database
  * rake db:migrate = creates the table in the database
  * rake db:rollback = deletes the last migration done.

3. What two columns does `t.timestamps null: false` create in our database?
  * created_at
  * updated_at

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
  It is a many to many relationship.

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
  

6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
