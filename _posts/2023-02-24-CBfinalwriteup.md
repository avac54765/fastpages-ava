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
    - This program is meant to motivate users to workout and never give up.
    - The functionality of my program is for users to input their own motivational quotes into a table and be able to see others' quotes as well.
    - The user inputs a quote by typing a quote longer than two characters and clicking submit.
    - The output of my program is the addition of the user's quote in a table above where they entered their quote.
<br>
- Row 2 (Data Abstraction):
    ![Class Code]({{site.baseurl}}/images/inspoclass.png)
    ![SQlite table]({{site.baseurl}}/images/sqinspotable.png)
    ![Read Frontend]({{site.baseurl}}/images/readfrontend.png)
    - My data is collected in a database with a class titled Inspo. The data within this class is portrayed in this SQlite table titled Inspo_data.
    - The data represented in this database are the various quotes that users have inputted (are shown in a table in frontend). 
    
<br>
- Row 3 (Managing Complexity):
    ![Class Code]({{site.baseurl}}/images/inspoclass.png)
    ![SQlite table]({{site.baseurl}}/images/sqinspotable.png)
    - Without the use of this database to collect the quotes, the inputted quotes would only be stored locally in a very disorganized manner. This disorganized alternative would include the use of a list in the backend that stores the quotes and would call a rest API to connect the frontend and backend. Although, a programmer would need to individually add all of the quotes to this list in the backend directly. This use of a list would make it much more difficult to see the stored data, debug, update, and access specific quotes.
<br>
- Row 4 (Procedural Abstraction):
    - Procedure: create_quote
    ![procedure]({{site.baseurl}}/images/create_quote_defined.png)
        procedure called:
         ![procedure called]({{site.baseurl}}/images/create_quote.png)
    - This procedure is in charge of taking the submitted quote(parameter) from the form, changing the data into javascript format, and sending it to the backend to be added to the database (POST). Without this function, the inputted quotes would not be stored and seen from the frontend.
<br>
- Row 5 (Algorithm Implentation):
    - ![API Read class]({{site.baseurl}}/images/defget.png)
    ![Frontend Read]({{site.baseurl}}/images/databasecreateerror.png)
    - This Read class is in charge of taking existing data in the database, changing it into json data, and sending it to the frontend to be read. This "get" function sequences through three steps to retrieve and change the format of the quotes. First, the function retrieves all the data from the database. Then the function iterates through all of the quotes that have been retrieved, turning them into json ready data. Finally the data is turned into json to be sent to the frontend. The frontend uses the function read_Inspos to reference the Read class from the API. The data sent from the API is then tested for any response errors. If the condition is met, an error response will be returned. If not, the function will continue to the next step of actually adding the quotes to the table in the frontend. 
<br>
- Row 6 (Testing):
    - First call: In my video, the user inputs a the quote "Be prepared!" into the form and clicks submit.
        - conditions being tested: Checks if the quote is valid (greater than two characters) and if it is successfully added to the database and fetched from the frontend.
        - result: The quote appears in the table above the form, and stays once refreshed.
    - Second call: The user enters nothing into the form and clicks submit.
        - Conditions being tested: The quote is checked for a minimum length of two characters.
        - result: Due to the invalidity of quote, the program will alert the user "Please fill out this field".



    - Third call LOCAL HOST ONLY RN: The user enters "h" into the form.
        - Conditions being tested: The quote is checked for a minimum length of two characters.
        - result: Due to the invalidity of quote, the program will alert the user "Quote is too short, please refresh and enter a longer quote" at the top of their screen.