---
layout: default
permalist: /search/ 
title: Search
---

{% capture initSearch %}

<h1>Search</h1>

<form id="search-for" action="">
    <label class="label" for="search">Search term (accepts a regex):</label>
    </br>
    <input class="input" id="search" type="text" name="search" autofocus placeholder="e.Promise" autocomplete="off">

    <ul class="list list--results" id="list">
    </ul>
</form>

<script type="text/javascript" src="{{site.baseurl}}/assets/src/fetch.js"></script>
<script type="text/javascript" src="{{site.baseurl}}/assets/src/search.js"></script>


{% endCapture %}