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

*a) toys
b) dogs
c) It's necessary to create a join table

Q: Say we have an app with Dog and Toy models, where toys belong to dogs and
dogs have many toys. Which of the following will correctly create a new toy and
associate it with the dog with id=2?

a)

```rb
Toy.create(name: "Squeaky Cheeseburger", dog_id: 2)
```

b)

```rb
dog = Dog.find(2)
Toy.create(name: "Squeaky Cheeseburger", dog: dog)
```

c)

```rb
dog = Dog.find_by(id: 2)
dog.toys << Toy.create(name: "Squeaky Cheeseburger")
```

*d) All of these will work

Q: Say we have an app with Doctor and Patient models, where doctors have many
patients and patients have many doctors. Which sql table should include the
foreign key?

a) doctors
b) patients
*c) It's necessary to create a join table

Q: Say we have a many-to-many relationship among Doctor, Patient and Appointment
models, where a doctor has many patients through appointments and vice versa.

(T/F) When setting up the Active Record associations in the `Doctor` model, we
**must** specify its relationship with `Appointment` **before** we can specify
its relationship with `Patient`. (true)

Q: Which of the following is **not** true about using Active Record to set up
relationships among models?

*a) It enables us to accomplish things that we couldn't accomplish with Ruby and SQL alone
b) Once it's configured, it automatically gives us access to a number of instance methods
c) It makes it unnecessary to write SQL code ourselves
d) It is consistent with the **convention over configuration** philosophy
e) You need to follow some strict naming conventions for it to work

For the next three questions, say we have used Active Record to set up a
many-to-many relationship among Teacher, Student and Class models, such that a
teacher has many students through classes and vice versa.

Q: Which of the following methods will Active Record make available to instances
of the `Teacher` model? (select all that apply)

a) `class`
*b) `classes`
c) `student`
*d) `students`
e) `teacher`
f) `teachers`

Q: Which of the following methods will Active Record make available to instances
of the `Student` model? (select all that apply)

a) `class`
*b) `classes`
c) `student`
d) `students`
e) `teacher`
*f) `teachers`

Q: Which of the following methods will Active Record make available to instances
of the `Class` model? (select all that apply)

a) `class`
b) `classes`
*c) `student`
d) `students`
*e) `teacher`
f) `teachers`
