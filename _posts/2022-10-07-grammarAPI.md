---
keywords: fastai
description: This API provides data about spelling and grammar checks.
title: Grammar API
toc: true
comments: true
permalink: /grammarAPI/python
image: /images/API.png
categories: [week 7]
nb_path: _notebooks/2022-10-07-grammarAPI.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-10-07-grammarAPI.ipynb
-->

<div class="container" id="notebook-container">
        
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="The-Different-Languages-Offered:">The Different Languages Offered:<a class="anchor-link" href="#The-Different-Languages-Offered:"> </a></h1>
</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">requests</span>

<span class="n">url</span> <span class="o">=</span> <span class="s2">&quot;https://dnaber-languagetool.p.rapidapi.com/v2/languages&quot;</span>

<span class="n">headers</span> <span class="o">=</span> <span class="p">{</span>
	<span class="s2">&quot;X-RapidAPI-Key&quot;</span><span class="p">:</span> <span class="s2">&quot;7b146afe20msh92e84c02ae27c6ap1185b5jsnb7a574f24cbe&quot;</span><span class="p">,</span>
	<span class="s2">&quot;X-RapidAPI-Host&quot;</span><span class="p">:</span> <span class="s2">&quot;dnaber-languagetool.p.rapidapi.com&quot;</span>
<span class="p">}</span>

<span class="n">response</span> <span class="o">=</span> <span class="n">requests</span><span class="o">.</span><span class="n">request</span><span class="p">(</span><span class="s2">&quot;GET&quot;</span><span class="p">,</span> <span class="n">url</span><span class="p">,</span> <span class="n">headers</span><span class="o">=</span><span class="n">headers</span><span class="p">)</span>

<span class="c1"># print(response.text)</span>


<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Languages Supported&quot;</span><span class="p">)</span>
<span class="n">languagelist</span> <span class="o">=</span> <span class="n">response</span><span class="o">.</span><span class="n">json</span><span class="p">()</span> 


<span class="k">for</span> <span class="n">language</span> <span class="ow">in</span> <span class="n">languagelist</span><span class="p">:</span>
	<span class="nb">print</span><span class="p">(</span><span class="n">language</span><span class="p">[</span><span class="s2">&quot;name&quot;</span><span class="p">],</span> <span class="s2">&quot; = &quot;</span><span class="p">,</span> <span class="n">language</span><span class="p">[</span><span class="s2">&quot;code&quot;</span><span class="p">])</span> <span class="c1">#this code is used in the next step to check the grammer in a specified language</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Languages Supported
Arabic  =  ar
Asturian  =  ast
Belarusian  =  be
Breton  =  br
Catalan  =  ca
Catalan (Valencian)  =  ca
Chinese  =  zh
Danish  =  da
Dutch  =  nl
Dutch  =  nl
Dutch (Belgium)  =  nl
English  =  en
English  =  en
English (Australian)  =  en
English (Australian)  =  en
English (Canadian)  =  en
English (Canadian)  =  en
English (GB)  =  en
English (GB)  =  en
English (New Zealand)  =  en
English (New Zealand)  =  en
English (South African)  =  en
English (South African)  =  en
English (US)  =  en
English (US)  =  en
Esperanto  =  eo
French  =  fr
French  =  fr
Galician  =  gl
German  =  de
German  =  de
German (Austria)  =  de
German (Austria)  =  de
German (Germany)  =  de
German (Germany)  =  de
German (Swiss)  =  de
German (Swiss)  =  de
Greek  =  el
Irish  =  ga
Italian  =  it
Japanese  =  ja
Khmer  =  km
Norwegian (Bokm??l)  =  nb
Norwegian (Bokm??l)  =  no
Persian  =  fa
Polish  =  pl
Portuguese  =  pt
Portuguese (Angola preAO)  =  pt
Portuguese (Angola preAO)  =  pt
Portuguese (Brazil)  =  pt
Portuguese (Brazil)  =  pt
Portuguese (Mo??ambique preAO)  =  pt
Portuguese (Mo??ambique preAO)  =  pt
Portuguese (Portugal)  =  pt
Portuguese (Portugal)  =  pt
Romanian  =  ro
Russian  =  ru
Simple German  =  de-DE-x-simple-language
Slovak  =  sk
Slovenian  =  sl
Spanish  =  es
Spanish  =  es
Spanish (voseo)  =  es
Swedish  =  sv
Tagalog  =  tl
Tamil  =  ta
Ukrainian  =  uk
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Below-is-the-proccess-of-getting-text-checked-gramatically.-The-result-displayed-is-the-error-and-possible-reccomendations-to-change">Below is the proccess of getting text checked gramatically. The result displayed is the error and possible reccomendations to change<a class="anchor-link" href="#Below-is-the-proccess-of-getting-text-checked-gramatically.-The-result-displayed-is-the-error-and-possible-reccomendations-to-change"> </a></h1>
</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">requests</span>
<span class="kn">import</span> <span class="nn">json</span>

<span class="n">url</span> <span class="o">=</span> <span class="s2">&quot;https://dnaber-languagetool.p.rapidapi.com/v2/check&quot;</span>

<span class="n">payload</span> <span class="o">=</span> <span class="s2">&quot;language=en-US&amp;text=&quot;</span> <span class="c1">#because of use of code&#39;eu&#39; this is checking in English</span>
<span class="n">headers</span> <span class="o">=</span> <span class="p">{</span>
	<span class="s2">&quot;content-type&quot;</span><span class="p">:</span> <span class="s2">&quot;application/x-www-form-urlencoded&quot;</span><span class="p">,</span>
	<span class="s2">&quot;X-RapidAPI-Key&quot;</span><span class="p">:</span> <span class="s2">&quot;7b146afe20msh92e84c02ae27c6ap1185b5jsnb7a574f24cbe&quot;</span><span class="p">,</span>
	<span class="s2">&quot;X-RapidAPI-Host&quot;</span><span class="p">:</span> <span class="s2">&quot;dnaber-languagetool.p.rapidapi.com&quot;</span>
<span class="p">}</span>

<span class="n">text</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;Please enter the text you would like checked&quot;</span><span class="p">)</span>

<span class="n">payload</span> <span class="o">+=</span> <span class="n">text</span> <span class="c1">#this appends the string defined above to add the text needing to be checked</span>

<span class="n">response</span> <span class="o">=</span> <span class="n">requests</span><span class="o">.</span><span class="n">request</span><span class="p">(</span><span class="s2">&quot;POST&quot;</span><span class="p">,</span> <span class="n">url</span><span class="p">,</span> <span class="n">data</span><span class="o">=</span><span class="n">payload</span><span class="p">,</span> <span class="n">headers</span><span class="o">=</span><span class="n">headers</span><span class="p">)</span>

<span class="c1"># print(response.text)</span>


<span class="c1">#print(json.dumps(response.json(), indent=4))</span>

<span class="nb">print</span><span class="p">(</span><span class="n">json</span><span class="o">.</span><span class="n">dumps</span><span class="p">(</span><span class="n">response</span><span class="o">.</span><span class="n">json</span><span class="p">()[</span><span class="s2">&quot;matches&quot;</span><span class="p">],</span> <span class="n">indent</span><span class="o">=</span><span class="mi">4</span><span class="p">))</span> <span class="c1">#the json.dumps formats the data to be prettier :)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[
    {
        &#34;message&#34;: &#34;This sentence does not start with an uppercase letter.&#34;,
        &#34;shortMessage&#34;: &#34;&#34;,
        &#34;replacements&#34;: [
            {
                &#34;value&#34;: &#34;Hello&#34;
            }
        ],
        &#34;offset&#34;: 0,
        &#34;length&#34;: 5,
        &#34;context&#34;: {
            &#34;text&#34;: &#34;hello my nme is&#34;,
            &#34;offset&#34;: 0,
            &#34;length&#34;: 5
        },
        &#34;sentence&#34;: &#34;hello my nme is&#34;,
        &#34;type&#34;: {
            &#34;typeName&#34;: &#34;Other&#34;
        },
        &#34;rule&#34;: {
            &#34;id&#34;: &#34;UPPERCASE_SENTENCE_START&#34;,
            &#34;description&#34;: &#34;Checks that a sentence starts with an uppercase letter&#34;,
            &#34;issueType&#34;: &#34;typographical&#34;,
            &#34;urls&#34;: [
                {
                    &#34;value&#34;: &#34;https://languagetool.org/insights/post/spelling-capital-letters/&#34;
                }
            ],
            &#34;category&#34;: {
                &#34;id&#34;: &#34;CASING&#34;,
                &#34;name&#34;: &#34;Capitalization&#34;
            },
            &#34;isPremium&#34;: false
        },
        &#34;ignoreForIncompleteSentence&#34;: true,
        &#34;contextForSureMatch&#34;: -1
    },
    {
        &#34;message&#34;: &#34;Possible spelling mistake found.&#34;,
        &#34;shortMessage&#34;: &#34;Spelling mistake&#34;,
        &#34;replacements&#34;: [
            {
                &#34;value&#34;: &#34;me&#34;
            },
            {
                &#34;value&#34;: &#34;name&#34;
            },
            {
                &#34;value&#34;: &#34;NMR&#34;
            },
            {
                &#34;value&#34;: &#34;CME&#34;
            },
            {
                &#34;value&#34;: &#34;nee&#34;
            },
            {
                &#34;value&#34;: &#34;DME&#34;
            },
            {
                &#34;value&#34;: &#34;Mme&#34;
            },
            {
                &#34;value&#34;: &#34;Nome&#34;
            },
            {
                &#34;value&#34;: &#34;SME&#34;
            },
            {
                &#34;value&#34;: &#34;BME&#34;
            },
            {
                &#34;value&#34;: &#34;Noe&#34;
            },
            {
                &#34;value&#34;: &#34;nae&#34;
            },
            {
                &#34;value&#34;: &#34;n\u00e9e&#34;
            },
            {
                &#34;value&#34;: &#34;AME&#34;
            },
            {
                &#34;value&#34;: &#34;EME&#34;
            },
            {
                &#34;value&#34;: &#34;IME&#34;
            },
            {
                &#34;value&#34;: &#34;JME&#34;
            },
            {
                &#34;value&#34;: &#34;LME&#34;
            },
            {
                &#34;value&#34;: &#34;ME&#34;
            },
            {
                &#34;value&#34;: &#34;Me&#34;
            },
            {
                &#34;value&#34;: &#34;NCE&#34;
            },
            {
                &#34;value&#34;: &#34;NE&#34;
            },
            {
                &#34;value&#34;: &#34;NEE&#34;
            },
            {
                &#34;value&#34;: &#34;NGE&#34;
            },
            {
                &#34;value&#34;: &#34;NM&#34;
            },
            {
                &#34;value&#34;: &#34;NMA&#34;
            },
            {
                &#34;value&#34;: &#34;NMF&#34;
            },
            {
                &#34;value&#34;: &#34;NMI&#34;
            },
            {
                &#34;value&#34;: &#34;NMM&#34;
            },
            {
                &#34;value&#34;: &#34;NMT&#34;
            },
            {
                &#34;value&#34;: &#34;NOE&#34;
            },
            {
                &#34;value&#34;: &#34;Ne&#34;
            },
            {
                &#34;value&#34;: &#34;PME&#34;
            },
            {
                &#34;value&#34;: &#34;RME&#34;
            },
            {
                &#34;value&#34;: &#34;TME&#34;
            },
            {
                &#34;value&#34;: &#34;VME&#34;
            },
            {
                &#34;value&#34;: &#34;n me&#34;
            },
            {
                &#34;value&#34;: &#34;NMC&#34;
            },
            {
                &#34;value&#34;: &#34;NVMe&#34;
            },
            {
                &#34;value&#34;: &#34;Nye&#34;
            },
            {
                &#34;value&#34;: &#34;nm&#34;
            },
            {
                &#34;value&#34;: &#34;n\u00e9&#34;
            }
        ],
        &#34;offset&#34;: 9,
        &#34;length&#34;: 3,
        &#34;context&#34;: {
            &#34;text&#34;: &#34;hello my nme is&#34;,
            &#34;offset&#34;: 9,
            &#34;length&#34;: 3
        },
        &#34;sentence&#34;: &#34;hello my nme is&#34;,
        &#34;type&#34;: {
            &#34;typeName&#34;: &#34;Other&#34;
        },
        &#34;rule&#34;: {
            &#34;id&#34;: &#34;MORFOLOGIK_RULE_EN_US&#34;,
            &#34;description&#34;: &#34;Possible spelling mistake&#34;,
            &#34;issueType&#34;: &#34;misspelling&#34;,
            &#34;category&#34;: {
                &#34;id&#34;: &#34;TYPOS&#34;,
                &#34;name&#34;: &#34;Possible Typo&#34;
            },
            &#34;isPremium&#34;: false
        },
        &#34;ignoreForIncompleteSentence&#34;: false,
        &#34;contextForSureMatch&#34;: 0
    }
]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 

