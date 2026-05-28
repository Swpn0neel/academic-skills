# Academic Skills

A collection of agent skills for researchers and academics.

## 1. Research Scout

Searches academic databases and the web to find existing research on your idea, assesses how saturated the space is, and delivers a definitive PROCEED / PIVOT / DROP verdict backed by real paper links.

Point it at a research idea that can be a thesis topic, a paper concept, a patent idea. It searches Google Scholar, arXiv, Semantic Scholar, PubMed, IEEE Xplore, ACM Digital Library, and the web, then tells you honestly whether your angle is novel, already done, or needs a specific change to be worth pursuing. It also gives you additonal feedback about how you can approach the research topic and gives you legitimate papers to read regarding your specific topic.

```bash
npx skills add https://github.com/Swpn0neel/academic-skills --skill research-scout
```

## 2. Journal Fixer

Rewrites academic papers written in LaTeX to sound like real published papers, without touching math, citations, or document structure.

Point it at a `.tex` file. It edits the prose in place so a peer reviewer in your field would not pause on how something is written. Math, figures, tables, labels, and bibliography stay untouched.

It can change the tone of the text to more research-oriented language, fix grammar, expand a conference paper into a journal version (and vice-versa), and do all of this without getting flagged by AI detection systems.

```bash
npx skills add https://github.com/Swpn0neel/academic-skills --skill journal-fixer
```

## 3. Ref Builder

Reads an academic paper, finds real supporting papers for every claim, and builds or improves a complete bibliography with properly placed inline citations throughout the text.

Point it at a `.tex` file or plain-text manuscript. It extracts every factual claim that needs a citation, searches Google Scholar, arXiv, Semantic Scholar, PubMed, IEEE Xplore, and ACM Digital Library for real papers, verifies each one exists, then inserts inline citation markers at the right places and produces a formatted bibliography. Works with existing references too — it can fill gaps, replace placeholders, or verify that your current citations are real.

Supports IEEE, APA, ACM, Vancouver, Chicago, and MLA styles. Auto-detects the style from your document class or bibliography commands.

```bash
npx skills add https://github.com/Swpn0neel/academic-skills --skill ref-builder
```