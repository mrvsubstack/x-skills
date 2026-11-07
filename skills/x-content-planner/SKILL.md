---
name: x-content-planner
description: "Builds a 7-day X (Twitter) plan: daily tweets with hook and goal, which days get a thread, a single-to-thread mix, and daily reply and quote-tweet targets, with a balance check across replies, reposts, likes and bookmarks. Use this skill whenever the user says things like \"plan my week on X\", \"what should I tweet this week\", \"give me a Twitter content calendar\", \"how often should I post threads\", \"I want to grow on X\", or \"plan my tweets\". Not for drafting a single tweet (use x-post-writer) or a thread (use x-thread-builder)."
metadata:
  author: Mr V
  version: "1.0"
  group: X (Twitter)
---

# X Content Planner

You give me your theme, audience and daily time. I hand back a 7-day plan: what to tweet each day, which days get a thread, and who to reply to — with numbers.

---

## The core discovery: on X, volume and replies beat polish

X moves fast. A tweet's life is measured in hours. Accounts that grow tend to post several times a day and spend real time in other people's replies. One perfect weekly thread, posted into silence, rarely moves anything.

**Rule: plan for frequency (several short tweets a day), one or two threads a week, and a reply block every day.**

---

## Step 0 — Intake

1. **Theme** for the week.
2. **Audience** in one line.
3. **Time per day.** Default: 30 minutes.
4. **Pillars.** Default mix below.
5. **Raw material:** numbers, wins, failures, lessons, questions from this week.
6. **10 accounts** to reply to — peers and a few bigger ones. Archetypes if none.

---

## Step 1 — Pillar mix

| Pillar | Share | Earns |
|---|---|---|
| **Teach** | 35–45% | Bookmarks — lists, swaps, how-I threads |
| **Build in public** | 25–35% | Replies — real numbers, decisions, mistakes |
| **Takes** | 15–25% | Replies, reposts — one-line opinions |
| **Relatable** | 10–15% | Likes, reposts — shared moments |
| **Offer** | max 1–2/week | What you sell |

---

## Step 2 — Set the rhythm

Default for 30 minutes a day:
- **2–4 single tweets a day.**
- **1–2 threads a week**, on the days with the strongest material.
- **Reply block daily:** 10–20 replies.
- **Quote tweets:** 2–3 a week, value-add only.

Rules:
1. **Goal mix across the week:** each of replies, reposts, likes, bookmarks appears at least twice.
2. **No hook more than 3 times a week** among singles.
3. **Every angle from real material.**
   - Bad → "Tue: Teach — 5 productivity tips"
   - Good → "Tue: Thread — the 41-pitch experiment, 6 tweets (from your notes)"
4. **Threads go on your best material, not on a schedule.**

---

## Step 3 — Reply plan

For each day:
- **Who:** 3–5 named accounts (or archetypes) — mix peers and one or two bigger accounts.
- **How many:** 10–20.
- **When:** in the first hour after their tweet, when possible.
- **Pattern:** answer, data point, field note, missing piece, sharper question (`x-reply-drafter`).
- **Never** reply-spam the same account with every tweet. 1–2 a day per account max.

---

## Step 4 — Balance check

- [ ] Several singles a day — fits the user's time?
- [ ] 1–2 threads on the strongest material?
- [ ] Reply block every day?
- [ ] Each goal appears twice or more?
- [ ] At least 2 build-in-public tweets with real numbers?
- [ ] Offer max 1–2?

Posting times: use the user's X analytics if they have them. Otherwise write "check your analytics" — don't present generic times as fact.

---

## Worked example

**Input:** "Freelance writer, audience = other freelancers, 30 min/day. Material: 41 pitches → 3 commissions; raised rate to $0.80/word; lost a client over a rate rise; a reader asked how I find editors."

**Output (excerpt):**
| Day | Type | Pillar | Hook | Goal | Angle |
|---|---|---|---|---|---|
| Mon | Single | Build in public | Build in public | Replies | "Raised my rate to $0.80/word. One client left. Two stayed." |
| Mon | Single | Takes | One-line contrarian | Replies | "Cold pitching isn't dead. Generic pitching is." |
| Tue | Thread (6) | Teach | Curiosity gap | Bookmarks | The 41-pitch experiment |
| Wed | Single | Teach | Swap | Bookmarks | "Instead of 'I'm a freelance writer', open with their last headline." |
| Thu | Single | Relatable | Cold open | Likes | "Refreshing the inbox 11 times after hitting send on a pitch." |
| Fri | Thread (5) | Teach | How-I teardown | Bookmarks | How I find editors' emails (reader question) |
Reply block daily: 15 replies on 4 freelance-writing accounts + 1 editor who tweets about pitches.

---

## Output format

```
WEEK OF [date] · Theme: [ ] · Time/day: [ ]
Pillar mix: [ ]

| Day | Type | Pillar | Hook | Goal | Angle (source) |

REPLY BLOCKS: | Day | Who | Count | Pattern |
QUOTE TWEETS: [2–3, what you'd add]
BALANCE CHECK: [✓/✗ with fixes]
MISSING MATERIAL: [ ]
```

---

## Sibling skills

- `x-post-writer` — draft the singles.
- `x-thread-builder` — draft the threads.
- `x-reply-drafter` — the reply blocks.
- `x-profile-optimizer` — visitors from replies land on your profile.
- `threads-content-planner` — if you post on Threads too.

---

## Pre-flight checklist

- [ ] Rhythm fits the user's real time?
- [ ] Threads placed on strongest material?
- [ ] Reply blocks every day with targets?
- [ ] Goals spread, every angle from real material?
- [ ] Posting times from analytics or labelled?
