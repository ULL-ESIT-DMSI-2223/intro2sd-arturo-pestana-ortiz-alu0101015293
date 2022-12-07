---
layout: default
permalist: /search/ 
title: Search
---

{% capture initSearch %}

<h1>Search</h1>

<form id="search-for" action="">
    <label class="label" for="search">Buscador (acepta expresiones regulares):</label>
    </br>
    <input class="input" id="search" type="text" name="search" autofocus placeholder="Ejemplo" autocomplete="off">

    <ul class="list list--results" id="list"> </ul>
</form>

<script type="text/javascript" src="{{site.baseurl}}/assets/src/fetch.js"></script>
<script type="text/javascript" src="{{site.baseurl}}/assets/src/search.js"></script>

<script type="text/javascript">
    const search = new JekyllSearch(
        '{{site.baserurl}}/assets/src/search.json',
        '#search',
        '#list',
        '{{site.baseurl}}'
    );
    search.init();
</script>

<noscript>Please enable JavaScript to use the search form.</noscript>

fetchedData() {
    return fetch(this.dataource, {mode: 'no-cors'})
    .then(blob => blob.json())
} ## esto dehe de ir en el search.js

{% endCapture %}

{{ initSearch | lstrip }}