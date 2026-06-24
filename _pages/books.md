---
layout: page
title: bookshelf
permalink: /books/
nav: false
collection: books
---

## Books that I am reading, have read, or will read
<h2>2026</h2>

<!-- 1. CURRENTLY READING -->
<h3>Currently Reading</h3>
<div class="row">
  {% assign reading_books = site.books | where: "year", 2026 | where: "status", "reading" %}
  {% for book in reading_books %}
    <div class="col-sm-4">
      <strong>{{ book.title }}</strong> by {{ book.author }}
    </div>
  {% empty %}
    <p>No books currently being read.</p>
  {% endfor %}
</div>

<hr>

<!-- 2. NEXT UP / TO READ -->
<h3>Up Next</h3>
<div class="row">
  {% assign to_read_books = site.books | where: "year", 2026 | where: "status", "to-read" %}
  {% for book in to_read_books %}
    <div class="col-sm-4">
      <strong>{{ book.title }}</strong> by {{ book.author }}
    </div>
  {% empty %}
    <p>No books on the horizon yet.</p>
  {% endfor %}
</div>

<hr>

<!-- 3. FINISHED -->
<h3>Finished</h3>
<div class="row">
  {% assign finished_books = site.books | where: "year", 2026 | where: "status", "finished" %}
  {% for book in finished_books %}
    <div class="col-sm-4">
      <strong>{{ book.title }}</strong> by {{ book.author }}
    </div>
  {% empty %}
    <p>No finished books recorded for this year.</p>
  {% endfor %}
</div>
