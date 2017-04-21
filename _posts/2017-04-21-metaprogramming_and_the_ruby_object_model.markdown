---
layout: post
title:  "Metaprogramming and the Ruby Object Model"
date:   2017-04-21 17:38:53 +0000
---

Working on this blog has helped me understand the basics of how Ruby works which is the foundation for learning Metaprogramming. This is a summary of what I believe is the most important part of Ruby if you want to use Metaprogramming: the Ruby Object Model.

WHAT IS METAPROGRAMING?
Metaprogramming is best explained as programming programs. Metaprogramming can be used to add, edit or modify the code of your program while its running. Scary isn't it? Using it you can make new or delete existing methods of objects, reopen or modify existing classes, catch methods that don't exist, and avoid repetitions in your code to keep your program DRY.

It is in Ruby’s nature to be a metraprogramming-friendly language. Ruby is an object oriented and interpreted language where most constructs (variables, classes, methods…) in a Ruby program are available at runtime. All this constructs live together in a system called the object model. Understanding the object model in Ruby is the key to metaprogramming. 

THE RUBY OBJECT MODEL

Key concepts about the Ruby object model:
* Almost everything in Ruby is an object. Objects have a state (instance variables) and a link to a class where their methods (behavior) lives. 
* Instance variables live in the object and methods in the object’s class, where they are called instance method of the class.
* Classes are also objects (instances of Class class), plus a list of instance methods and a link to a superclass.
* Singleton classes are classes with only a single instance and they can’t be inherited. Each object in Ruby has its own singleton class. A singleton class is where the object’s singleton methods live. Class methods are singleton methods. The superclass of a singleton class of an object is the object’s class itself
* SELF: Self is always referring to the current object. Self is where the instance variables are found and the default receiver for method calls.
* When a method is called, Ruby looks into the object’s class (receiver’s class) and from there it climbs up the ancestors chain until it finds the method. This behavior is also called  the “one step to the right and then up” rule. Once Ruby has found a method it executes the method with the receiver as self.
* All methods calls have a receiver. If the receiver is not explicit the default receiver (self) will be used.

Metaprogramming itself is a big topic for me that I would love to go into detail in one of the next comming blogs, maybe closer to Rails.



