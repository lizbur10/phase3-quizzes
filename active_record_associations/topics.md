# Active Record Associations

## Active Record Association Intro
* What are common methods accessible through Active Record associations?
* How do you use association macros?

## One To Many Associations
> source/s: https://learning.flatironschool.com/courses/3299/pages/video-active-record-one-to-many?module_item_id=294823, https://learning.flatironschool.com/courses/3299/assignments/133959?module_item_id=278759

* Understand how and why Active Record implements associations between models
* Use Active Record migrations and methods to build out a domain model that associates classes
* Establish the one-to-many (or has-many/belongs-to) association in Active Record

## Many to Many
> source/s: https://learning.flatironschool.com/courses/3299/assignments/134080?module_item_id=278760
* Establish the many-to-many (or has many through) association in Active Record

## Active Record Association Methods
> source/s: https://learning.flatironschool.com/courses/3299/assignments/74088?module_item_id=143912

* Understand the common methods we have access to from our Active Record associations
* Use the methods that Active Record gives you based on your associations



## Questions

Q: Say we have an app with Dog and Toy models, where toys belong to dogs and
dogs have many toys. Which sql table should contain the foreign key?

*a) toys (Yes! In our model, toys belong to dogs so the toys table should contain the foreign key)
b) dogs (Not quite! In our model, toys belong to dogs so the toys table should contain the foreign key)
c) It's necessary to create a join table (Not quite! This is a one-to-many association, so we don't need a join)

Q: Say we have an app with Dog and Toy models, where toys belong to dogs and
dogs have many toys. Which of the following will correctly create a new toy and
associate it with the dog with id=2?

a)

```rb
Toy.create(name: "Squeaky Cheeseburger", dog_id: 2)
```
(It's true that this code will work, but you might want to take another look at the other snippets)

b)

```rb
dog = Dog.find(2)
Toy.create(name: "Squeaky Cheeseburger", dog: dog)
```
(It's true that this code will work, but you might want to take another look at the other snippets)

c)

```rb
dog = Dog.find_by(id: 2)
dog.toys << Toy.create(name: "Squeaky Cheeseburger")
```
(It's true that this code will work, but you might want to take another look at the other snippets)

*d) All of these will work
(Yes! The snippets show three different ways we can accomplish our task)

Q: Say we have an app with Doctor and Patient models, where doctors have many
patients and patients have many doctors. Which sql table should include the
foreign key?

a) doctors (Not quite! What do we need to do to set up a many-to-many association?)
b) patients (Not quite! What do we need to do to set up a many-to-many association?)
*c) It's necessary to create a join table (Yes! This is a many-to-many association, so we'll need to create a join table)

Q: Say we have a many-to-many relationship among Doctor, Patient and Appointment
models, where a doctor has many patients through appointments and vice versa.

(T/F) When setting up the Active Record associations in the `Doctor` model, we
**must** specify its relationship with `Appointment` **before** we can specify
its relationship with `Patient`. (true)

(Correct: Yes! The association with `Appointment` needs to be set up before we can set up an association **through** it)
(Incorrect: Not quite! The association with `Appointment` needs to be set up before we can set up an association **through** it)

Q: Which of the following is **not** true about using Active Record to set up
relationships among models?

*a) It enables us to accomplish things that we couldn't accomplish with Ruby and SQL alone (Correct! It is **not** true that AR allows us to accomplish things we can't accomplish with Ruby and SQL alone. AR just saves us from doing all that coding ourselves!)
b) Once it's configured, it automatically gives us access to a number of instance methods (This **is** one of the advantages of using AR - you may want to go back and review)
c) It makes it unnecessary to write SQL code ourselves (This **is** one of the advantages of using AR - you may want to go back and review)
d) It is consistent with the **convention over configuration** philosophy (This **is** true of using AR - you may want to go back and review)
e) You need to follow some strict naming conventions for it to work (This **is** true of using AR - you may want to go back and review)

For the next three questions, say we have used Active Record to set up a
many-to-many relationship among Teacher, Student and Class models, such that a
teacher has many students through classes and vice versa.

Q: Which of the following methods will Active Record make available to instances
of the `Teacher` model? (select all that apply)

a) `class` (Not quite. Remember, a teacher **has many** classes)
*b) `classes` (Yes! A teacher has many classes, so AR provides a `classes` instance method)
c) `student` (Not quite. Remember, a teacher **has many** students)
*d) `students` (Yes! A teacher has many students, so AR provides a `students` instance method)
e) `teacher` (Be sure to study the source/s for this question. You'll get it next time.)
f) `teachers` (Be sure to study the source/s for this question. You'll get it next time.)

Q: Which of the following methods will Active Record make available to instances
of the `Student` model? (select all that apply)

a) `class` (Not quite. Remember, a student **has many** classes)
*b) `classes` (Yes! A student has many classes, so AR provides a `classes` instance method)
c) `student` (Be sure to study the source/s for this question. You'll get it next time.)
d) `students` (Be sure to study the source/s for this question. You'll get it next time.)
e) `teacher` (Not quite. Remember, a student **has many** teachers)
*f) `teachers` (Yes! A student has many teachers, so AR provides a `teachers` instance method)

Q: Which of the following methods will Active Record make available to instances
of the `Class` model? (select all that apply)

a) `class` (Be sure to study the source/s for this question. You'll get it next time.)
b) `classes` (Be sure to study the source/s for this question. You'll get it next time.)
*c) `student` (Yes! A class **belongs to** a student, so AR provides a `student` instance method)
d) `students` (Not quite. Remember, a class **belongs to** a student)
*e) `teacher` (Yes! A class **belongs to** a teacher, so AR provides a `teacher` instance method)
f) `teachers` (Not quite. Remember, a class **belongs to** a teacher)
