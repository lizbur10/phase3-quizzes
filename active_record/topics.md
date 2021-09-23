# Active Record
> old quiz: https://learning.flatironschool.com/courses/3299/quizzes/19094?module_item_id=267147

# Active Record Introduction

* The Active Record conventions and why programmers use them
* Active Record query methods
* Using Active Record to create a table

# Active Record Mechanics
> source/s: https://learning.flatironschool.com/courses/3299/pages/active-record-mechanics?module_item_id=143901

* Understand the connection between an ORM and Active Record
* Understand why Active Record is useful
* Learn what "convention over configuration" means
* Develop a basic understanding of how to get started with Active Record

# Active Record Migrations 
> source/s: https://learning.flatironschool.com/courses/3299/pages/video-active-record-migrations?module_item_id=294221, https://learning.flatironschool.com/courses/3299/assignments/74082?module_item_id=143904, https://learning.flatironschool.com/courses/3299/assignments/74083?module_item_id=143905

* Create, connect to, and manipulate a SQLite database using Active Record
* Write your own migrations
* Run a migration to create a table
* Run a migration to add a column to a table
* Run a migration to change something in the table

# Active Record CRUD 
> source/s: https://learning.flatironschool.com/courses/3299/pages/video-active-record-read-and-create?module_item_id=294821, https://learning.flatironschool.com/courses/3299/pages/video-active-record-update-and-delete?module_item_id=294822, https://learning.flatironschool.com/courses/3299/assignments/74085?module_item_id=143907

* Create migrations using Active Record
* Interact with a SQL database table from a Ruby class using Active Record
* Perform CRUD operations on a SQL database table using Active Record
* Create a table using Active Record
* Use Active Record's querying methods

## Questions

Q: In order for Active Record to work, it is necessary to follow the naming conventions it is expecting. Specifically, the name of the class must be _______ and the name of the table must be ________. (singular, plural)

Source: https://learning.flatironschool.com/courses/3299/pages/active-record-mechanics?module_item_id=143901


Q: Which of the following steps is **not** required to get Active Record set up?

*a) Set up attribute macros (`attr_accessor`, `attr_reader`, or `attr_writer`) in the model file
b) Write code to establish the connection to the database
c) Write code to create the database table
d) Run a command in the terminal to install the Active Record gem
e) Set up the model to inherit from `ActiveRecord::Base`

Q: (T/F) If we have Active Record set up for our application and we create an `Article` model in the `article.rb` file, Active Record will automatically create the `articles` table in the database for us. (false)

Source: https://learning.flatironschool.com/courses/3299/pages/active-record-mechanics?module_item_id=143901


Q: In the following code, which is used to create a Rake `migrate` task, what
goes in the blank? (namespace)

```rb
__________ :db do
  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end
end
```

Incorrect answer info: The first line in the snippet is creating a `namespace`, which helps better describe and organize our Rake tasks.

Source: https://learning.flatironschool.com/courses/3299/assignments/74081?module_item_id=143903


Q: Which of the following is true about using Active Record migrations to do the setup for our database?

*a) Using migrations takes care of writing the SQL to create a table, but does not take care of establishing the connection to the database.
b) Using migrations takes care of establishing the connection to the database, but does not take care of writing the SQL to create a table.
c) Using migrations takes care of both establishing the connection to the database and writing the SQL to create a table.

Source: https://learning.flatironschool.com/courses/3299/assignments/74082?module_item_id=143904


Q: Which of the following are reasons that we need to include a timestamp at the
beginning of a migration's filename? (select all that apply)

*a) It ensures that the migrations are run in the right order.
*b) It helps ensure that each migration is only run once.
c) Active Record uses the timestamp to figure out how to revert a migration. (Incorrect answer info: For reverting a migration, AR refers to the **content** of the migration (e.g., removing a table or column that was created; reversing a change made to a column), not the timestamp.)
d) It allows us to reuse the part of the filename after the timestamp for multiple migration files. (Incorrect answer info: We want our filenames to be as descriptive as possible of the actual change being made so it doesn't't make sense to reuse names.)

Source: https://learning.flatironschool.com/courses/3299/assignments/74082?module_item_id=143904


Q: (T/F) Having the class name in a migration file match the name of the file
itself is helpful for keeping a clear record of the updates we've made to the
database, but it isn't necessary. (false)

For incorrect answer: Active Record relies on naming conventions in order for it to work so, if the name of the class and the name of the file don't match, the migration will error out.

Source: https://learning.flatironschool.com/courses/3299/assignments/74082?module_item_id=143904


Q: Which of the following is **not** an Active Record querying method?

*a) #sort
b) #where
c) #first
d) #maximum


