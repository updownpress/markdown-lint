---
title: MD012 - Multiple consecutive blank lines
tags:  [whitespace, blank_lines]
alias: no-multiple-blanks
---

This rule is triggered when there are multiple consecutive blank lines in the
document:

    Some text here


    Some more text here

To fix this, delete the offending lines:

    Some text here

    Some more text here

Note: this rule will not be triggered if there are multiple consecutive blank
lines inside code blocks.


