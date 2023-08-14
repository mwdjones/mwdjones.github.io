---
layout: default
permalink: /cv/
title: cv
nav: true
nav_order: 4
cv_pdf: MWJ_CV_LaTeX.pdf
description: A downloadable version of the CV below can be accessed via the icon to the right. 
---

<header class="post-header">
   <h1 class="post-title">{{ page.title }} {% if page.cv_pdf %}<a href="{{ page.cv_pdf | prepend: 'assets/pdf/' | relative_url}}" target="_blank" rel="noopener noreferrer" class="float-right"><i class="fas fa-file-pdf"></i></a>{% endif %}</h1>
     {% if page.description %}<p class="post-description">{{ page.description }}</p>{% endif %}
</header>

<embed src="https://mwdjones.github.io/assets/pdf/MWJ_CV_LaTeX.pdf" type="application/pdf"/>
