---
title: Research
permalink: /research/
---

{% assign people_sorted = site.people | sort: "joined" %}
{% assign people_array = "pi|postdoc|gradstudent|others" | split: "|" %}


<!--
{% assign people_sorted = site.people | sort: "joined" %}
<ul>
{% for y in yearsSorted %}
  <li>{{ y.name }}
    <ul>
      {% assign yearTitlesSorted = y.items | sort: "title" %}
      {% for t in yearTitlesSorted %}
      <li>{{ t.title }}</li>
      {% endfor %}
    </ul>
  </li>
{% endfor %}
</ul>-->

<h3>Research groups</h3>
{% for item in people_array %}

<div class="pos_header">
 {% if item == 'pi' %}


<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains item %}
    {% if profile.name == "new hire (soon)"%}
    	{% break %}
    {% endif %}
    <div class="list-item-people">
      <p class="list-post-title">
      	<!--{% if profile.avatar %}
        <a href="{{ site.baseurl }}{{ profile.url }}"><img width="200" height="230" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
        {% else %}
        <a href="{{ site.baseurl }}{{ profile.url }}"><img width="200" height="230" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg"></a>
        {% endif %}-->
        <a href="{{profile.website}}"><img width="15%" height="15%" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
            {% if profile.affiliation %}
                  <a class="name" href="{{profile.website}}"><div style="text-align: left;"><font size="+0"><b>{{ profile.affiliation }} group</b></font></div></a>
                  <small><span style="color:#9d9d9d"><div style="text-align: left;">(Principal investigator: {{ profile.name }})</div></span></small>
            {% else %}
                  <a class="name" href="{{profile.website}}"><div style="text-align: left;"><font size="+0"><b>{{ profile.name }} group</b></font></div></a>
            {% endif %}
        <br><header class="text-left">{{ profile.content }}</header>      
        <hr>      
		</p>
    </div>    
    {% endif %}	
  {% endfor %}
</div>

 {% endif %}
</div>
{% endfor %}

We collaborate with research groups nationally and internationally, but also across the university:

<ul>
  <li>The wider <a href="http://www.bristol.ac.uk/neuroscience/" target="_blank">Bristol Neuroscience</a></li>
  <li><a href="http://www.bristol.ac.uk/phys-pharm-neuro/" target="_blank">School of Physiology, Pharmacology and Neuroscience</a></li>
  <li><a href="http://www.bristol.ac.uk/psychology/" target="_blank">School of Psychological Science</a></li>
  <li><a href="https://www.bristolmathsresearch.org/statistical-science/" target="_blank">Institute for Statistical Science</a></li>
  <li><a href="http://intelligentsystems.bristol.ac.uk/" target="_blank">Intelligent Systems Lab</a></li>
  <li><a href="http://vilab.blogs.bristol.ac.uk/" target="_blank">Visual Information Lab</a></li>  
</ul>  

<hr>

{% include footer.html %}

