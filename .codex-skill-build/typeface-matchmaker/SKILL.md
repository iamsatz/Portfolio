---
name: typeface-matchmaker
description: Helps choose, pair, compare, and replace typefaces based on a user taste bank of commercial and free fonts. Use when the user asks for font recommendations, free or open-source alternatives to paid/commercial fonts, typography direction, font pairings, brand/UI/editorial type choices, or "what free font feels like this paid font" based on their saved typeface references.
---

# Typeface Matchmaker

## Core Rule

Recommend only free, open-source, or clearly free-for-use fonts unless the user explicitly asks for paid fonts too. Never suggest piracy, "free download" mirrors, or unauthorized copies of commercial fonts.

Free does not always mean open source. When the user's project is commercial, call out license uncertainty and prefer sources with clear licenses such as Google Fonts, Fontshare, The League of Moveable Type, Velvetyne, Collletttivo, Uncut.wtf, official GitHub repos, and foundry pages that state a free license.

## Workflow

1. Identify the target typeface or mood.
   - If the user gives a paid font name, match its genre, proportions, contrast, terminals, rhythm, x-height, width, weight range, optical size, and intended use.
   - If the user gives a project context, choose typefaces by role: UI text, editorial text, display headline, logo, mono/code, poster, packaging, or decorative accent.

2. Load only the needed reference:
   - Use `references/taste-profile.md` to understand the user's taste clusters and recurring paid-font anchors.
   - Use `references/free-alternatives.md` to find free candidates and substitution heuristics.

3. Return recommendations in practical tiers:
   - "Closest free feel": the best non-paid substitute for the target.
   - "Cleaner/workhorse option": a safer typeface for real-world usage.
   - "More characterful option": a bolder choice that preserves the taste direction.
   - Include pairings when useful.

4. Explain tradeoffs briefly.
   - Say what matches: contrast, warmth, geometric structure, editorial tone, width, stiffness, friendliness, ink traps, etc.
   - Say what differs: less luxurious, less weird, lower contrast, fewer weights, weaker italics, less optical-size control, etc.

5. Include source/license hints.
   - Mention the source platform for each recommendation.
   - If unsure about current licensing, tell the user to verify the license before shipping.

## Matching Language

Use typography language instead of vague taste words. Prefer observations like:

- "neo-grotesk with a high x-height and slightly softened rhythm"
- "high-contrast editorial serif with sharp, fashion-adjacent display tension"
- "humanist sans with open apertures and UI-safe spacing"
- "geometric sans with circular bowls and a startup/product feel"
- "compressed grotesk for dense headlines"
- "warm retro serif with Cooper/Bookman energy"
- "technical mono with code/editorial crossover"

## Output Shape

For a single paid-font substitute:

```text
For [paid font], try:

1. [Free font] - closest free feel. [Why it matches.] Source: [source].
2. [Free font] - safer/workhorse version. [Tradeoff.] Source: [source].
3. [Free font] - more expressive option. [Tradeoff.] Source: [source].

Pair it with: [free font] for text/UI or [free font] for display.
```

For a project brief, give a small system:

```text
Direction: [short typography point of view]
Display: [font]
Text/UI: [font]
Mono/accent: [font]
Why this works: [2-4 concise sentences]
```

## Boundaries

Do not claim a free font is a clone. Say "alternative," "similar role," "adjacent feel," or "free substitute." If the user wants an exact commercial typeface, suggest licensing it.

Do not over-index on font names alone. A font can share a genre but fail the use case because of width, spacing, language support, missing italics, or too much personality.
