---
layout: page
title: Assignments
permalink: /assignments/
---

<ul id="archive">
{% for asg in site.assignments reversed %}
      <li class="archiveposturl" style="background: transparent">
        <span><a href="{{ asg.url | prepend: site.baseurl}}">{{ asg.title }}</a></span>
<strong style="font-size:100%; font-family: 'Titillium Web', sans-serif; float:right">
<a title="Download problems (pdf)" href="{{ asg.pdf | prepend: site.baseurl }}"><i class="fas fa-file-pdf"></i></a> 
{% if asg.attachment %}
&nbsp; <a title="Download attachments (zip)" href="{{ asg.attachment | prepend: site.baseurl }}"><i class="fas fa-file-archive"></i></a>
{% endif %}
</strong> 
      </li>
{% endfor %}
</ul>


<h1 style="color:blue;">some additional exercises for you</h1>

* [ download assignment 1 ](/static_files/materials/ass/asst1.pdf)
* [ download assignment 2 ](/static_files/materials/ass/asst2.pdf)
* [ download assignment 3 ](/static_files/materials/ass/asst3.pdf)
* [ download assignment 4 ](/static_files/materials/ass/asst4.pdf)
* [ download assignment 5 ](/static_files/materials/ass/asst5.pdf)