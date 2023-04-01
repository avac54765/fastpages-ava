---
title: Collegeboard MCQ Test 4 Reflection
toc: true
comments: true
layout: post
description: Reflecting on my fourth CB MCQ Test
permalink: /CB/MCQ4
image: /images/cbimage.png
categories: [week 28, collegeboard, reflection]
---



# My Overall Score

![MCQ 4 Score]({{site.baseurl}}/images/mcq4score.PNG)

I received a 47/50 on the test. 

This test definitely was challenging in terms of the topics. I feel like I was able to infer for many of the questions I did not know, but I did have to google the definition for heuristic and a little bit about how data is transferred through the internet. I also still take awhile on the questions that involve binary conversions (I am a very slow math person when it comes to powers in my head). I feel that I am improving on my test taking skills though.


# Incorrect Questions

### Question 20- Metadata and data from a call using a cellphone
![Q20]({{site.baseurl}}/images/q20.PNG)

On this question, I was half correct. I just didn't realize that answer 3 was also correct in which suspects can be found from the metadata of certain calls. I got this incorrect because I was thinking that the police would need to be able to hear the calls to generate suspect lists (ex. hear what they are talking about), but it turns out you can generate a list of numbers from the criminal's calls to make the list (anyone they talk to is a suspect).


### Question 37- Efficiency of algorithm to draw shapes
![Q37]({{site.baseurl}}/images/q37.PNG)

On this question, I was correct that the number of steps is approximately equal to n^2. Although due to this being a O(n^2) time complexity, this algorithm does run in a reasonable time.



### Question 49- Traverse list to compare quiz scores
![Q49]({{site.baseurl}}/images/q49pt1.PNG)
![Q49]({{site.baseurl}}/images/q49pt2.PNG)

On this question, I didn't think about the length of the list and how the program will fail to compare the last score. This is due to the program terminating when the index is greater than OR equal to the length of the list meaning the last one is not checked. To fix this, the program would need to say repeat until idex > len, not index >= len.

Answer A starts at the second index and compares ALL of the scores by repeating the list the length of the list (minus one for the initial max score).


# Advice for next time:

The mistakes I am making are just simple misunderstandings that can be easily fixed with a little bit more practice with how the Collegboard questions are asked. I am getting better and better at knowing what these questions are asking. More tips:
    - take time reading all questions and answers
    - try to prove the other options wrong also instead of just finding the first "correct one"
    - think about how a programmer would write a question in a certain scenario 