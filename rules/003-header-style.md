---
title: MD003 - Header style
tags:  [headers]
alias: header-style
---

Parameters: style ("consistent", "atx", "atx_closed", "setext", "setext_with_atx"; default "consistent")

This rule is triggered when different header styles (atx, setext, and 'closed'
atx) are used in the same document:

    # ATX style H1

    ## Closed ATX style H2 ##

    Setext style H1
    ===============

Be consistent with the style of header used in a document:

    # ATX style H1

    ## ATX style H2

The setext_with_atx doc style allows atx-style headers of level 3 or more in
documents with setext style headers:

    Setext style H1
    ===============

    Setext style H2
    ---------------

    ### ATX style H3

Note: the configured header style can be a specific style to use (atx,
atx_closed, setext, setext_with_atx), or simply require that the usage be
consistent within the document.
