---
title: MD033 - Inline HTML
tags:  [html]
alias: no-inline-html
---

This rule is triggered whenever raw HTML is used in a markdown document:

    <h1>Inline HTML header</h1>

To fix this, use 'pure' markdown instead of including raw HTML:

    # Markdown header

Rationale: Raw HTML is allowed in markdown, but this rule is included for
those who want their documents to only include "pure" markdown, or for those
who are rendering markdown documents in something other than HTML.


