---
layout: default
permalink: /search/
title: Search
---

{% capture initSearch %}

<h1>Search</h1>

<form id="search-form" action="">~
  <label class="label" for="search">Search term (accepts a regex):</label>
  <br/>
  <input 
    class="input" 
    id="search" 
    type="text" 
    name="search" 
    autofocus 
    placeholder="e.g. Promise" 
    autocomplete="off">

  <ul class="list list--results" id="list">
  </ul>
</form>

<script type="text/javascript" src="{{site.baseurl}}/assets/src/fetch.js"></script> 
<script type="text/javascript" src="{{site.baseurl}}/assets/src/fetch.js"></script>
[comment]: <> (es donde se mete todo el codigo de busqueda)



<script type="text/javascript">

  const search = new JekyllSearch(
    '{{site.url}}/assets/src/search.json',
    '#search',
    '#list',
    '{{site.baseurl}}'
  );
  search.init();

</script>

[comment]: <> (estamos creando objetos de la clase JekyllSearch)

<noscript>Please enable JavaScript to use the search form.</noscript>

{% endcapture %}

{{ initSearch | lstrip }}

[comment]: <> (lstrip -> quita los blancos que se encuentran a la izquierda)

[comment]: <> (autofocus -> cuando se cargue la pagina quiero que el cursor este aqui, es decir, en la cajita)
[comment]: <> (name = search -> el nombre para el servidor)

[comment]: <> (ul -> lista desordenada en html)
[comment]: <> (ol -> lista ordenada en html)