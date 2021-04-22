---
layout: post
title:      "MyLists Javascript Portfolio"
date:       2021-04-22 16:45:46 +0000
permalink:  mylists_javascript_portfolio
---


I just finished my MVP-SPA Javascript portfolio project, MyLists, and feel proud about it, about how far I’ve got and how much I’ve learned on my journey with the Flatiron School Self-Paced Program. Feeling good.

The main motivation of this project was to create a list-based website management system with tagging and search functionality. There are some browser extensions on the market, but I really wish this functionality would be a standard in the modern browsers. The MVP though, only covers the tab navigation, List creation and assignment/removal of a website to a given list. You can see the MVP flowchart diagram [here ](https://drive.google.com/file/d/1P3OrDBLsD-koSpY4GY_k0Nw3TTx96WRF/view?usp=sharing).

My Sinatra project was based in the same concept but it has been fun to develop the same idea for the frontend and see how efficient and powerful JS can be on the browser side. 


The hardest part of this project, now that I write this blog retrospectively, was the planning part: To make this project/idea meet the requirements, create the classes, establish the object relationships and try to keep my code DRY. Unfortunately, I couldn’t start right away writing classes so I started writing functional programming js and then turn it into classes at some point.

Here is a short description about the 5 classes that myLists comprises:

1. myListsTabHandler: template for creating myLists tab objects. Each tab has one associated form.
When the user clicks on an inactive tab, this will be activated and its associated form will be displayed, all other tabs and forms will be deactivatedor hide respectively.

2. myListsFormHandler: template for creating myLists form objects. Some forms have a datalist object associated. 
When the user clicks on submit, form data will be updated on the front- and backend sides.

3. myListsDatalistHandler: template for creating myLists datalist objects and update the datalist when new lists are created.

4. myListsFieldsetHandler (static methods): handles the display of all created lists and their associated websites.

5. myListsFetchRequest (static methods): serves as a fetch interface for get, post and delete requests.



Feel free to checkout my Github [repo](https://github.com/Emanao/my-lists-js-portfolio-project).

Thanks!

