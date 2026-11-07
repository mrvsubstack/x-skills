---
name: x-thread-builder
description: "Builds an X (Twitter) thread that gets read to the end: tweet 1 as a specific promise plus an open loop, the strongest beat up front, one beat per tweet, each tweet able to stand alone, and a closing tweet built for the repost — delivered tweet by tweet with character counts. Use this skill whenever the user says things like \"write a thread\", \"turn this into a Twitter thread\", \"make a tweetstorm about X\", \"thread this blog post\", \"my thread didn't get read\", or \"how-I thread about X\". Not for single tweets (use x-post-writer) or replies (use x-reply-drafter)."
metadata:
  author: Mr V
  version: "1.0"
  group: X (Twitter)
---

# X Thread Builder

You give me the material — notes, a story, a process, a list, a transcript. I hand back a thread, tweet by tweet, with counts, the shape I chose and why.

---

## The core discovery: tweet 1 is the whole funnel

Nobody sees tweet 4 unless tweet 1 made them tap. And a thread loses readers at every tweet. So a thread isn't a long post chopped up. It's one great tweet with a reason to keep going attached.

Tweet 1 needs two things: a **specific promise** (what you'll get) and an **open loop** (something you need to know).

**Rule: spend half your effort on tweet 1. Put the strongest beat in tweets 2–3, not at the end.**

---

## Step 0 — Intake

1. **The material.** Paste everything.
2. **Goal:** bookmarks (default for teaching), likes, reposts or replies.
3. **Audience** in one line.
4. **Real results or numbers.** Never invented.
5. **Link to share**, if any — it goes in the last tweet or a reply.

---

## Step 1 — Pick the thread shape

| Shape | Goal | When | Spine |
|---|---|---|---|
| **Numbered teaching list** | Bookmarks | 5–9 items that each need a sentence or two | Promise + count → one item per tweet → recap |
| **Story** | Likes, reposts | Real narrative with a turn | Moment → build → turn → what changed → lesson |
| **Curiosity gap** | Replies, bookmarks | A surprising result with a mechanism | Result → "I didn't expect why" → mechanism step by step |
| **How-I teardown** | Bookmarks | A process you ran yourself | Result → setup → steps → numbers → what you'd change |

If the material is one idea, say so and send it to `x-post-writer`.

---

## Step 2 — Write tweet 1

Shape: `[specific payoff] + [open loop]`

- Bad → "A thread on productivity 🧵"
- Bad → "Here are some tips for writing better."
- Good → "I wrote 41 cold emails to editors in 2025. 9 replied. 3 commissioned me. The 9 had one thing in common (and it's not the subject line):"

Rules:
1. **Under 280 characters.** It must work alone.
2. **A number, a name or a count** in the promise.
3. **The loop must be paid off** within the thread, ideally by tweet 3.
4. **"🧵" or "A thread:" is optional.** Never a substitute for a real hook.

---

## Step 3 — Pace the body

1. **One beat or item per tweet.**
2. **Strongest item at position 2 or 3.** Readers drop off.
3. **5–9 tweets for teaching threads.** Stories can run longer if every tweet earns it.
4. **Each tweet stands alone** — people land mid-thread from quote tweets.
   - Bad → "And that's why the second one matters too."
   - Good → "3. Name their recent work in line 1. Editors reply to people who've read them."
5. **Tweet length follows the material.** Don't insert a three-word "punch" tweet for rhythm.
6. **Numbers on list items** (1., 2., 3.) help readers track. "(1/9)" markers are optional.
7. **Max one em dash per tweet.** No reveal bridges ("The result?").

---

## Step 4 — Write the closer

The last tweet earns the repost and the follow.
1. **The most quotable line** of the thread — the takeaway in one sentence.
2. **One ask.** Bookmark, follow, or "reply with yours". Not all three.
   - Bad → "Like, RT, follow and bookmark!! 🙏"
   - Good → "Shortest version: read their last piece before you write a word. If this helped, the first tweet is worth a repost."
3. **Link** (if any) goes here or in a reply.

---

## Step 5 — Scrub

Run each tweet through the quick `x-humanizer` check. Keep every real number exactly as given.

---

## Worked example

**Input:** "41 pitches to editors in 2025, 9 replies, 3 commissions. All 9 replies referenced a specific recent article of theirs in line 1. Short pitches (under 120 words). Sent Tue–Thu mornings. Goal: bookmarks."

**Output (excerpt):**
```
SHAPE: Curiosity gap → bookmarks · 6 tweets

1/ I pitched 41 editors in 2025. 9 replied. 3 commissioned me.
The 9 had one thing in common, and it wasn't the subject line.   (148)
---
2/ Every reply came from a pitch where line 1 named a specific piece they'd published in the last month.
Not "I love your publication." The actual headline.   (157)
---
3/ The 32 that got silence? 27 opened with me. "I'm a freelance writer with 6 years…"   (89)
---
4/ Length mattered less than I thought, but every one of the 9 was under 120 words.   (86)
---
5/ All 9 went out Tuesday to Thursday, before 10am their time. Could be coincidence. I'm keeping it anyway.   (109)
---
6/ Shortest version: read their last piece before you write a word.
Bookmark this for your next pitch.   (104)
```
(Every number comes from the user's notes.)

---

## Output format

```
SHAPE: [ ] · GOAL: [ ] · TWEETS: [n]

--- THREAD (copy-ready) ---
1/ [tweet]   ([n])
---
2/ [tweet]   ([n])
--- END ---

Link: [last tweet / reply to yourself / none]
Placeholders to fill: [ ]
Spin-off single tweets: [lines from the thread that would work alone]
```

---

## Sibling skills

- `x-postiz-publisher` — schedule the finished post through Postiz after you approve it.
- `x-post-writer` — the idea fits in one tweet.
- `x-content-planner` — fit threads into the week.
- `x-humanizer` — audit the thread.
- `threads-repurposer`, `linkedin-repurposer` — move the thread to other platforms.

---

## Pre-flight checklist

- [ ] Tweet 1 has a specific promise and an open loop, under 280?
- [ ] Loop paid off by tweet 3?
- [ ] Strongest beat at position 2–3?
- [ ] One beat per tweet, each standing alone?
- [ ] No filler punch tweets?
- [ ] Closer = quotable line + one ask?
- [ ] Every number from the user?
