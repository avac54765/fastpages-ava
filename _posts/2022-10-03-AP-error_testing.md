---
keywords: fastai
description: Practice with identifying and correcting code blocks
title: Big Idea 1 'Identifying and Correcting Errors'
toc: true
comments: true
permalink: /collegeboard/error
image: /images/error.jpg
categories: [week 7]
nb_path: _notebooks/2022-10-03-AP-error_testing.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-10-03-AP-error_testing.ipynb
-->

<div class="container" id="notebook-container">
        
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a href="https://apclassroom.collegeboard.org/103/home?unit=1">College Board Big Idea 1</a></p>
<h2 id="Identifying-and-Correcting-Errors-(Unit-1.4)">Identifying and Correcting Errors (Unit 1.4)<a class="anchor-link" href="#Identifying-and-Correcting-Errors-(Unit-1.4)"> </a></h2><blockquote><p>Become familiar with types of errors and strategies to fixing them</p>
<ul>
<li>Lightly Review Videos and take notes on topics with Blog</li>
<li>Complete assigned MCQ questions</li>
</ul>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Here-are-some-code-segments-you-can-practice-fixing:">Here are some code segments you can practice fixing:<a class="anchor-link" href="#Here-are-some-code-segments-you-can-practice-fixing:"> </a></h1>
</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">alphabet</span> <span class="o">=</span> <span class="s2">&quot;abcdefghijklmnopqrstuvwxyz&quot;</span>

<span class="n">alphabetList</span> <span class="o">=</span> <span class="p">[]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">alphabet</span><span class="p">:</span>
    <span class="n">alphabetList</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">alphabetList</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[&#39;a&#39;, &#39;b&#39;, &#39;c&#39;, &#39;d&#39;, &#39;e&#39;, &#39;f&#39;, &#39;g&#39;, &#39;h&#39;, &#39;i&#39;, &#39;j&#39;, &#39;k&#39;, &#39;l&#39;, &#39;m&#39;, &#39;n&#39;, &#39;o&#39;, &#39;p&#39;, &#39;q&#39;, &#39;r&#39;, &#39;s&#39;, &#39;t&#39;, &#39;u&#39;, &#39;v&#39;, &#39;w&#39;, &#39;x&#39;, &#39;y&#39;, &#39;z&#39;]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The intended outcome is to determine where the letter is in the alphabet using a while loop</p>
<ul>
<li>What is a good test case to check the current outcome? Why?</li>
<li>Make changes to get the intended outcome.</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">letter</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;What letter would you like to check?&quot;</span><span class="p">)</span>

<span class="n">i</span> <span class="o">=</span> <span class="mi">0</span>

<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;</span> <span class="mi">26</span><span class="p">:</span>
    <span class="k">if</span> <span class="n">alphabetList</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">==</span> <span class="n">letter</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;The letter &quot;</span> <span class="o">+</span> <span class="n">letter</span> <span class="o">+</span> <span class="s2">&quot; is the &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot; letter in the alphabet&quot;</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">1</span>

<span class="c1"># the count was off due to computer counting, so we added +1 to the string</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>The letter c is the 3 letter in the alphabet
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The intended outcome is to determine where the letter is in the alphabet using a for loop</p>
<ul>
<li>What is a good test case to check the current outcome? Why?</li>
<li>Make changes to get the intended outcome.</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">letter</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;What letter would you like to check?&quot;</span><span class="p">)</span>

<span class="n">count</span> <span class="o">=</span> <span class="mi">1</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">alphabetList</span><span class="p">:</span>
    <span class="k">if</span> <span class="n">i</span> <span class="o">==</span> <span class="n">letter</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;The letter &quot;</span> <span class="o">+</span> <span class="n">letter</span> <span class="o">+</span> <span class="s2">&quot; is the &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">count</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot; letter in the alphabet&quot;</span><span class="p">)</span>
    <span class="n">count</span> <span class="o">+=</span> <span class="mi">1</span>

<span class="c1"># the count variable was defined in the loop, but was moved out of the loop</span>
<span class="c1"># the count was also off so we defined count =1 and not 0</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>The letter z is the 26 letter in the alphabet
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This code outputs the even numbers from 0 - 10 using a while loop.</p>
<ul>
<li>Analyze this code to determine what can be changed to get the outcome to be odd numbers. (Code block below)</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">evens</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">i</span> <span class="o">=</span> <span class="mi">0</span>

<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;=</span> <span class="mi">10</span><span class="p">:</span>
    <span class="n">evens</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">2</span>

<span class="nb">print</span><span class="p">(</span><span class="n">evens</span><span class="p">)</span>    
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[0, 2, 4, 6, 8, 10]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This code should output the odd numbers from 0 - 10 using a while loop.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">odds</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">i</span> <span class="o">=</span> <span class="mi">1</span>

<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;=</span> <span class="mi">10</span><span class="p">:</span>
    <span class="n">odds</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">2</span>

<span class="nb">print</span><span class="p">(</span><span class="n">odds</span><span class="p">)</span>

<span class="c1">#this was printing the evens still, so we had to set i=1 not 0</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[1, 3, 5, 7, 9]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This code outputs the even numbers from 0 - 10 using a for loop.</p>
<ul>
<li>Analyze this code to determine what can be changed to get the outcome to be odd numbers. (Code block below)</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">numbers</span> <span class="o">=</span> <span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">3</span><span class="p">,</span><span class="mi">4</span><span class="p">,</span><span class="mi">5</span><span class="p">,</span><span class="mi">6</span><span class="p">,</span><span class="mi">7</span><span class="p">,</span><span class="mi">8</span><span class="p">,</span><span class="mi">9</span><span class="p">,</span><span class="mi">10</span><span class="p">]</span>
<span class="n">evens</span> <span class="o">=</span> <span class="p">[]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">numbers</span><span class="p">:</span>
    <span class="k">if</span> <span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">0</span><span class="p">):</span>
        <span class="n">evens</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>

<span class="nb">print</span><span class="p">(</span><span class="n">evens</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[0, 2, 4, 6, 8, 10]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This code should output the odd numbers from 0 - 10 using a for loop.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">numbers</span> <span class="o">=</span> <span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">3</span><span class="p">,</span><span class="mi">4</span><span class="p">,</span><span class="mi">5</span><span class="p">,</span><span class="mi">6</span><span class="p">,</span><span class="mi">7</span><span class="p">,</span><span class="mi">8</span><span class="p">,</span><span class="mi">9</span><span class="p">,</span><span class="mi">10</span><span class="p">]</span>
<span class="n">odds</span> <span class="o">=</span> <span class="p">[]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">numbers</span><span class="p">:</span>
    <span class="k">if</span> <span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">1</span><span class="p">):</span>
        <span class="n">odds</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>

<span class="nb">print</span><span class="p">(</span><span class="n">odds</span><span class="p">)</span>

<span class="c1"># changed the remainder from 0 to 1 </span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[1, 3, 5, 7, 9]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The intended outcome is printing a number between 1 and 100 once, if it is a multiple of 2 or 5</p>
<ul>
<li>What values are outputted incorrectly. Why?</li>
<li>Make changes to get the intended outcome.</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">numbers</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">newNumbers</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">i</span> <span class="o">=</span> <span class="mi">0</span>

<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;</span> <span class="mi">100</span><span class="p">:</span>
    <span class="n">numbers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">1</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">numbers</span><span class="p">:</span>
    <span class="k">if</span> <span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="k">pass</span>
    <span class="k">elif</span> <span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">5</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="n">newNumbers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
    <span class="k">elif</span> <span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="n">newNumbers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>

<span class="nb">print</span><span class="p">(</span><span class="n">newNumbers</span><span class="p">)</span> 

<span class="c1">#change second if statement to elif to get rid of repeats (else if)</span>
<span class="c1">#to get rid of zero, add either continue, or add pass and add elif= if the number is zero it skips</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[2, 4, 5, 6, 8, 10, 12, 14, 15, 16, 18, 20, 22, 24, 25, 26, 28, 30, 32, 34, 35, 36, 38, 40, 42, 44, 45, 46, 48, 50, 52, 54, 55, 56, 58, 60, 62, 64, 65, 66, 68, 70, 72, 74, 75, 76, 78, 80, 82, 84, 85, 86, 88, 90, 92, 94, 95, 96, 98]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Challenge">Challenge<a class="anchor-link" href="#Challenge"> </a></h1><p>This code segment is at a very early stage of implementation.</p>
<ul>
<li>What are some ways to (user) error proof this code?</li>
<li>The code should be able to calculate the cost of the meal of the user</li>
</ul>
<p>Hint:</p>
<ul>
<li>write a “single” test describing an expectation of the program of the program</li>
<li>test - input burger, expect output of burger price</li>
<li>run the test, which should fail because the program lacks that feature</li>
<li>write “just enough” code, the simplest possible, to make the test pass</li>
</ul>
<p>Then repeat this process until you get program working like you want it to work.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">menu</span> <span class="o">=</span>  <span class="p">{</span><span class="s2">&quot;burger&quot;</span><span class="p">:</span> <span class="mf">3.99</span><span class="p">,</span>
         <span class="s2">&quot;fries&quot;</span><span class="p">:</span> <span class="mf">1.99</span><span class="p">,</span>
         <span class="s2">&quot;drink&quot;</span><span class="p">:</span> <span class="mf">0.99</span><span class="p">}</span>
<span class="n">total</span> <span class="o">=</span> <span class="mi">0</span>
<span class="n">wholeordertotal</span> <span class="o">=</span> <span class="mi">0</span>


<span class="c1">#shows the user the menu and prompts them to select an item</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Menu&quot;</span><span class="p">)</span>
<span class="k">for</span> <span class="n">k</span><span class="p">,</span><span class="n">v</span> <span class="ow">in</span> <span class="n">menu</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">k</span> <span class="o">+</span> <span class="s2">&quot;  $&quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">v</span><span class="p">))</span> <span class="c1">#why does v have &quot;str&quot; in front of it?</span>
    
<span class="c1">#ideally the code should prompt the user multiple times</span>
<span class="n">item</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;Please select an item from the menu&quot;</span><span class="p">)</span>

<span class="c1">#below the total is = to the value of the item typed in</span>
<span class="n">total</span> <span class="o">=</span> <span class="n">menu</span><span class="p">[</span><span class="n">item</span><span class="p">]</span>

<span class="c1">#below is the total for someone who orders the whole menu</span>
<span class="k">for</span> <span class="n">k</span> <span class="ow">in</span> <span class="n">menu</span><span class="p">:</span>
    <span class="n">wholeordertotal</span> <span class="o">=</span> <span class="n">wholeordertotal</span> <span class="o">+</span> <span class="n">menu</span><span class="p">[</span><span class="n">k</span><span class="p">]</span>

<span class="c1">#code should add the price of the menu items selected by the user </span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;You owe: $&quot;</span><span class="p">,</span> <span class="n">total</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Do you want everything?: $&quot;</span><span class="p">,</span> <span class="n">wholeordertotal</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Menu
burger  $3.99
fries  $1.99
drink  $0.99
You owe: $ 3.99
Do you want everything?: $ 6.970000000000001
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Adding-up-the-total-with-multiple-items:">Adding up the total with multiple items:<a class="anchor-link" href="#Adding-up-the-total-with-multiple-items:"> </a></h1>
</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">ast</span> <span class="kn">import</span> <span class="n">While</span>


<span class="n">menu</span> <span class="o">=</span>  <span class="p">{</span><span class="s2">&quot;burger&quot;</span><span class="p">:</span> <span class="mf">3.99</span><span class="p">,</span>
         <span class="s2">&quot;fries&quot;</span><span class="p">:</span> <span class="mf">1.99</span><span class="p">,</span>
         <span class="s2">&quot;drink&quot;</span><span class="p">:</span> <span class="mf">0.99</span><span class="p">}</span>
<span class="n">total</span> <span class="o">=</span> <span class="mi">0</span>


<span class="c1">#shows the user the menu and prompts them to select an item</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Menu&quot;</span><span class="p">)</span>
<span class="k">for</span> <span class="n">k</span><span class="p">,</span><span class="n">v</span> <span class="ow">in</span> <span class="n">menu</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">k</span> <span class="o">+</span> <span class="s2">&quot;  $&quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">v</span><span class="p">))</span> <span class="c1">#why does v have &quot;str&quot; in front of it?</span>

<span class="c1">#this definition of item is temporary and is just used to item is defined before the function</span>
<span class="n">item</span> <span class="o">=</span> <span class="s2">&quot;temporary value&quot;</span>    

<span class="k">while</span> <span class="n">item</span> <span class="o">!=</span> <span class="s2">&quot;&quot;</span><span class="p">:</span> <span class="c1">#!= means not equal to</span>
    <span class="c1">#this code prompts the user multiple times until they simply click enter without an input</span>
    <span class="n">item</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;Please select an item from the menu&quot;</span><span class="p">)</span>
    <span class="k">if</span> <span class="n">item</span> <span class="o">!=</span><span class="s2">&quot;&quot;</span><span class="p">:</span>
        <span class="n">total</span> <span class="o">=</span> <span class="n">total</span> <span class="o">+</span> <span class="n">menu</span><span class="p">[</span><span class="n">item</span><span class="p">]</span> <span class="c1">#this adds up the total of the previous item(s) and the new item</span>

        <span class="c1">#this loop will continue until the user enters with no input</span>



<span class="c1">#code should add the price of the menu items selected by the user </span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;You owe: $&quot;</span><span class="p">,</span> <span class="n">total</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Menu
burger  $3.99
fries  $1.99
drink  $0.99
You owe: $ 5.98
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 

