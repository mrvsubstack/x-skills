---
name: x-profile-optimizer
description: "Audits an X (Twitter) profile the way a stranger sees it in two seconds — display name, handle, bio, photo, header, pinned post and link — and rewrites each weak part so profile visits turn into follows. Use this skill whenever the user says things like \"fix my Twitter bio\", \"review my X profile\", \"what should I pin on X\", \"rewrite my bio in 160 characters\", \"what should my header say\", or \"X profile audit\". Not for writing tweets (use x-post-writer)."
metadata:
  author: Mr V
  version: "1.0"
  group: X (Twitter)
---

# X Profile Optimizer

You paste your display name, handle, bio and link, describe or screenshot your header, and paste your pinned tweet. I hand back a scorecard, the top fixes and copy-ready rewrites inside X's limits.

---

## The core discovery: the follow happens on the hover card

On X, many follow decisions happen before anyone opens your profile — on the hover card or the quick glance after a good reply. That shows: **name, bio, and follower count**. If they click through, they see the **pinned post** next.

Name + bio + pin. That's your two-second pitch.

**Rule: the bio says what a follower gets. The pin proves it. Everything else supports those two.**

---

## Step 0 — Intake

1. **Display name, @handle, bio, link, location.**
2. **Header and photo** — screenshot or one sentence each.
3. **Pinned post** text, or "none".
4. **Goal:** grow followers (default), drive signups, land clients, build authority.
5. **Your best-performing tweet or thread**, if known.
6. **Premium or not** (affects some limits).

Score only what you've been shown.

---

## Step 1 — Score seven parts

Limits change — verify with web search and label anything unverified. At the time of writing: bio 160 characters, display name 50.

| # | Part | Passes when |
|---|---|---|
| 1 | **Photo** | Clear face, high contrast, readable as a tiny circle |
| 2 | **Header** | One readable value line or visual, safe on mobile, supports the bio |
| 3 | **Display name** | Your name + a searchable topic word if there's room |
| 4 | **@handle** | Short, sayable |
| 5 | **Bio** | What a follower gets + topic + one proof or specific, within limit |
| 6 | **Pinned post** | Your best proof of what following gets you |
| 7 | **Link** | One, matched to the goal |

---

## Step 2 — Rewrite

### Bio — value + topic + proof
1. **Lead with what a follower gets.**
   - Bad → "Entrepreneur. Investor. Thinker. Opinions my own."
   - Good → "I pitch editors so you don't have to guess. Daily notes on freelance writing. 3 commissions from 41 cold pitches last year."
2. **One specific.** A number, a cadence, a niche. Real only.
3. **Skip "opinions my own", "RT ≠ endorsement".** Dead space.
4. **Count characters.**

### Display name
`Name | Topic` if it fits and the topic is what people search. Optional, but it helps search and replies.

### Header
One line, large, readable on a phone, not covered by the photo. Ideas: your promise, your series name, a single proof. Not a busy collage.
- Bad → a stock photo of a laptop.
- Good → "Daily: how freelance writers get paid more" on a plain background.

### Pinned post — pick one shape
| Shape | Use when |
|---|---|
| **Best thread** | You have a thread that clearly outperformed and still represents you |
| **Start here** | "If you're new: I tweet about [topic] for [who]. Best threads: [3 one-liners]." |
| **Proof + offer** | Goal is signups or clients: one result + one link |

Rules: it must still be true; under 280 characters for the first tweet; one ask.

### Link
One destination, matched to the goal: newsletter, booking page, product.

---

## Worked example

**Input:** Name "Jordan Lee". Bio "Writer. Coffee. Dog. Opinions my own." No pin. Goal: grow followers among freelance writers. Detail: tweets daily about pitching; 41 pitches → 3 commissions.

**Output:**
```
DISPLAY NAME  before: Jordan Lee
              after:  Jordan Lee | Freelance Pitching   (31)

BIO  before: Writer. Coffee. Dog. Opinions my own.
     after:  Daily notes on getting commissioned as a freelance writer.
             41 cold pitches → 3 commissions in 2025. Here's every lesson.   (124)

HEADER  "How freelance writers get the yes" — plain background, text right of centre

PIN  Pin the 41-pitch thread (best performer, still on-topic)
```
(41 and 3 are the user's numbers.)

---

## Output format

```
GOAL: [ ] · TWO-SECOND TEST: pass / fail — [why]

SCORECARD: | # | Part | Score | Reason |
TOP 3 FIXES: [ ]

REWRITES (copy-ready, with counts)
Display name · Bio · Header line · Pinned post (or which tweet to pin) · Link

LIMITS: [verified / unverified]
MISSING: [ ]
```

---

## Sibling skills

- `x-thread-builder` — write the thread worth pinning.
- `x-content-planner` — make your tweets match the bio's promise.
- `threads-profile-optimizer`, `linkedin-profile-optimizer` — other platforms.

---

## Pre-flight checklist

- [ ] Two-second test run?
- [ ] Bio within limit, leads with what a follower gets?
- [ ] Pin chosen or written, still true, one ask?
- [ ] Header readable on mobile?
- [ ] No invented proof?
- [ ] Limits verified or labelled?
