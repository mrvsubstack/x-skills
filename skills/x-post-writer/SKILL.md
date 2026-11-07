---
name: x-post-writer
description: "Writes a single tweet (or a 2–3 tweet mini-thread) using a hook picked by the reaction you want — replies, reposts, likes or bookmarks — inside the 280-character limit, scrubbed of AI tells and delivered copy-ready with options. Use this skill whenever the user says things like \"write a tweet\", \"turn this into a tweet\", \"give me 5 tweet options\", \"make this punchier for X\", \"I need a post for Twitter\", or \"tweet about X\". Not for long threads (use x-thread-builder) or replying to someone (use x-reply-drafter)."
metadata:
  author: Mr V
  version: "1.0"
  group: X (Twitter)
---

# X Post Writer

You give me a thought, a number, a lesson or a pile of notes. I hand back 3 tweet options built on different hooks, each counted, plus my pick and why.

---

## The core discovery: on X, the tweet is the hook

On LinkedIn you get a hook and then a post. On X, for most people, the whole tweet is the hook — 280 characters, and most readers decide in the first 8 words.

Which means the job isn't "write something good". It's "compress one idea until every word is earning its place, and point it at one reaction."

**Rule: one idea, one reaction, one tweet. If you need "and also", you need a second tweet.**

---

## Step 0 — Intake

1. **The idea or raw notes.**
2. **Goal:** replies, reposts, likes or bookmarks. Default: bookmarks for teaching, replies for opinions.
3. **Audience** in one line.
4. **One real detail** — number, date, named tool or person. Never invented; ask once, then drop the claim if there's nothing.
5. **Account type:** standard (280 characters) or Premium (longer posts allowed — verify the current limit). Default: write for 280 anyway. Short travels.

---

## Step 1 — Pick the hook by goal

| Goal | Hook | Shape |
|---|---|---|
| **Replies** | One-line contrarian | "[Common belief] is wrong. [Your opposite, in under 15 words]." |
| | Build in public | "[Real metric, good or ugly]. [What you're doing about it]." |
| **Reposts** | Data point | "[Odd-precision number] [that reframes something familiar]." |
| | Relatable cold open | A shared moment, no setup. Readers repost it because it's them. |
| **Likes** | Relatable cold open | — |
| **Bookmarks** | Mini list | "[n] [things] that [outcome]:" then 3–5 short lines |
| | Swap | "Instead of [weak], try [strong]." |

Give 3 options on different hooks. Recommend one.

---

## Step 2 — Compress

### Rules
1. **First 8 words do the work.**
   - Bad → "I've been thinking a lot recently about how most people approach pricing…"
   - Good → "Raised prices 160%. Lost 2 clients. Revenue up 38%."
2. **Odd-precision numbers.** "38%" over "almost 40%". "$4,730" over "about $5k".
3. **Cut every word that doesn't change the meaning.** "Really", "very", "just", "actually", "I think that".
4. **No hashtags** unless it's a live event tag the audience actually uses. Zero is normal on X.
5. **No link in the tweet** if reach matters — put it in a reply to yourself. Verify current link treatment with web search if the user asks; it changes.
6. **Line breaks are allowed.** A mini list reads better stacked.
7. **Count characters.** Show the count.

---

## Step 3 — Mini-thread (optional)

If the idea needs one extra beat — the proof, or the "how" — write 2–3 tweets:
- Tweet 1 stands alone completely.
- Tweet 2 adds the proof or the example.
- Tweet 3 (optional) adds the takeaway or the link.

More than 3 → use `x-thread-builder`.

---

## Step 4 — Quick scrub

No AI word clusters (leverage, unlock, game-changer, crucial). No "Here's the thing". No "It's not X, it's Y". No staccato "Simple. Fast. Free." unless it's genuinely the user's voice. Run `x-humanizer` for the full pass.

---

## Worked example

**Input:** "I stopped answering emails before 11am and finally finished my book draft. 4 months of trying before that, 6 weeks after."

**Output:**
```
A) Build in public  ← recommended
"Tried to finish my book draft for 4 months.
Stopped opening email before 11am.
Finished it in 6 weeks."
(104 chars) — Goal: reposts/replies. Three plain lines, a real before/after, no lesson spelled out — readers supply it in the replies.

B) One-line contrarian
"You don't need more time to write. You need 3 hours a day nobody can reach you."
(82 chars) — Goal: replies.

C) Swap
"Instead of 'I'll write after I clear my inbox', try 'my inbox opens at 11'."
(77 chars) — Goal: bookmarks.
```

---

## Output format

```
GOAL: [ ]
A) [hook] ← recommended
[tweet]   ([n] chars)
Why: [one line]
B) [hook]
[tweet]   ([n] chars)
C) [hook]
[tweet]   ([n] chars)

Mini-thread (if used): [tweet 2] [tweet 3]
Link (reply to yourself): [or none]
Placeholders to fill: [ ]
```

---

## Sibling skills

- `x-postiz-publisher` — schedule the finished post through Postiz after you approve it.
- `x-thread-builder` — the idea needs 5+ tweets.
- `x-reply-drafter` — replying or quote-tweeting.
- `x-content-planner` — what to post this week.
- `x-humanizer` — scrub or audit.
- `threads-post-writer` — the same idea, warmer, for Threads.

---

## Pre-flight checklist

- [ ] One idea, one goal?
- [ ] First 8 words carry the hook?
- [ ] Under 280 characters (or Premium limit verified)?
- [ ] Every number is the user's?
- [ ] No hashtags, no link in the tweet (unless asked)?
- [ ] 3 options on different hooks, one recommended?
