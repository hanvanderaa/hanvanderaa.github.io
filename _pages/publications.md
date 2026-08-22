---
layout: page
permalink: /publications/
title: publications
display_title: Publications
nav: true
nav_order: 1
---

<!-- _pages/publications.md -->

<div class="pub-nav" markdown="1">
[Conference Papers](#conference-papers) &middot; [Journal Articles](#journal-articles) &middot; [Workshop, Forum, and Demo Papers](#workshop-forum-and-demo-papers) &middot; [Edited Proceedings](#edited-proceedings) &middot; [Book Chapters](#book-chapters) &middot; [Invited Articles](#invited-articles) &middot; [Book](#book) &middot; [Theses](#theses)
</div>

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<script>
  document.addEventListener("DOMContentLoaded", function () {
    document.querySelectorAll(".pub-nav a[href^='#']").forEach(function (link) {
      link.addEventListener("click", function (event) {
        event.preventDefault();
        var target = document.getElementById(this.getAttribute("href").slice(1));
        if (target) {
          target.scrollIntoView({ behavior: "smooth", block: "start" });
        }
      });
    });
  });
</script>

<div class="publications">

<h2 id="conference-papers">Conference Papers</h2>
{% bibliography -q @*[category=conference] -g year %}

<h2 id="journal-articles">Journal Articles</h2>
{% bibliography -q @*[category=journal] -g year %}

<h2 id="workshop-forum-and-demo-papers">Workshop, Forum, and Demo Papers</h2>
{% bibliography -q @*[category=workshop] -g year %}

<h2 id="edited-proceedings">Edited Proceedings</h2>
{% bibliography -q @*[category=proceedings] %}

<h2 id="book-chapters">Book Chapters</h2>
{% bibliography -q @*[category=chapter] %}

<h2 id="invited-articles">Invited Articles</h2>
{% bibliography -q @*[category=invited] %}

<h2 id="book">Book</h2>
{% bibliography -q @*[category=book] %}

<h2 id="theses">Theses</h2>
{% bibliography -q @*[category=thesis] %}

</div>
