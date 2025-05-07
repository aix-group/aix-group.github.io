---
permalink: /publications/
title: Publications
---

Showing peer-reviewed publications since 2014. For more recent preprints, see [Google Scholar](https://scholar.google.com/citations?hl=en&user=aK6ZccUAAAAJ).

<input id="filter" type="text" size=20 placeholder="filter..." />


<script type="text/javascript">
  function filter(text) {
    text = text.toLowerCase();
    var bibitems = document.querySelectorAll('ol.bibliography li');
    bibitems.forEach(el => el.style.display = 'none');
    bibitems.forEach(el => {
      var c = el.children;
      var tmp = c[c.length -1].value.toLowerCase();
      if(tmp.includes(text)) {
        el.style.display = 'inline';
      }
    });
  };
  document.addEventListener("DOMContentLoaded", function(event) {
    document.querySelector('#filter').addEventListener('input', (e) => {
      filter(document.querySelector('#filter').value);
    });
    var urlParts   = document.URL.split('#');
    if (urlParts.length > 1) {
        var anchor = decodeURIComponent(urlParts[1]);
        document.querySelector('#filter').value = anchor;
        filter(anchor);
    }
  });
</script>

<div class="bib">
{% bibliography -f references.bib -f additional-team.bib  -q !@techreport[year >=2014]  --remove_duplicates  %}
</div>

