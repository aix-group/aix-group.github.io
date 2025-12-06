---
permalink: /publications/
permalink: /publications/
classes: wide
author_profile: true
---

<div class="bib-header">
  <p>Peer-reviewed publications since 2014, for more see <a href="https://scholar.google.com/citations?hl=en&user=aK6ZccUAAAAJ">Google Scholar</a>.</p>
  <input id="filter" placeholder="filter…" />
</div>

<script type="text/javascript">
  function updateYearHeadings() {
    // For each year heading inside .bib
    var yearHeadings = document.querySelectorAll('.bib h2');
    yearHeadings.forEach(function (h2) {
      // Find the next sibling <ol class="bibliography">
      var sib = h2.nextElementSibling;
      while (
        sib &&
        !(
          sib.tagName &&
          sib.tagName.toLowerCase() === 'ol' &&
          sib.classList.contains('bibliography')
        )
      ) {
        sib = sib.nextElementSibling;
      }
      if (!sib) return;

      // Check if that <ol> has any visible <li>
      var hasVisible = false;
      sib.querySelectorAll('li').forEach(function (li) {
        if (li.style.display !== 'none') {
          hasVisible = true;
        }
      });

      // Hide year if no visible entries, otherwise show it
      h2.style.display = hasVisible ? '' : 'none';
    });
  }

  function filter(text) {
    text = (text || '').toLowerCase();
    var bibitems = document.querySelectorAll('ol.bibliography li');

    // Show all by default
    bibitems.forEach(function (el) {
      el.style.display = 'inline';
    });

    // If there is actually filter text, hide non-matching ones
    if (text.trim() !== '') {
      bibitems.forEach(function (el) {
        var c = el.children;
        var last = c[c.length - 1];      // hidden <input> is last child
        if (!last || typeof last.value !== 'string') {
          el.style.display = 'none';
          return;
        }
        var tmp = last.value.toLowerCase();
        if (tmp.includes(text)) {
          el.style.display = 'inline';
        } else {
          el.style.display = 'none';
        }
      });
    }

    // After entries are updated, adjust year headings
    updateYearHeadings();
  }

  document.addEventListener("DOMContentLoaded", function () {
    var filterInput = document.querySelector('#filter');

    if (filterInput) {
      filterInput.addEventListener('input', function () {
        filter(filterInput.value);
      });
    }

    // support /publications/#some+query
    var urlParts = document.URL.split('#');
    if (urlParts.length > 1) {
      var anchor = decodeURIComponent(urlParts[1]);
      if (filterInput) {
        filterInput.value = anchor;
      }
      filter(anchor);
    } else {
      // Ensure headings are correct on first load (no filter)
      updateYearHeadings();
    }

    // -------------------------------------------------------
    // Copy BibTeX handler (for the little copy icon)
    // -------------------------------------------------------
    document.addEventListener('click', function (e) {
      var btn = e.target.closest('.pub-bibtex__copy');
      if (!btn) return;

      var details = btn.closest('.pub-bibtex');
      if (!details) return;

      var pre = details.querySelector('pre');
      if (!pre) return;

      var text = pre.innerText || pre.textContent || '';

      function markCopied() {
        btn.classList.add('copied');
        setTimeout(function () {
          btn.classList.remove('copied');
        }, 1200);
      }

      if (navigator.clipboard && navigator.clipboard.writeText) {
        navigator.clipboard.writeText(text)
          .then(markCopied)
          .catch(function (err) {
            console.error('Clipboard copy failed:', err);
          });
      } else {
        // Fallback for older browsers
        var textarea = document.createElement('textarea');
        textarea.value = text;
        textarea.style.position = 'fixed';
        textarea.style.left = '-9999px';
        document.body.appendChild(textarea);
        textarea.select();
        try {
          document.execCommand('copy');
          markCopied();
        } catch (err) {
          console.error('execCommand copy failed:', err);
        }
        document.body.removeChild(textarea);
      }
    });
  });
</script>


<div class="bib">
{% bibliography -f references.bib -f additional-team.bib -q !@techreport[year >=2014] --remove_duplicates %}
</div>
