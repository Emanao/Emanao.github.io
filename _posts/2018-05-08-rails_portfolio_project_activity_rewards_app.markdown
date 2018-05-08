---
layout: post
title:      "Rails Portfolio Project: Activity Rewards App"
date:       2018-05-08 14:48:19 +0000
permalink:  rails_portfolio_project_activity_rewards_app
---


For our third portfolio project at Flatiron we were asked to build a Content Management system that manages related data through complex forms and RESTful routes. This time I came up with a very different idea from my previous one (the bookmark management system). I started building the beta version of what it should be a family/personal reward system app, but with how a loyalty rewards program works in mind.

The activity rewards app tracks points for specific user activities, which an administrator have assigned before. Some further statistical admin functionality is provided.
 
All users are required to have either a local or remote account (GitHub in my case) for authentication purposes. Once they are authenticated they access to their profile page. The profile page differs from user role. When admin users access to their profile page they can add goals to existing users or edit existing goals. Admins can also search users by name and they have an overview of some user statistics in their profile page. Regular users profile page offers the possibility to update their achieved goals and see the total balance in their points account.

The initial phase of the activity rewards app has 3 models: User, Achievement and Activity models and their relationships are: users can have many activities to follow and one activity can have many users. The achievement model represents the activities being followed (goals) by the users  an how many time they achieved it.

The biggest challenge I faced during this project was while in the midst of my implementation I identified e.g. that regular user functionality needed to be shifted over from regular user to the administrator role. After the first shock, I could realize that changes were doable without starting over since I could move the logic easily from one controller to the other making some little adjustments in the view and of course the routing. I think the worst part was to get myself mentally ready for the change since it was a big structural one.



