# claude-helpers

A few markdown files I keep in my Claude projects to make Claude better at specific things: prompting, copy, marketing strategy, knowledge management.

## How to use

Drop the files wherever Claude can see them.

- **Claude Code**: `@`-mention a file in chat, or have a subagent `Read` it.
- **Claude.ai**: upload to a Project as Project Knowledge.
- **Cowork**: keep them in your working directory and reference by name.

Each file works as project knowledge (Claude pulls from it automatically across every conversation) or as a one-shot drop into a single chat.

## The files

### prompting-cookbook.md

Anthropic's prompting docs condensed into one file. XML structuring, chain of thought, multishot examples, model-specific tips for Claude 4.x / 4.5 / Opus 4.6, strategies for reducing hallucination, Cowork patterns. Based on docs.anthropic.com as of Feb 2026.

### copywriting-masters.md

Persuasive-copy diagnostics and theory built around six classic copywriters: Schwartz, Hopkins, Halbert, Caples, Collier, Ogilvy. The top of the file is a diagnostic that picks the right master based on audience awareness and market sophistication. Useful when Claude is writing sales pages, ads, or pitches.

### marketing-frameworks.md

Frameworks pulled from 13 marketing books (Blue Ocean Strategy, Cialdini's *Influence*, *Yes!*, *Pre-Suasion*, *Made to Stick*, and others). Reference material for positioning, offers, funnels, strategy.

### llm-wiki-pattern.md

A pattern for using an LLM to build and maintain a personal knowledge base. The LLM does the bookkeeping (cross-references, summaries, contradictions) that humans normally abandon. Pairs well with Obsidian.

### qa-agent-template.md

A reusable pre-release QA agent. Built around iOS/Swift but the structure adapts to any language. You fill in the project-specific scope sections; the role definition, examples, and self-critique step stay the same.

## Why files instead of prompts

These are too long to paste every time, and too specific to bake into a system prompt. Putting them in a repo means you can version them, diff them, branch them, and Claude picks them up across every conversation in a Project.

## Attribution

The prompting file is a condensation of Anthropic's public documentation. The copywriting and marketing files distill principles from published books; author and title credit appears inline in each file. The LLM wiki pattern is an original write-up.

## What's not in here

Voice profiles of named people, anything tied to private products, anything with personal data. If you fork this, do the same: generic templates public, product-specific stuff private.

## License

[CC BY 4.0](LICENSE). Use, adapt, share. Credit `claude-helpers`.

## Contributing

Open an issue if you've built something similar and want to compare notes. Not actively taking PRs.
