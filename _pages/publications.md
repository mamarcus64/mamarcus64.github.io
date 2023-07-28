---
layout: page
permalink: /publications/
title: publications
description:
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">
<h3>Journal and Conference Articles</h3>
{% bibliography -f {{ site.scholar.bibliography }} %}

</div>

<div class="publications">
<h3>Conference Presentations</h3>
{% bibliography -f {{ site.scholar.conference_bibliography }} %}
</div>
