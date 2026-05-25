# Journal Fixer

An agent skill that rewrites academic papers or journals in LaTeX manuscripts to sound like real published papers, without touching math, citations, or document structure.

## What it does

Point it at a `.tex` file. It edits the prose in place so a peer reviewer in your field would not pause on how something is written. Math, figures, tables, labels, and bibliography stay untouched.

It can change the tone of the text to more research-oriented language. It can fix the grammar of sentences. It can expand the content of a conference paper into a research journal, and vice-versa. And all of this without getting flagged by any AI detection system.

## Installation Command

```bash
npx skills add https://github.com/Swpn0neel/academic-skills --skill journal-fixer
```