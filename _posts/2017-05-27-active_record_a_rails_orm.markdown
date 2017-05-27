---
layout: post
title:  Active Record, a Rails ORM
date:   2017-05-27 03:22:30 +0000
---


After finishing my CLI gem project, I started the exciting journey exploring the database interactions with SQL, Object-Relational Mapper (ORMs) and Active Record (a Rails ORM). 

Once I finished my lectures, one of my big questions was what is Rails about and how is it related to Active Record. During my search I learnt that Rails is the best option when web applications need to access databases. Rails offers a model-view-controller framework written in Ruby where Active Record is the model representing business data and logic.  
Active Record is the ORM that Rails uses that allows you to represent models and their data, associations between models, validate models before getting persisted into the database and perform database operations in an object-oriented fashion. All this without writing any SQL statement. Still a good understanding of SQL is fundamental to work effectively with Active Records. 

To create Active Record models, the only thing we have to do is to subclass the ApplicationRecord::Base and Active Records will create methods to allow an application to read and manipulate data (CRUD) stored in its tables.

Once we have our models created, we’ll create the relationships between them through a set of macros (belongs_to, has_many…) that Active Record includes when inherited. When one of this macros is called on a class, a module of methods is created on the fly and added to the class. These methods allow the original parent class to interact with objects from the class passed as an symbol argument, the associated child. Rails associations in our models represent the database tables relationships.

The migration feature of Rails allow data definitions to be written in Ruby. Over the time as the database changes, the migration files will act as a version history of the database changes. Again, migrations don’t involve writing SQL, but you do need to know enough about databases to structure yours.

This is my short overview about the complex topic, Active Record.
