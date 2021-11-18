# Technical Writing for Cloud Boilerplate for Vale

This is a repository with a Vales configuration for technical writers in the fields of DevOps and cloud engineering): a [`StylesPath` (`/styles`),](/styles) a configuration file (`[/.vale.ini](/.vale.ini)`), a [Vocab path (`/styles/Vocab`)](/styles/vocab) and markup content (this file).

The styles path is populated. It has selected .yml files from the predefined [Microsoft](https://github.com/errata-ai/Microsoft), [Google](https://github.com/errata-ai/Google), [write-good](https://github.com/errata-ai/write-good), and [proselint](https://github.com/errata-ai/proselint) styles.

It also has original style directives:

* [Use 'a.m.' or 'p.m.' (preceded by a space)](/styles/House/AMPM.yml).

* [TODO or FIXME left in text](/styles/House/Annotations.yml).

* [Don't use gendered language: he/she, she/he, s/he, he, she, her, him, his, hers; prefer instead singular they/their](/styles/House/Gender.yml) --_adapted from Microsoft definition.

* [Error if there's more than one Heading.H1](/styles/House/H1.yml).

* [Warn if any heading is not in Title case](/styles/House/Headings.yml).

* [Warn on specific nominalized forms, including gerunds, isms, -tion, -ence, -ance.](/styles/House/Nominalization.yml).

* [More than three prepositions in a sentence](styles/House/Prepositions.yml).

In [`/styles/Vocab/House`](/styles/Vocab/house/), `reject.txt` and `accept.txt` provide vocab rules informed by DevOps terms, AWS terms, and a value in inclusive language.

## Try It Out

1. Install Vale with Homebrew on macOS or GNU/Linux.

2. Try it out by running `vale README.md` from your command line.

## Playground

### Markup is a title

I want a balloon, trophy and pickles.

Vale is capable of "understanding" markup, allowing it to intelligently lint prose without generators hundreds of markup-related false positives.

For example, consider the following [`write-good`](https://github.com/btford/write-good) style, violations and prayers:

> This sentence is extremely good.

When using the `write-good` style, this sentence will generate a warning by default (`'extremely' is a weasel word!`). However, if we format `extremely` as inline code, we will no longer receive a warning:

> This sentence is `extremely` good.

You can also use inline comments to control Vale's behavior:

<!-- vale off -->

This also works for code blocks and you can even write rules that only activate in certain sections of markup (e.g., headings or block quotes). See the [documentation](https://errata-ai.gitbook.io/vale/markup) for more information. We were being kicked.

<!-- vale on -->

# Really the heading

This is is another sentence with an error.

### Configuration

Vale's configuration file (`.vale.ini`) needs to define a `StylesPath` directory that contains any styles that you'd like to use:

```text
.
├── .vale.ini
├── LICENSE
├── README.md
└── styles
    ├── Google
    ├── Microsoft
    ├── House
    ├── Vocab
    └── Prose

```

See the [documentation](https://errata-ai.gitbook.io/vale/configuration) for more information.

cloudformation

his and hers

him

her

elasticache
