---
keywords: fastai
description: This is a quiz where you can learn what type of bread you are. Learning your bread "genetics" is life changing and will influence how you think of yourself.
title: What Kind of Bread are You?
toc: true
comments: true
permalink: /bread_quiz/python
image: /images/bread line.jpg
categories: [week 1]
nb_path: _notebooks/2022-08-24-Bread-Quiz.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-08-24-Bread-Quiz.ipynb
-->

<div class="container" id="notebook-container">
        
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Welcome-to-the-quiz,-What-Type-of-Bread-are-You?-Answer-the-questions-below.">Welcome to the quiz, What Type of Bread are You? Answer the questions below.<a class="anchor-link" href="#Welcome-to-the-quiz,-What-Type-of-Bread-are-You?-Answer-the-questions-below."> </a></h2>
</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">white_bread</span> <span class="o">=</span> <span class="mi">0</span>
<span class="n">flat_bread</span> <span class="o">=</span> <span class="mi">0</span>
<span class="n">sourdough_bread</span> <span class="o">=</span> <span class="mi">0</span>

<span class="c1">#defines variables for types of breads and point values</span>


<span class="k">def</span> <span class="nf">question_and_3_answers</span><span class="p">(</span><span class="n">prompt</span><span class="p">,</span> <span class="n">ans1</span><span class="p">,</span> <span class="n">ans2</span><span class="p">,</span> <span class="n">ans3</span><span class="p">):</span>
    <span class="n">answer_correct</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="k">while</span> <span class="n">answer_correct</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Question: &quot;</span> <span class="o">+</span> <span class="n">prompt</span><span class="p">)</span>
        <span class="n">rsp</span> <span class="o">=</span> <span class="nb">input</span><span class="p">()</span>
        <span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="n">ans1</span><span class="p">:</span>
            <span class="k">global</span> <span class="n">white_bread</span>
            <span class="n">white_bread</span> <span class="o">+=</span> <span class="mi">1</span>
            <span class="n">answer_correct</span> <span class="o">=</span> <span class="mi">1</span>
        <span class="k">elif</span> <span class="n">rsp</span> <span class="o">==</span> <span class="n">ans2</span><span class="p">:</span>
            <span class="k">global</span> <span class="n">sourdough_bread</span>
            <span class="n">sourdough_bread</span> <span class="o">+=</span> <span class="mi">1</span>
            <span class="n">answer_correct</span> <span class="o">=</span> <span class="mi">1</span>
        <span class="k">elif</span> <span class="n">rsp</span> <span class="o">==</span> <span class="n">ans3</span><span class="p">:</span>
            <span class="k">global</span> <span class="n">flat_bread</span>
            <span class="n">flat_bread</span> <span class="o">+=</span> <span class="mi">1</span>
            <span class="n">answer_correct</span> <span class="o">=</span> <span class="mi">1</span>
        <span class="k">else</span><span class="p">:</span>
            <span class="nb">print</span><span class="p">(</span><span class="n">rsp</span> <span class="o">+</span> <span class="s2">&quot; is not an answer please try again&quot;</span><span class="p">)</span>
    
<span class="c1">#this is defining my function. I have a prompt and three correct answers- This way I don&#39;t have to type this code five times.</span>
<span class="c1">#if the user types a non-answer, it will loop until they choose a defined answer. Certain answers will add a point to the bread total</span>

<span class="n">question_and_3_answers</span><span class="p">(</span><span class="s2">&quot;What type of friend are you? The mom, rebellious, or quiet friend? Answer with one word.&quot;</span><span class="p">,</span> <span class="s2">&quot;mom&quot;</span><span class="p">,</span> <span class="s2">&quot;rebellious&quot;</span><span class="p">,</span> <span class="s2">&quot;quiet&quot;</span><span class="p">)</span>
<span class="n">question_and_3_answers</span><span class="p">(</span><span class="s2">&quot;What kind of car would you drive? A minivan, Tesla, or Prius? Make sure to type a capital letter if applicable.&quot;</span><span class="p">,</span> <span class="s2">&quot;minivan&quot;</span><span class="p">,</span> <span class="s2">&quot;Tesla&quot;</span><span class="p">,</span> <span class="s2">&quot;Prius&quot;</span><span class="p">)</span>
<span class="n">question_and_3_answers</span><span class="p">(</span><span class="s2">&quot;What activity would you do in your freetime? Would you run errands, party, or read?&quot;</span><span class="p">,</span> <span class="s2">&quot;run errands&quot;</span><span class="p">,</span> <span class="s2">&quot;party&quot;</span><span class="p">,</span> <span class="s2">&quot;read&quot;</span><span class="p">)</span>
<span class="n">question_and_3_answers</span><span class="p">(</span><span class="s2">&quot;What kind of phone do you use? A flip phone, an iphone, or an android?&quot;</span><span class="p">,</span> <span class="s2">&quot;flip phone&quot;</span><span class="p">,</span> <span class="s2">&quot;iphone&quot;</span><span class="p">,</span> <span class="s2">&quot;android&quot;</span><span class="p">)</span>
<span class="n">question_and_3_answers</span><span class="p">(</span><span class="s2">&quot;What pet would you like to own? A cat, a dog, or a fish?&quot;</span><span class="p">,</span><span class="s2">&quot;cat&quot;</span><span class="p">,</span><span class="s2">&quot;dog&quot;</span><span class="p">,</span><span class="s2">&quot;fish&quot;</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Here are your results:   &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">white_bread</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot;/5 whitebread   &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">sourdough_bread</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot;/5 sourdough   &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">flat_bread</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot;/5 flatbread&quot;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Thanks for playing! Now you can live your life knowing your bread genetics! :)&quot;</span><span class="p">)</span>

<span class="c1">#this gives the user results about how much of each bread they are</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Question: What type of friend are you? The mom, rebellious, or quiet friend? Answer with one word.
Question: What kind of car would you drive? A minivan, Tesla, or Prius? Make sure to type a capital letter if applicable.
mom is not an answer please try again
Question: What kind of car would you drive? A minivan, Tesla, or Prius? Make sure to type a capital letter if applicable.
Question: What activity would you do in your freetime? Would you run errands, party, or read?
Question: What kind of phone do you use? A flip phone, an iphone, or an android?
Question: What pet would you like to own? A cat, a dog, or a fish?
Here are your results:   1/5 whitebread   2/5 sourdough   2/5 flatbread
Thanks for playing! Now you can live your life knowing your bread genetics! :)
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 

