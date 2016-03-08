---
title: MD040 - Fenced code blocks should have a language specified
tags:  [code, language]
alias: fenced-code-language
---

This rule is triggered when fenced code blocks are used, but a language isn't
specified:

    ```
    #!/bin/bash
    echo Hello world
    ```

To fix this, add a language specifier to the code block:

    ```bash
    #!/bin/bash
    echo Hello world
    ```

