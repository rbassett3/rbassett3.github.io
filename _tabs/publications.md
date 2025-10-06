---
layout: default
icon: fa-solid fa-book
order: 2
---

# Publications

This page is a repository for the published versions of my work. If you are looking for an up-to-date list of my recent work, you will be better served by my [Google Scholar page](https://scholar.google.com/citations?user=9ZHI8bgAAAAJ&hl=en) or [CV](../assets/cv/CV.pdf) since I update this repository sporadically and do not add manuscripts that are in preprint or under review.

## List of Pubs in Reverse Chronological Order

{% assign publications = site.publications | sort: "year" | reverse %}
{% for pub in publications %}
<div class="pubitem">
  <div class="pubtitle"><strong> {{ pub.title }}</strong></div>
  <div class="pubauthors">{{ pub.authors }}</div>
  <div class="pubinfo">{{ pub.publication }}, {{ pub.year}}</div>
  <div class="publinks">
  <a href="{{ pub.link}}"><i class="far fa-file-pdf"></i> PDF</a
  >&nbsp;&nbsp; {% if pub.code %}
  <a href="{{pub.code}}"><i class="fas fa-link"></i> Code & Experiments</a
  >&nbsp;&nbsp; {% endif %}
</div>
  <br>
</div>
{% endfor %}


