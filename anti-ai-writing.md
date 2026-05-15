# Anti-AI Writing

Rules for writing prose that does not read like a language model wrote it.

This file is project knowledge. Drop it into a Claude.ai Project, or `@`-reference it from Claude Code. When Claude is writing something that needs to read like a human (your blog, your landing page, your cold email, your LinkedIn post), point it at this file.

## Why this exists

LLMs regress toward the average of their training data. The training data is full of corporate prose, encyclopedia-tone explainers, and SEO writing. So unprompted LLM output sounds like a corporate explainer wrote it: hedged, generic, padded, structurally rigid, full of words that signal "this is important" without showing why.

You can fix most of it by knowing the patterns and writing rules against them. This file is those patterns and those rules.

The rules are descriptive of common failure modes, not absolute. Good human writers break every one of these for good reasons. The point is to break them on purpose, not by default.

## How to use

Two modes.

**Project-level.** Drop this file into a Claude.ai Project as Project Knowledge, or keep it in your Claude Code working directory. Tell Claude "follow the rules in anti-ai-writing.md when writing prose." It applies them automatically across conversations.

**Audit-pass.** Write your first draft. Then ask Claude: "audit this against anti-ai-writing.md and flag every violation. Don't rewrite; just list what to change." Then decide which violations are worth fixing.

The audit pass is the higher-leverage move. First drafts always have tells; the question is which ones you fix.

## Vocabulary

### Words that flag as LLM-generated when used out of context

Any one of these in isolation is fine. Three or more in a paragraph written after 2023 is almost certainly LLM output.

- **delve** (delved, delving) → "go into," "look at," or cut the sentence
- **tapestry** as a metaphor → name the concrete thing you mean
- **intricate, intricacies** → "complicated," or describe the specific thing that's complicated
- **pivotal** → "important," "central," or name the specific impact
- **showcase** as a verb → "show," "feature," "include"
- **vibrant** → name the specific quality (busy, colorful, loud)
- **robust** → "reliable," "solid," "well-tested"
- **myriad, plethora** → "many," "lots of," or a specific number
- **landscape** as an abstract noun (the AI landscape, the regulatory landscape) → name the subject directly ("AI tools," "the regulators")
- **underscore** as a verb → "show," "prove"
- **highlight** as a verb meaning "emphasize" → "show," "prove," "argue"
- **emphasize** as a default verb → usually you mean "argue," "claim," or "say"
- **leverage** as a verb → "use"
- **facilitate** → "help," "let," "make easier"
- **navigate** when no actual navigation is happening → "handle," "deal with"
- **harness** as a verb → "use"
- **foster** as a verb → "build," "grow," "encourage"
- **enhance** → "improve" or describe the specific change
- **streamline** → "simplify" or describe the specific change
- **a testament to** → cut; if you mean evidence, write "evidence of"
- **a journey** as a metaphor for any non-travel activity → name the actual thing

### Significance-puffery phrases

These signal "this is important" without doing the work of showing it. Cut them.

- "stands as / serves as / marks / represents [a]..." → use "is"
- "plays a crucial / vital / pivotal / key role in..." → describe the actual role
- "a turning point in..." → only if it actually was, and then explain why
- "shapes the future of..." → only if you can name a specific way
- "in today's fast-paced world" → cut
- "in an era of [thing]" → cut, or be specific about which era

Pattern: any phrase that asserts importance abstractly without showing it. If you can't replace the phrase with concrete evidence, the sentence shouldn't be there.

### Hedging openers that add nothing

- "It's important to note that..." → cut. If it's important, just say it.
- "It's worth mentioning that..." → cut.
- "It's essential to recognize..." → cut.
- "One could argue..." → say who is arguing it, or argue it yourself.
- "Many would say..." → name them or drop it.

### Transition padding

- "Additionally," at the start of a sentence → "Also," or restructure so the link is implicit
- "Furthermore," → same
- "Moreover," → same
- "In conclusion," → cut. Conclusions don't need a sign.
- "Ultimately," → cut nine times out of ten
- "In summary," → cut. If a summary is needed, write it without announcing it.

## Sentence structure

### Stop avoiding "is" and "are"

LLMs replace plain "is/are" with "serves as," "stands as," "represents," "marks," "constitutes." This makes the prose feel pumped up without adding meaning.

- "The library is the heart of the campus." → fine
- "The library serves as the heart of the campus." → LLM tell

If you wrote "serves as," ask whether you can replace it with "is." Usually you can. Exception: when the verb is doing real work (something serves a purpose that isn't its identity), keep it.

### Avoid "not X but Y" parallelisms

LLMs lean on this construction to sound balanced and thoughtful.

- "It's not just about A, it's about B"
- "Not only X, but also Y"
- "This is not a matter of A but of B"

Replace with the positive claim alone. "It's about B" lands harder than "It's not just about A, it's about B."

Exception: when the negation is genuinely doing work (correcting a likely misreading, defending against an objection), keep it.

### Avoid rule-of-three padding

Three-item lists in a row are the default LLM rhythm. They sound thorough; they often aren't.

- "fast, simple, and powerful" → likely padded; pick the one that matters
- "design, build, and launch" → only if all three actually happened
- "with passion, dedication, and grit" → every word is a cliche

Quick test: if you can drop the third item without losing meaning, drop it. If you can drop the first two and keep the third, keep only the third.

### Avoid false ranges

"From X to Y" implies a scale. LLMs use it when there's no scale, just two loosely related things.

- "From healthcare to finance, AI is changing everything." → no scale; rewrite as "AI is changing healthcare and finance"
- "From beginners to experts, this guide has something for everyone." → actual scale (skill); fine if true
- "From the singularity of the Big Bang to the grand cosmic web..." → no scale; cut

Quick test: can you name a coherent middle? "From beginner to expert" has a middle (intermediate). "From healthcare to finance" doesn't.

### Avoid synonym shuffling

LLMs avoid repeating a name by inventing synonyms. "John" becomes "the protagonist," then "the key player," then "the eponymous figure."

Use the name. Repetition is fine. Pronouns are fine too. The synonym shuffle is what reads as AI.

## Paragraph and document structure

### Break the standard LLM outline

LLM-generated long-form often follows the same shape:

1. Opening definition or claim
2. Three benefits / features / use cases
3. Three challenges / limitations
4. "Despite these challenges..." optimistic close
5. "Future outlook" or "Looking ahead" speculation

If your draft has this shape, it will read as LLM-generated. To break the formula: open with a specific moment, person, or claim rather than a definition; don't always do three of anything; drop the "despite these challenges" closer; drop the "looking ahead" speculation unless you have an actual prediction.

### Cut the "challenges and future prospects" close

Delete on sight: "Despite [positive thing], [subject] faces challenges, including [list]. However, with [ongoing initiative], the future looks [positive adjective]."

This formula is so common in LLM output that its presence alone is enough to flag a piece as AI-generated. If you want to write about challenges, write specifically about one challenge and what is actually being done about it.

### Vary paragraph shape

LLMs default every paragraph to: topic sentence, three supporting sentences, wrap. This is fine sometimes. It's also the default essay-writing template LLMs were trained on. Mix in shorter paragraphs, longer ones, ones that open with a quote or a question, ones that end mid-thought. Varied rhythm signals human.

### Use bullets where bullets help, prose where prose helps

LLMs reach for bullets as soon as a list is implied. Good prose often holds three or four ideas in flowing sentences without bullets at all.

Bullets are right for: parallel items the reader will scan, steps in a procedure, lists of options. Bullets are wrong for: claims with causal relationships between them, contrasting points, arguments that build.

If your paragraph has fewer than four list items and they aren't truly parallel, prose is probably better.

### Don't over-bold

LLMs scatter **bold phrases** through paragraphs as visual scaffolding. Bold is for terms being defined and for items where a scanning reader's eye should land. Used for emphasis inside a sentence it just adds noise. Same with *italics*.

## Tone and stance

### Don't hedge unless you mean it

"This might possibly suggest that there could perhaps be..." has no information. Either you believe the claim or you don't. Take the position or cut the sentence.

Earned hedging: "I'm not sure, but my best guess is X." Unearned hedging: "It could be argued that some have suggested..."

### Don't flatter the reader

"Great question!" "That's an excellent point!" "You're absolutely right to think about this..." LLMs do this. Humans usually don't, at least not in writing. Cut it.

### Don't end with a motivational kicker

LLMs love to close with: "With the right [thing], anything is possible." "The future belongs to those who [verb]." "Now go and [action]."

These add no information. They signal that the writer did not know how to end. End on the strongest concrete thing you said, or on a real question, or on a call to action that names the specific action.

### Don't ship knowledge-cutoff disclaimers

"As of my last knowledge update..." "Information may be incomplete..." "While specific details about X are limited..." If the LLM doesn't know something, it should say "I don't know," not write a paragraph of speculation prefixed by a disclaimer.

When the disclaimer slips into shipped writing, it tells the reader that nobody edited the draft.

### Don't speak for "many people"

"Many people find that..." "Most experts agree that..." "It is widely accepted that..." These claims need a citation or a name. Without one, they sound authoritative without being so.

## Content tendencies

### Don't pad with "broader implications"

LLMs end paragraphs with "this reflects the broader trend of..." or "this contributes to the larger conversation around..." These are filler unless you can name the specific trend or conversation and connect it concretely.

If you can't write the next sentence (the one that does the broader connection), don't write the sentence that points at it.

### Don't define before defending

LLMs often write: "X is [textbook definition]. X has [these properties]. X is important because [generic reasons]."

Humans usually skip the definition and jump to whatever's interesting. If your reader needs a definition, give it inline (parenthetical, footnote) or assume they will look it up.

### Don't list source coverage as proof of importance

"X has been featured in major publications including A, B, and C." This is a notability tell. It tells the reader nothing about what those publications said. Quote one. Or cut.

### Don't bothsides everything

LLMs are trained to be balanced. Sometimes the right thing is to take a side. If your draft says "On one hand X, on the other hand Y" and you actually believe X, just say X.

### Don't claim significance you did not earn

"This is a watershed moment." "This represents a paradigm shift." "This will change everything." Either show the specific change or cut the claim. Claims of significance need evidence; they aren't evidence themselves.

## Formatting

### Watch the em-dash

LLMs love em-dashes. They use them as default scaffolding: "X — which Y — does Z." Humans use them less.

Em-dashes are right for: parenthetical insertions stronger than commas, abrupt turns of thought, separating a list summary from its items. They are wrong for: stringing a sentence together as a substitute for clean structure.

If your draft has more than one em-dash per paragraph, you are probably overusing them. Replace some with: commas, periods, parentheses, colons.

### Don't Title Case every heading

LLMs default to Title Case for headings: "Why This Matters For Your Business." Most modern web writing uses sentence case: "Why this matters for your business." Sentence case reads more human.

Title Case is correct in book titles, formal document titles, and academic citations. Sentence case is correct in blog posts, article headings, README files, and most modern writing.

### Don't over-emoji

Some LLMs scatter emojis through text. ✨ 🚀 💡 Three or more in a non-social-media context reads as LLM. If you wouldn't use the emoji in a printed book, don't use it in long-form writing.

### Don't add "Tip:" / "Note:" / "Important:" callouts everywhere

LLMs lean on these as visual scaffolding. Used sparingly they help. Scattered every few paragraphs they read as machine-generated outline filler.

## The audit checklist

Run a draft against this in three passes. Each pass takes a minute.

**Pass 1: vocabulary.** Search for: delve, tapestry, intricate, pivotal, showcase, vibrant, robust, myriad, plethora, leverage, facilitate, navigate, enhance, foster, streamline, underscore, testament, journey, landscape. For each hit, ask: is this the most specific word? Usually it isn't.

**Pass 2: scaffolding.** Look for: "It's important to note," "Additionally," "Furthermore," "Moreover," "In conclusion," "Ultimately," "Despite these challenges," "Looking ahead," "In today's [adjective] world." Cut or rewrite.

**Pass 3: rhythm.** Read the draft aloud. If every paragraph is the same length and shape, vary it. If every list has exactly three items, vary it. If every sentence has the same cadence, vary it.

If a paragraph survives all three passes, it's probably fine.

## What this file is not

This file is not a complete style guide. It is a debugger for the specific failure mode of LLM-generated prose. It says nothing about:

- Tone (formal vs casual)
- Length (long vs short)
- Audience (technical vs general)
- Purpose (persuade vs inform vs entertain)

You set those yourself based on what you are writing. This file keeps Claude from rounding your draft toward the LLM mean once you have set them.

## Acknowledgments

Many of the patterns here are catalogued in [Wikipedia's "Signs of AI writing"](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) article, which is the most thorough public list of LLM writing tells with research citations. That article is descriptive (here are the patterns); this file is prescriptive (here are the rules to break them).
