# Objective Relational Mapping 
> old quiz: https://learning.flatironschool.com/courses/3299/quizzes/19089?module_item_id=267106

## Intro 
The benefits of ORM
How ORMs can abstract database logic
How to use data from a database to make Ruby objects
Turning database rows into Ruby objects
Mapping a database table to a Ruby object

## Defining Object-Relational Mapping
> source/s: https://learning.flatironschool.com/courses/3299/pages/defining-object-relational-mapping?module_item_id=143883

Explain the concept of an ORM and why we build them.
Describe the code that will map your Ruby objects to a database.

## Mapping Ruby Classes to a Database
> source/s: https://learning.flatironschool.com/courses/3299/assignments/133607?module_item_id=277032

Write code that maps a Ruby class to a database table
Write code that inserts data regarding an instance of a class into a database table row

## Questions

Q: How does an ORM (Object-Relational Map) map between our object-oriented code and a database table? Match each OO concept to the corresponding database structure:

Concepts:

a) Class
b) Instance of a class
c) Attribute belonging to a class
d) Value of an attribute for an instance of a class

Options:

1) Database table
2) Table row
3) Table column
4) Table cell


Q: (T/F) Using an ORM enables us to save Ruby objects in our database. (false)

Incorrect answer info: This one is a bit tricky! We are not able to save the object itself into our database; instead, we are saving the values of the attributes of that object.


Q: Which of the following are advantages of using an ORM? (select all that apply)

a) It allows us to abstract common database tasks into methods
b) It cuts down on repetitive code
c) It sets up a consistent, logical relationship between object-oriented code and database tables
*d) All of these are advantages of using an ORM

