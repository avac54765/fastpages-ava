---
keywords: fastai
description: Fibonacci's sequence is a famous sequence in which the "n"th term is the previous two terms added together. Here I am programing this sequence using a recursive loop.
title: Fibonacci's Sequence with a Recursive Loop
toc: true
comments: true
permalink: /fibonacci/python
image: /images/newfibonacci.png
categories: [week 2]
nb_path: _notebooks/2022-09-06-fibonacci.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-09-06-fibonacci.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">fibonacci_loop</span><span class="p">(</span><span class="n">n</span><span class="p">):</span>
    <span class="k">if</span> <span class="n">n</span> <span class="o">&lt;=</span> <span class="mi">1</span><span class="p">:</span>
        <span class="k">return</span> <span class="n">n</span> <span class="c1">#you must return n if n&lt;=1 otherwise term will be negative</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="k">return</span><span class="p">(</span><span class="n">fibonacci_loop</span><span class="p">(</span><span class="n">n</span><span class="o">-</span><span class="mi">1</span><span class="p">)</span> <span class="o">+</span> <span class="n">fibonacci_loop</span><span class="p">(</span><span class="n">n</span><span class="o">-</span><span class="mi">2</span><span class="p">))</span>


<span class="n">nterms</span><span class="o">=</span> <span class="mi">10</span> <span class="c1">#the user can put a term number in here and this loop will list the terms in the fibonacci sequence until that term</span>

<span class="k">if</span> <span class="n">nterms</span> <span class="o">&lt;=</span> <span class="mi">0</span><span class="p">:</span> <span class="c1">#term cannot be negative</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Please enter a positive integer. Negatives are not accepted.&quot;</span><span class="p">)</span>
<span class="k">else</span><span class="p">:</span>
    <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">nterms</span><span class="p">):</span> <span class="c1">#if the integer is positive, the function will be able to list until &quot;n&quot;th term</span>
        <span class="nb">print</span><span class="p">(</span><span class="n">fibonacci_loop</span><span class="p">(</span><span class="n">i</span><span class="p">))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>0
1
1
2
3
5
8
13
21
34
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 
