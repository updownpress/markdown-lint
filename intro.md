---
title: Markdown lint tool
---

A tool to check markdown files and flag style issues.

## Installation

Markdownlint is written in ruby and is distributed as a rubygem. As long as
you have a relatively up to date ruby on your system, markdownlint will be
simple to install and use.

To install from rubygems, run:

    gem install mdl

To install the latest development version from github:

    git clone https://github.com/mivok/markdownlint
    cd markdownlint
    rake install

## Usage

<!-- ed begin: added by geraldb -->

Try:

   $ mdl -h
   
Resulting in:

```
Usage: mdl [options] [FILE.md|DIR ...]
    -c, --config FILE                The configuration file to use
    -g, --git-recurse                Only process files known to git when given a directory
    -l, --list-rules                 Don't process any files, just list enabled rules
    -r, --rules RULE1,RULE2          Only process these rules
    -w, --[no-]warnings              Show kramdown warnings
    -s, --style STYLE                Load the given style
    -t, --tags TAG1,TAG2             Only process rules with these tags
    -v, --[no-]verbose               Increase verbosity
    -h, --help                       Show this message
    -V, --version                    Show version
```

<!-- ed end: added by geraldb -->


To have markdownlint check your markdown files, simply run `mdl` with the
filenames as a parameter:

    mdl README.md

Markdownlint can also take a directory, and it will scan all markdown files
within the directory (and nested directories):

    mdl docs/

If you don't specify a filename, markdownlint will use stdin:

    cat foo.md | mdl

Markdownlint will output a list of issues it finds, and the line number where
the issue is. See [RULES.md](rules/rules.md) for information on each issue, as
well as how to correct it:

    README.md:1: MD013 Line length
    README.md:70: MD029 Ordered list item prefix
    README.md:71: MD029 Ordered list item prefix
    README.md:72: MD029 Ordered list item prefix
    README.md:73: MD029 Ordered list item prefix

Markdownlint has many more options you can pass on the command line, run
`mdl --help` to see what they are, or see the documentation on
[configuring markdownlint](configuration.md).

### Styles

Not everyone writes markdown in the same way, and there are multiple flavors
and styles, each of which are valid. While markdownlint's default settings
will result in markdown files that reflect the author's preferred markdown
authoring preferences, your project may have different guidelines.

It's not markdownlint's intention to dictate any one specific style, and in
order to support these differing styles and/or preferences, markdownlint
supports what are called 'style files'. A style file is a file describing
which rules markdownlint should enable, and also what settings to apply to
individual rules. For example, rule [MD013](rules/013-line-length.md)
checks for long lines, and by default will report an issue for any line longer
than 80 characters. If your project has a different maximum line length limit,
or if you don't want to enforce a line limit at all, then this can be
configured in a style file.

For more information on creating style files, see the
[creating styles](creating_styles.md) document.

