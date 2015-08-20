---
layout: page
title: Search my blog posts
permalink: search/
---
<input id="search" type="text" value="" onkeydown="if (event.keyCode == 13) doSearch()"/>
<div>
<input id="searchBtn" type="submit" onclick="doSearch()" value="Search">
</div>

<div id="output"></div>

<script type="text/javascript" src="{{ site.baseurl }}public/js/search-min.js"></script>