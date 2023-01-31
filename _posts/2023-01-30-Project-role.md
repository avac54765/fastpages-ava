---
title: Individual Project Blog
toc: true
comments: true
layout: post
description: Planning out write-up and section/feature of project.
permalink: /project/individual
image: /images/cbimage.png
categories: [week 20, collegeboard, planning, project]
---


# Preview Write-Up for CollegeBoard Requirements

- Row 1 (Program Purpose and Function)
    - The purpose of my function is to motivate users to want to workout.
    - The function of my program is for users to input their own motivational quotes and see other motivational quotes from other users/developers. This page also as an alert of a motivational saying.
    - The input of my video would be a user putting in a quote into the form and seeing their quote be placed in a table of other quotes. The user could also click the motivational button to receive an alert at the top of their screen of a motivational saying.
- Row 2 (Data Abstraction):
    - The collection of data will be in a database with a class named Quotes
    - the data in this database will contain all of the quotes that users have inputted which are then showed to the users in the table. 
- Row 3 (Managing Complexity):
    - This database and class manage complexity because they keep the inputted data organized and easy to access from the frontend. Without this class and database, I would have to store all input locally within a list/dictionary and use a rest API to call it.
- Row 4 (Procedural Abstraction):
    - show procedure of backend? class? Maybe show CRUD features.
    - The delete feature allows a user to delete a quote that they have posted. This would delete the quote from the table of quotes.
- Row 5 (Algorithm Implementation):
    - sequencing = setter function in class = going through steps
    - selection = if a condition is tested = garbage data
    - iteration = loop for putting the quotes in the table
    - A user will input a quote, using the API to send it to the backend and add it to the database. The API will then send an updated list of the quotes to the frontend to be turned into a table. 
- Row 6 (Testing):
    - first call: sending a quote to the backend
    - second call: sending a short quote to the backend
    - first condition: is the quote valid? long enough?
    - second condition: is the quote valid? long enough (more than two characters?)
    - first result: quote is added to the table
    - second result: an error message is returned saying the quote is not long enough/valid.


# What is my feature?

![Quotes images]({{site.baseurl}}/images/quotes.png)
![Inspo Table]({{site.baseurl}}/images/inspoindividual.png)

My feature of our team CPT project is the Inspiration page. 

- This page allows for users to gain motivation and inspiration to work out.
- Users can read existing quotes or even input their own quotes for others to read. 
- All of the quotes will be added to a table below all of the image quotes for all users to read.
- Users will be able to edit and delete the quotes they add to the table. 


# How do I plan to code it?

- the frontend will include an HTML5 table with an ID for the form that will be used to send to the backend
- the frontend also consists of the styling and images
- the backend will consist of a class, database, and API in order to send data, store it, and send an updated list back
- Json, Javascript, and HTML will autogenerate the table


# What will be in the video?

- will demonstrate what a user will see when clicking on the inspiration page
    - show the images at the top
    - add a quote to the form
    - show quote being added to the table
    - show a single letter being added to the form
    - show the error message that is returned
    - maybe show the alert inspo message

