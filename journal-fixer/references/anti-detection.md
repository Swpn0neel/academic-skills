# Anti-detection: academic-specific AI tells

Use this in Phase 4 (the second-pass audit) along with `humanizer.md`.
The two files are complementary:

- `humanizer.md` covers the general-purpose anti-AI patterns adapted for
  academic LaTeX (em-dash overuse, rule of three, copula avoidance, AI
  vocabulary, hedge stacking, signposting, smart-quote contamination,
  etc.) and contains the self-audit loop.
- This file covers the additional tells that show up specifically in
  **AI-generated academic writing** — patterns that an experienced
  reviewer or a detection tool trained on post-2023 academic prose will
  catch even after the general humanizer pass.

These are the things that make a paper read "AI" even when every
individual sentence looks fine. Run this pass after `humanizer.md`, not
before.

## How to run this pass

For each paragraph you rewrote, walk through the checklist below.
Whenever you find a hit, fix it before moving on. Do this *after* the
academic-style pass and *after* the humanizer pass — the residual
patterns this catches are the ones the previous passes won't have
removed.

It is a check, not a creative rewrite. If you don't see any hits in a
paragraph, leave it alone.

## The checklist

### 1. Uniform paragraph shape

AI-generated paper paragraphs have a recognisable rhythm:

- 3–5 sentences
- Sentence 1: topic claim
- Sentence 2–3: supporting elaboration
- Sentence 4–5: synthesising restatement
- Often ends with an "underscoring", "highlighting", or "providing"
  participial clause

If every paragraph in a section has this exact shape, that is a strong
detector signal even if no individual sentence is bad. Real academic
paragraphs vary much more: some are two sentences, some are eight, some
end on a bare claim, some end on a citation, some on a number.

**Fix:** vary at least every third paragraph. Break up a long one with
a paragraph boundary mid-thought, or merge two short ones into one
denser paragraph.

### 2. Paper-introductory throat-clearing

Real research introductions do not warm up. They state a problem and
move. AI introductions warm up at length:

- "In recent years, the field of X has seen tremendous growth..."
- "With the advent of Y, researchers have increasingly turned to..."
- "X has long been a topic of interest in the community..."

**Fix:** if the first paragraph of the introduction does not contain a
specific fact, finding, or problem statement, rewrite it so it does.
The reader should know in two sentences what the paper is about.

### 3. Empty contribution claims

Look at the contributions paragraph. Each contribution should be a
specific, falsifiable claim. AI contributions tend to be vague:

- "We propose a novel framework for X" — what does it do?
- "We provide a comprehensive evaluation" — on what?
- "We demonstrate the effectiveness of our approach" — by which metric?
- "We open new avenues for research" — name one.

**Fix:** every bullet in a contributions list should answer "what,
specifically, did this paper add to the literature that someone could
verify or refute?"

### 4. The "novel framework" gauntlet

AI papers love the word "novel" and the word "framework". A real paper
uses each carefully:

- "novel" — once, attached to the actual new thing.
- "framework" — when there is genuinely a framework (a set of related
  abstractions). Often what AI calls a "framework" is just a method or
  a model.

**Fix:** count occurrences. If "novel" appears more than 2–3 times in a
short paper, cut. If "framework" appears for things that are not
frameworks, replace with "method", "model", "approach", or the actual
component name.

### 5. Decoration verbs in results

Results sections are about what was observed and measured. AI results
sections are about how impressive that is.

Decoration verbs to flag: *demonstrate, exhibit, showcase, validate,
underscore, highlight, emphasise, prove, establish (when used loosely),
confirm, verify*.

A normal sentence: "Our model reaches 87% accuracy on X (Table 2)."
An AI sentence: "Our model demonstrates remarkable performance,
achieving 87% accuracy and underscoring the effectiveness of our
proposed approach."

**Fix:** in results sections, lean on neutral verbs (*reach, achieve,
score, increase to, decrease to, improve over, match, fall short of*)
plus the number. Save *show* and *find* for places where you really are
making an inference from the data.

### 6. Citation theatre

AI tends to cite for vibes, not for content. Watch for:

- Sentences ending in citation piles `[3, 7, 12, 15, 18]` where the
  sentence does not actually need five sources to support it.
- Citations that don't seem to do work — the sentence reads the same
  with them removed.
- "Several recent works" or "many studies" followed by 3–4 citations,
  where naming one or two specifically would be more honest.
- Suspicious clusters: every third sentence in related work ends with
  exactly two citations.

**Fix:** for each citation cluster, ask whether each citation is the
*right* citation for the specific claim. If the cluster is decorative,
keep the strongest one or two and drop the rest.

(If you are editing and don't have access to verify the citations
themselves, leave the keys alone — your job is only to flag the
*pattern* and reshape the prose, not to guess which citation is real.)

### 7. Even hedging distribution

Real papers hedge where the literature is uncertain and assert where it
is settled. AI papers spread hedging evenly across all sentences.
Visible signs:

- Methods section with hedges ("X may be considered a standard
  approach...") — methods should be assertive about what was done.
- Results section with hedges around the actual numbers ("our model
  appears to achieve approximately 87%...") — measured results are not
  hedged.
- Discussion section *without* hedges around interpretive claims — if
  every interpretation is asserted as fact, that is also suspicious.

**Fix:** strip hedges from methods and reported numbers. Restore
appropriate hedges to interpretive claims in discussion.

### 8. Symmetric "balanced view" reflexes

AI prose has a strong reflex to present "both sides" even when the
paper is making a one-sided argument. Signs:

- "While X has many advantages, it also has limitations..."
- "Although our approach performs well, we acknowledge that..."
- "X has been praised by some and criticised by others..."

These are fine where they're true. But AI tends to insert them at the
end of every paragraph as a tic.

**Fix:** keep balanced views where they reflect the literature.
Remove them where they're decorative concession-making.

### 9. The "implications" pile-on

AI conclusions and discussions love to gesture at "implications" without
naming them.

- "These findings have important implications for the field of X."
- "Our results have profound implications for both theory and practice."
- "The implications of our work extend beyond X to Y and Z."

**Fix:** for each "implications" sentence, either name the implication
specifically or delete the sentence. "Our finding that batch
normalisation degrades calibration suggests that uncertainty-sensitive
applications should consider alternatives" is real. "Our findings have
significant implications for safety-critical systems" is decoration.

### 10. Smooth transition addiction

Real academic prose lets the reader do some of the connective work. AI
prose explicitly bridges every paragraph and every section.

Transition phrases to flag: *Furthermore, Moreover, Additionally,
Building on this, As we have seen, Having established X, we now turn
to Y, In what follows*.

**Fix:** delete most of these. Read the paragraph after deleting the
transition. If it still flows, the transition was decoration. If it
doesn't flow, the relationship needs a more specific connector
("In contrast,", "By the same argument,", "To test this,") rather than
a generic one.

### 11. Section-end summary tics

AI writers like to end every subsection with a one-sentence summary
("In summary, X improves Y."). Real papers do this only where the
section was complex enough to warrant it.

**Fix:** in a paper where every subsection ends with a summary, delete
all but the truly necessary ones (usually only at the end of major
sections).

### 12. Generic future work

AI conclusions almost always end with a generic "future work" paragraph
that lists three plausible-but-unspecific directions.

- "In future work, we plan to explore X, extend Y, and investigate Z."

This is a tell because real future-work paragraphs are either short and
specific ("We plan to test whether the effect persists for transformer
sizes above 13B parameters") or absent entirely.

**Fix:** if the future-work paragraph is generic, either replace with a
specific one (ask the user if needed) or shorten to a single sentence.

### 13. The "comprehensive overview" trap

In related work and background sections, AI defaults to wanting to give
a "comprehensive overview" of the field. Real related-work sections are
**selective**: they cite the works that matter for *this* paper's
argument, not a tour of the literature.

Signs:
- Related work that mentions sub-areas not relevant to the paper.
- Citations to surveys instead of to specific findings.
- Paragraphs of the form "X has been studied in many forms: A [1], B
  [2], C [3], D [4]..."

**Fix:** prune. A focused related-work section that cites 12 papers
deeply beats a survey-style one that cites 60 superficially.

### 14. Polished but voiceless

Even after you remove the AI clichés, the prose can still feel "AI" if
it has no consistent author voice. Real papers have authorial tics:

- An author who uses "indeed" sparingly will use it once or twice in a
  paper.
- An author who likes long sentences with semicolons will use a few.
- An author who prefers "we show" over "we demonstrate" will be
  consistent.

After your edits, the paper's voice should feel coherent, not like a
patchwork of style.

**Fix:** read the paper end-to-end after editing. If two sections feel
like they were written by different people (and they aren't supposed
to be), tighten the prose-style choices to be consistent.

### 15. Suspicious n-gram patterns

Detection tools key on specific n-grams that appear far more often in
AI text than in pre-2023 text. The biggest offenders:

- "in the realm of"
- "delving into"
- "shed light on"
- "play a pivotal role"
- "a testament to"
- "underscores the importance of"
- "navigate the complexities of"
- "in the rapidly evolving landscape of"
- "leverage the power of"
- "a multifaceted approach"
- "intricate interplay"
- "comprehensive understanding"
- "the field of X has witnessed"
- "in light of these findings"
- "as we delve deeper"
- "it is imperative to"
- "with the rise of"
- "in today's data-driven world"

**Fix:** zero tolerance. Search the file for each of these and remove or
rewrite. Even one of these phrases will trip a trained detector.

### 16. AI-typical punctuation rhythm

In LaTeX, the practical version of em-dash overuse is `---` overuse.
LLMs sprinkle these where humans would use commas or periods. In a
typical 8-page paper, expect zero to four `---`s in real human writing;
ten or more is suspicious.

**Fix:** count `---` in the file. If there are more than five or six in
a normal-length paper, audit each one. Replace with a comma, a period, or
a parenthetical pair where appropriate.

Same applies to colons used to introduce a punchy follow-up clause
("X is the goal: Y is the means.") and to semicolons used as a
"sophisticated" linker rather than for genuine list-of-clauses use.

### 17. Heading-case inconsistency

If the paper mixes sentence case and title case across headings, that's
a tell that an AI generated different sections separately. Pick one
based on the venue (see `domain-conventions.md`) and apply consistently.

### 18. The honest test

After all the above, do this final pass for each paragraph you rewrote:

1. Read the paragraph aloud (or at least sub-vocalise it).
2. Ask: "Does this sound like the same person wrote it as the rest of
   the paper?"
3. Ask: "If a reviewer paused on this paragraph, would they pause
   because of *what it says* or because of *how it's written*?"

If the answer to #3 is "how it's written", the paragraph is not done
yet, even if every checklist item passed.

## Working with humanizer.md

After this pass, return to `humanizer.md` and run its self-audit loop on
the rewritten paragraphs:

> "What makes the below so obviously AI generated?"
> [list residual tells honestly]
> "Now make it not obviously AI generated."

Then revise once more.

`humanizer.md` already includes the explicit guidance that the general
humanizer's "add soul" advice (first-person opinions, mixed feelings,
tangents) does **not** apply to academic writing. The equivalent in a
paper is *consistent terminology, sentence rhythm, and structural
choices*, not personality. If your pass is making the paper sound like a
blog post, you have over-applied. Pull it back.

## What good looks like

A paragraph that has passed all of the above:

- Has a specific claim, supported by specific evidence (numbers,
  citations, references to figures or sections).
- Uses a tense and voice consistent with the rest of the paper and the
  field's conventions.
- Has at least one sentence noticeably shorter or longer than the others.
- Does not begin with "Furthermore" or "Moreover".
- Does not end with a participial clause that adds nothing.
- Uses each technical term consistently throughout.
- Hedges where the literature is uncertain, not where the data is firm.

If most of the paragraphs in the rewritten paper meet these criteria,
the paper will not read as AI-generated to a knowledgeable reviewer or
a detector.
