# SI 364 - Final Project questions

## Overall

* **What's a one-two sentence description of what your app will do?**

## The Data

* **What data will your app use? From where will you get it? (e.g. scraping a site? what site? -- careful not to run it too much. An API? Which API?)**
# My app will get restaurant data from the Zomato API

* **What data will a user need to enter into a form?**
# Users will need to enter in a city and the type of cuisine they are looking for

* **How many fields will your form have? What's an example of some data user might enter into it?**
# My form will have two fields, one for the the type of cuisine they are looking for and one for the city

* **After a user enters data into the form, what happens? Does that data help a user search for more data? Does that data get saved in a database? Does that determine what already-saved data the user should see?**
# When a user enters data into the form, a search will be done, with the cuisine and city, using the Zomato API to find a list of restaurants that match both of those specifications

* **What models will you have in your application?**
# I will have a Restaurant model, a Cuisine model, and a City model

* **What fields will each model have?**
# The Restaurant model will have foreign keys for it's cuisine and city. It will also have an id field, a restaurant name field, and potentially a field to hold a link to the menu or restaurant site.

* **What uniqueness constraints will there be on each table? (e.g. can't add a song with the same title as an existing song)**
# Users won't be able to add a restaurant with the same name and city as an existing restaurant

* **What relationships will exist between the tables? What's a 1:many relationship between? What about a many:many relationship?**
# There will be a one to many relationship between a city and restaurants and a many to many relationship between cities and cuisines

* **How many get_or_create functions will you need? In what order will you invoke them? Which one will need to invoke at least one of the others?**
# I will have three get_or_create functions, one for each model. I will use the get_or_create_restaurant function to invoke the get_or_create_city and get_or_create_cuisine functions. I will need to invoke functions for city and cuisine before I invoke the get_or_create_restaurant function.

## The Pages

* **How many pages (routes) will your application have?**
# My application will have four pages/routes. The first will be a greeting screen where users are asked to input a city and cuisine type. The next page will show a list of restaurants that fit those parameters, allowing users to check off places they have been to already. After that, users will see a list of places all the places they have not been to. There will also be a page to show already visited restaurants. There will additionally be two error pages.

* **How many different views will a user be able to see, NOT counting errors?**
#Users will be able to see four different views, all excepte the error pages.

* **Basically, what will a user see on each page / at each route? Will it change depending on something else -- e.g. they see a form if they haven't submitted anything, but they see a list of things if they have?**
#The first page will be a greeting screen where users are asked to input a city and cuisine type. There will also be an option to show previously visited restaurants. The next page will show a list of restaurants that fit those parameters, allowing users to check off places they have been to already. After that, users will see a list of places all the places they have not been to.

## Extras

* **Why might your application send email?**
#My application may send an email to the user when a new restaurant has been visited and added to the visited restaurants database.

* **If you plan to have user accounts, what information will be specific to a user account? What can you only see if you're logged in? What will you see if you're not logged in -- anything?**
#I don't plan to have user accounts as of right now, but may think about adding them in later.

* **What are your biggest concerns about the process of building this application?**
#My biggest concern is that I will face difficulty tracking and parsing through all of the restaurant information that I may get back on each search.