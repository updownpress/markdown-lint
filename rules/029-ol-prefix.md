---
title: MD029 - Ordered list item prefix
tags:  [ol]
alias: ol-prefix
---

Parameters: style ("one", "ordered"; default "one")

This rule is triggered on ordered lists that do not either start with '1.' or
do not have a prefix that increases in numerical order (depending on the
configured style, which defaults to 'one').

Example valid list if the style is configured as 'one':

    1. Do this.
    1. Do that.
    1. Done.

Example valid list if the style is configured as 'ordered':

    1. Do this.
    2. Do that.
    3. Done.


