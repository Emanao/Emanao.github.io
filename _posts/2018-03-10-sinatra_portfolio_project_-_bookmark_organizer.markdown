---
layout: post
title:      "Sinatra Portfolio Project - Bookmark Organizer"
date:       2018-03-10 18:14:41 +0000
permalink:  sinatra_portfolio_project_-_bookmark_organizer
---


For our second portfolio project at Flatiron we were asked to create a Sinatra web application that helps users to track something important for them. I decided to go for a Bookmark Organizer that can help users to organize their bookmarks by tagging them instead of having them in a hierarchical folder model.
From my point of view the better way of managing bookmarks is by tagging URLs with user assigned keywords based on the website's content rather than storing bookmarks in a rigid hierarchical folder structure.

As first step a user needs to create an account on the bookmark organizer site. After logging in, users access to the Bookmark Organizer home page, where they can see their list of bookmarks with corresponding tags and their list of used tags. If the user clicks a tag all bookmarks linked to this tag are shown (this is a very useful feature specially in case of editing or deleting tags).
Bookmarks can be created, viewed, updated and deleted. When the user creates a bookmark, he needs to choose a name for it and can add the URL, existing tags or create new tags. Tags on the other side can only be created together with bookmarks. They can be viewed, updated and deleted.

After defining the requirements of what my application should do, I started with the design of my little database. The database should have a User, Bookmark, BookmarkTag and Tag table. A bookmark should have the user_id foreign key since a user has_many bookmarks and a bookmark belongs_to a user, and the join table BookmarkTag should have the foreign keys of bookmarks and tags in order to have the many_to_many relationship between bookmarks and tags.

Next step: Setting up my project in visual studio code. First, I added the gems in my Gemfile, required bundler and configured the database connection in the environment file and created the Rakefile so I could run my migrations and could start testing my models. Once I had them working I went on setting up the model view controller structure, being the main file my config.ru (my applications entry point).

Last step, coding and testing, and repeat.

Some issues I run into were:
-	When using tux, I had some conflicts with ripl (used by tux) and irb, so I had to install the gem ripl-irb to solve the problem.
-	Having my port in use by a process (my app :) > sudo lsof -i tcp:9393 > to find the PID of the process and kill PID > to kill the process with this PID.

Tools that helped me:
-	OneNote from Microsoft > Great to help you get organized. 
-	Creating a reset task in rake to destroy the data in my tables and in this way be able to start from scratch.

