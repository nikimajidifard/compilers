---
layout: page
title: Lectures
permalink: /lectures/
---

You can download the lectures here (in PDF format). I will try to upload lectures prior to their corresponding classes.


<table>
  <tr>
    <th>EVENT</th>
    <th>DESCRIPTION</th>
  </tr>
  <tr>
    <td>The Procedure Abstraction; Run-Time Storage Organisation</td>
    <td> slides<p>open the slides <a href="/compilers/static_files/materials/lec/Subprgm-RuntimeOrg.pdf">here</a>.</p></td>
  </tr>
  <tr>
    <td>Recursive Descent Parsing</td>
    <td> slides<p>open the slides <a href="/compilers/static_files/materials/lec/parsing1.pdf">here</a>.</p></td>
  </tr>
  <tr>
    <td>LR Parser Construction</td>
    <td> slides<p>open the slides <a href="/compilers/static_files/materials/lec/LR.pdf">here</a>.</p></td>
  </tr>
  <tr>
    <td>Intermediate Representations(IR)</td>
    <td> slides<p>open the slides <a href="/compilers/static_files/materials/lec/IR.pdf">here</a>.</p></td>
  </tr>

  <tr>
    <td>LAB 1</td>
    <td>INTRODUCTION</td>
  </tr>
  <tr>
    <td>LAB 2</td>
    <td> LOOPS AND FUNCTION  <p>Open a PDF file <a href="/compilers/static_files/materials/lab/lab2.pdf">test lab 2</a>.</p></td>
  </tr>

  <tr>
    <td>LAB 3</td>
    <td>STRUCTS AND ARRAYS   <p>Open a PDF file <a href="/compilers/static_files/materials/lab/lab3.pdf">test lab 3</a>.</p></td>
  </tr>
  <tr>
    <td>LAB 4</td>
    <td>TYPE AND MEMORY SAFETY  <p>Open a PDF file <a href="/compilers/static_files/materials/lab/lab4.pdf">test lab 4</a>.</p></td>
  </tr>
  <tr>
    <td>LAB 5</td>
    <td>OPTIMIZATION    <p>Open a PDF file <a href="/compilers/static_files/materials/lab/lab5.pdf">test lab 5</a>.</p></td>
  </tr>
</table>











<ul id="archive">
{% for lecture in site.lectures reversed %}
<li class="archiveposturl" style="background: transparent">
<div class="lecture-container">
    {% if lecture.thumbnail %}
    <div class="thumbnail">
      <div class="center-cropped" style="margin-top:5px;margin-bottom:5px;background-image: url('{{ lecture.thumbnail | prepend: site.baseurl }}');">
        <img src="{{ lecture.thumbnail | prepend: site.baseurl }}"/>
      </div>
    </div>
    {% endif %}
    <div class="content">
        <span><a href="
            {% if lecture.slides contains '://' %}
              {{ lecture.slides }} 
            {% else %}
              {{ lecture.slides | prepend: site.baseurl }} 
            {% endif %}">{{ lecture.title }}</a>
        </span><br>

        {% if lecture.tldr %}
            <strong>tl;dr:</strong> 
            {{ lecture.tldr }}
            <br/>
        {% endif %}

        <strong>
            {% include lecture_links.html lecture=lecture %}
        </strong>
    </div>
</div>
</li>
{% endfor %}
</ul>