---
name: x-humanizer
description: "Strips the patterns that make a tweet or thread read machine-written — AI word clusters, reveal bridges, fragment stacks, stacked triples, performed honesty — while keeping the writer's edge and quirks. Three modes: Rewrite (default), Audit (pass/fail before posting: 280 fit, first 8 words, links, close) and Profile (learn your voice from 3–6 past tweets). Use this skill whenever the user says things like \"humanize this tweet\", \"this thread sounds like ChatGPT\", \"check my tweet before posting\", \"de-AI this\", \"make this sound like me\", or \"learn how I tweet\". Not for writing from scratch (use x-post-writer or x-thread-builder), and not a tool for beating AI detectors."
metadata:
  author: Mr V
  version: "1.0"
  group: X (Twitter)
---

# X Humanizer

You paste a tweet, a thread or a reply. I hand back the clean version, what changed, and a reader verdict: **reads human / mixed / reads AI**.

It fixes what readers notice. It doesn't promise anything about detectors — on 280 characters, their scores mean nothing.

---

## The core discovery: X has its own AI accent

AI on X doesn't sound like AI on LinkedIn. It has a specific accent:
- "Here's the thing nobody tells you:"
- "Most people [X]. The top 1% [Y]."
- "Read that again."
- "This is the way."
- Thread hooks that promise "everything you need to know" and deliver a list of generalities.
- "Simple. Powerful. Free."

Readers on X are fast and cynical. They've seen these a thousand times and they scroll the instant they spot one.

**Rule: kill the accent, keep the edge. A sharp human tweet stays sharp — just without the template.**

---

## The three modes

### Mode 1 — Rewrite (default)
**When:** ready to post. **How:** the four passes below.

### Mode 2 — Audit
**When:** "check this before I post". **How:** the audit checklist. Blockers, Warnings, one fix each. No rewrite.

### Mode 3 — Profile
**When:** "learn how I tweet". You paste 3–6 of your own tweets you liked. **How:** pull checkable habits — lowercase or not, typical length, how you open, punctuation quirks, words you overuse on purpose, how you end. Output as rules with a real example each for `voice-profile-bank`. Never invent one.

---

## The four passes (Rewrite mode)

### Pass 1 — Scrub
Judge each tweet on its own. **2+ markers in one tweet → rewrite that sentence.**

**Vocabulary markers:** game-changer, unlock, leverage, crucial, elevate, landscape, navigate, delve, seamless, "10x" as a verb, "the top 1%", "masterclass" (as filler).

**Single-hit fixes:**
1. "Here's the thing nobody tells you" / "Here's what most people miss".
2. "Most people X. The top 1% Y."
   - Bad → "Most people chase followers. The top 1% chase trust."
   - Good → "My 900-follower account books more calls than my old 12k one."
3. "Read that again." / "Let that sink in." / "This is the way."
4. "It's not X, it's Y."
5. Reveal bridges: "The result?", "The kicker?", "Plot twist:".
6. Thread openers promising "everything you need to know" with no specific.

**Punctuation:** max one em dash per tweet. Replace extras with a comma, colon or brackets — never a full stop.

### Pass 2 — Rhythm
1. **Kill fragment stacks.**
   - Bad → "Simple. Powerful. Free."
   - Good → "It's free and it takes ten minutes."
2. **No three-word "punch" tweets inserted into threads for drama.**
3. **One natural triple is fine; two stacked → break one.**
4. **Don't force variety.** Tweet length should follow the material.
5. **Keep genuine X style** — lowercase, terse, a bit blunt — if that's how the writer tweets.

### Pass 3 — Add (only what the writer gives you)
A tweet reads human with one of:
- A number with a referent ("41 pitches, 3 commissions").
- A named thing.
- A small real moment ("refreshed my inbox 11 times").

If missing, **ask**. Never insert a stat, story, confession or hedge the writer didn't provide.

### Pass 4 — Self-check
1. Did I create fragments or reveal bridges? → merge.
2. Did I blunt a real edge into mush? → restore the writer's take.
3. Did I strip their quirks? → restore.
4. Is every tweet still within 280 (or verified Premium limit)? → trim.

---

## Audit checklist (Mode 2)

**Blockers:**
- Over 280 characters on a standard account.
- First 8 words don't carry the hook.
- Single-hit X template phrase present.
- Unsourced stat or invented-sounding result.
- Thread tweet 1 with no specific promise.

**Warnings:**
- Link in the tweet (if reach matters — verify current treatment).
- Hashtags (usually unnecessary on X).
- Generic close ("Thoughts?", "Agree?").
- 2+ markers in one tweet.
- Nothing specific.

---

## Worked example (Rewrite)

**Input:**
"Here's the thing nobody tells you about writing:
Most people write for likes. The top 1% write for themselves.
Simple. Powerful. Life-changing.
Read that again."

**Output:**
```
Wrote 200 tweets for likes last year. Average: 14.

Wrote 30 about the one thing I actually cared about. Average: 210.

Turns out people can tell.
```
Changes: cut "here's the thing nobody tells you", "most people / top 1%", fragment stack, "read that again" · **asked the user** for 200/14 and 30/210 before using them.
Verdict: reads human.

---

## Output format

```
MODE: [rewrite / audit / profile]
VERDICT: [reads human / mixed / reads AI] (reader estimate, not a detector score)

--- CLEAN VERSION (copy-ready) ---
[tweet or thread, --- between tweets, counts]
--- END ---

CHANGES: [pattern → fix]
NEEDS FROM YOU: [ ]
KEPT ON PURPOSE: [ ]
```

---

## Sibling skills

- `x-post-writer`, `x-thread-builder` — write it first.
- `voice-profile-bank` — store Profile mode rules.
- `final-edit-modes` — edit into Mr V's own voice.
- `threads-humanizer`, `linkedin-humanizer`, `ig-humanizer` — other platforms.

---

## Pre-flight checklist

- [ ] Every X-template phrase removed?
- [ ] Edge kept, accent killed?
- [ ] No fragments created, no dash swapped for a full stop?
- [ ] Nothing inserted the writer didn't give?
- [ ] Every tweet within limit?
- [ ] Verdict labelled as a reader estimate?
