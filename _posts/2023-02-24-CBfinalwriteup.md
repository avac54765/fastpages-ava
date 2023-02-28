---
title: Individual Collegeboard CPT Write-Up
toc: true
comments: true
layout: post
description: CB CPT write-up
permalink: /project/write-up
image: /images/cbimage.png
categories: [week 24, collegeboard, write-up, project]
---


# Collegeboard Write up
> Below is my CB write-up for my CPT section of my team's fitness project. 

[I am using these scoring guidelines to organize my write-up.](https://apcentral.collegeboard.org/media/pdf/ap22-sg-computer-science-principles.pdf)

[Here is a link to my video]()



- Row 1 (Program Purpose and Function):
    - the purpose of my program is to aid ISPE students to stay organized and ensure they get credit for their class
    - my program works (functionality) by allowing users to input their workouts and corresponding grade, and see the following inputs on the page in an organized table
    - the user inputs a workout by typing their "Name", "Date of Completion", "Number of Hours Completed", "Grade" and click submit
    - the output of the program is that the data appears in a table below
<br>
- Row 2 (Data Abstraction):
    - name of collection type (database class): ISPE
    - data in this class is the data (workouts) that the user inputed
<br>
- Row 3 (Managing Complexity):
    - without the use of the class in the database, the inputed data would be very unorganized in a list and would only be stored locally. However, I could store the data in a list and use a rest API to connect the frontend and backend.
<br>
- Row 4 (Procedural Abstraction):
    - Show a procedure in creating the API or database?
    - the API and database are critical to this project since they allow data to be stored (not just locally) and connect the inputs from the frontend to the backend (data a user inputs will show up in table and stay there even when page is refreshed)
<br>
- Row 5 (Algorithm Implentation):
    - we haven't finished our code yet
    - describe process of input getting posted to the backend, getting stored in the database, and then sent back to the frontend (table) in JSON format using the API
<br>
- Row 6 (Testing):
    - First call: user inputs a workout into the form and clicks submit
        - conditions being tested: checks if data is valid and if it can be added to the database
        - result: data will appear in the table below with the corresponding grade
    - Second call: user enters invalid (garbage) data into the field: "number of hours completed"
        - Conditions being tested: checks if the data inputted is valid (numerical number) to be put in the database
        - result: the program will return the message "please enter a valid number"