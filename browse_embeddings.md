---
layout: page
permalink: /browse_embeddings/
# Use this for TeXt theme to hide from index/feeds
sharing: false
show_edit_on_github: false
show_subscribe: false
custom_css: full-width.css
---

<script>
  function setHeaderFooterHeight() {
    const header = document.querySelector('.js-page-header') || document.querySelector('.navigation');
    const footer = document.querySelector('.js-page-footer') || document.querySelector('.page__footer');
    
    if (header) {
      document.documentElement.style.setProperty('--header-height', header.offsetHeight + 'px');
    }
    if (footer) {
      document.documentElement.style.setProperty('--footer-height', footer.offsetHeight + 'px');
    }
  }

  window.addEventListener('load', setHeaderFooterHeight);
  window.addEventListener('resize', setHeaderFooterHeight);
</script>

<div class="iframe-container">
<iframe src="{{ '/assets/html/embedding_browser.html' | relative_url }}" 
        frameborder="0">
</iframe>
</div>