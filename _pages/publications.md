---
layout: page
permalink: /publications/
title: Publications
description: Papers in reverse chronological order. Also on <a href="https://scholar.google.com/citations?user=9buTD38AAAAJ&hl=en">Google Scholar</a>.
nav: true
nav_order: 3
---

<!-- _pages/publications.md
     Papers come from _bibliography/papers.bib, posters from _bibliography/posters.bib. -->

{% include bib_search.liquid %}

<div class="publications">

<h2 class="bibliography">Papers</h2>

{% bibliography %}

<h2 class="bibliography">Abstracts and posters</h2>

{% bibliography --file posters %}

</div>
