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

{% for item in people_array %}

<div class="pos_header">
 {% if item == 'pi' %}
<h3>Research groups</h3>

<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains item %}
    {% if profile.name == "new hire"%}
    	{% break %}
    {% endif %}
    <div class="list-item-people">
      <p class="list-post-title">
      	<!--{% if profile.avatar %}
        <a href="{{ site.baseurl }}{{ profile.url }}"><img width="200" height="230" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
        {% else %}
        <a href="{{ site.baseurl }}{{ profile.url }}"><img width="200" height="230" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg"></a>
        {% endif %}-->
    	<table class="fixed">
    		<col width="180" />
		  <tbody>
			<tr>
				<td>    
					<div class="content list">    
						<a href="{{profile.website}}"><img width="250" height="220" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
						<a class="name" href="{{profile.website}}"><font size="+0">{{ profile.name }}</font></a>
						{% if profile.affiliation %}
		        			<br><small><span style="color:#9d9d9d">{{ profile.affiliation }}</span></small>
		        		{% endif %}        
					</div>
				</td>
				<td>
				<header class="text-left">{{ profile.content }}</header>
				</td>
			</tr>
			</tbody>
		</table>     
		</p>
    </div>    
    {% endif %}	
  {% endfor %}
</div>

 {% endif %}
</div>
{% endfor %}


<!-- ### Research
Making sense of data is possibly the biggest problem in Neuroscience and beyond. We build algorithms to analyze data. We also use theory as well as computational and [neural modeling](https://en.wikipedia.org/wiki/Computational_neuroscience) to understand how information is processed in the nervous system, explaining data obtained in collaboration with [electrophysiologists](https://en.wikipedia.org/wiki/Electrophysiology) and in [psychophysical](https://en.wikipedia.org/wiki/Psychophysics) experiments. Lastly, we constrain and develop new technologies aimed at obtaining data about brains.


Our conceptual work addresses information processing in the nervous system from two angles: (1) By analyzing and explaining electrophysiological data, we study what neurons do. (2) By analyzing and explaining human behavior, we study what all these neurons do together. Much of our work looks at these questions from a normative or causal viewpoint, asking what problems the nervous system should be solving. This often means taking a Bayesian approach. Bayesian decision theory is the systematic way of calculating how the nervous system may make good decisions in the presence of uncertainty. Causal inference from observational data promises to be a key enabler for progress in science.

We've pursued projects that involve handshake greetings, human movement, [cell-phone related parkinson's research](http://journal.frontiersin.org/article/10.3389/fneur.2012.00158/abstract), competitions at [Kaggle](https://www.kaggle.com/), [meta-science analysis](http://www.nature.com/nature/journal/v489/n7415/full/489201a.html), data sharing initiatives, and [recording from all neurons in a mouse](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1002291).


### Lab Members

Our research group is remarkably interdisciplinary. Our interests span statistics, physics, biology, applied mathematics, molecular biology, metascience, cognitive science, and many other disciplines. Visit our [people page](http://kordinglab.com/people/) to see more information on each person who works in the lab (publications, contact information, photos).


### Publications

For PDFs of our work, visit our [publications page](http://kordinglab.com/publication/). Feel free to [issue on Github](https://github.com/KordingLab/KordingLab.github.io/issues) if links don't work or are obsolete.


### Collaborators

Here are some cool people in fields that interest us. **note:** This list is in no way complete. We have a lot of collaborators -- if you've collaborated with us and want a link here, let us know!

**University of Pennsylvania:**
- [David Issadore - Dept of Bioengineering](http://cnt.upenn.edu/david-issadore)
- [Jay Gottfried - Dept of Neurology](http://labs.feinberg.northwestern.edu/gottfried/)
- [Raquel and Ruben Gur - Dept of Neuropsychiatry](http://www.med.upenn.edu/bbl/faculty-regur.html)
- [Maria Geffen - Dept of Otorhinolaryngology](https://geffenlab.weebly.com/)
- [Yale Cohen - Dept of Otorhinolaryngology](http://auditoryresearchlaboratory.weebly.com/)
- [Dani Bassett - Dept of Bionengineering](https://www.danisbassett.com/)
- [Andrew Tsourkas - Dept of Bioengineering](http://www.seas.upenn.edu/~atsourk/)
- [Jason Moore - Dept of Biostatistics](https://www.med.upenn.edu/apps/faculty/index.php/g275/p8803452)
- [Lyle Ungar - Dept of CIS](http://www.cis.upenn.edu/~ungar/)

**Northwestern University:**
- [Lee Miller - Depts of Physiology and BME](http://physio.northwestern.edu/)
- [Mark Segraves - Depts of Neurobiology and Physiology](http://www.neurobiology.northwestern.edu/people/core-faculty/mark-segraves.html)
- [Matt Tresch - Depts of Physiology and BME](http://www.mccormick.northwestern.edu/biomedical/)
- [David Mohr - Dept of Preventive medicine](http://www.feinberg.northwestern.edu/faculty-profiles/az/profile.html?xid=17234)


**External:**

- [Scott Grafton - UCSB](https://www.psych.ucsb.edu/people/faculty/grafton)
- [Nicho Hatsopoulos - University of Chicago](http://pondside.uchicago.edu/oba/faculty/Hatsopoulos/lab/)
- [Peter Strick - University of Pittsburgh](http://www.cnbc.cmu.edu/faculty/strick-peter-l/view-details)
- [Mriganka Sur - MIT](http://surlab.mit.edu/)
- [Rob Turner - University of Pittsburgh](http://www.neurobio.pitt.edu/faculty/turner.htm)
-->