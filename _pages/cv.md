---
layout: cv
permalink: /cv/
title: CV
nav: true
nav_order: 5
cv_pdf:
cv_format: rendercv # options: rendercv, jsonresume
description:
toc:
  sidebar: left
---

<style>
  /*
    Fix for al_folio_cv 1.0.0 with Bootstrap compat off: the CV sections are <ul class="list-group">,
    which nothing styles, so browsers draw bullets and a 40px indent. These are the same rules that
    al_folio_cv 1.0.3 ships. If you later upgrade the plugin to >= 1.0.3, you can delete this block.
  */
  ul.list-group {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  ul.list-group > li.list-group-item {
    padding: 0.5rem 0.75rem;
    border-bottom: 1px solid var(--global-divider-color, rgba(128, 128, 128, 0.3));
  }

  ul.list-group-flush > li.list-group-item:last-child {
    border-bottom: 0;
  }

  /* no stray rule above the date badges */
  table.table-cv td,
  table.table-cv th {
    padding: 1px;
    border-top: 0;
  }
</style>
