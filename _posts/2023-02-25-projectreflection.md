---
title: Individual Collegeboard CPT Write-Up
toc: true
comments: true
layout: post
description: CB CPT project reflection
permalink: /project/reflection
image: /images/cbimage.pn
categories: [week 24, collegeboard, write-up, project, reflection]
---


# The Struggles of Backend
> No one will ever know the struggle it was and the journey that my group has been through to get where we are with backend. 

### Our Timeline

1. My group started off with only having one repository for both backend and frontend. 
2. My group figured out how to use the user database and api to create individual classes under the same api for each of our features. We used this knowledge to eventually create our own databases. 
3. Once we figured this step out, we created a backend repository and dragged our files into this repository (sorry mort we didn't realize we needed a separate backend oopsie). Once we did this we were able to use local hosts to try and connect frontend and backend. We had an issue with CORS with localhost to localhost but we were able to comment out the CORS lines in our main.py until we deployed using AWS.
4. Before full-stack worked, we had a lot of issues to debug. We spent hours fixing one database and making the same edits on everyone elses databases. It took a lot of teamwork to help each other fix our issues and typos. It felt like once something would work, something else would go wrong (we had to stay sane and help each other). 
5. After we got local full stack working, it was time to deploy. Deploying was confusing with AWS, but was much more simple once we got the guide. Unfortunately our group had issues with our site crashing when we tried to deploy. Main.py would run and successfully run a localhost, but our curl would not work. Thank you Mr. Mort for helping us fix an issue with each of our databases to make this work. Sri spent a lot of time getting our backend deployed when Alexa and I were in Texas. 
6. When is comes to adding features, my group spent hours together experimenting and trying new things. We figured out how to have an alert for specific errors to tell a user what they entered incorrectly (garbage data), but soon learned that it does not work with CORS when deployed (only works with local to local full stack). We did add new garbage data filters in the backend as well. Our features have similar structures so we were able to share ideas and debug together. 
7. Our main.py stopped working when a teammate tried to edit their code, so we went back to an older version of their code. Unfortunately, do so caused our site to crash, so we took a lot of time to figure out where the edit was needed to fix the site. The hard part about a team project is that when the site works, one member can change something and cause the site to crash for everyone. AWS was also down for awhile due to an incorrect Nginx file, but someone thankfully fixed the error.
8. Here we are today with running, deployed frontend and backend servers. Full stack works for everyone and we were all able to create our collegeboard videos and write-ups. 


# Backend Specifics

### My Inspo Database and Class

![Inspo Database]({{site.baseurl}}/images/inspodatabase.png)
![Inspo SQlite table]({{site.baseurl}}/images/insposqlite.png)

Above is my class for my inspiration database. This database stores all of the quotes that users send in from the frontend. This class is in charge of creating columns for each of the quotes, the user IDs, and user UIDs. 

![Inspo API]({{site.baseurl}}/images/inspodatabase.png)
