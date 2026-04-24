# Spotify UX Case Study — Part 1: Research
Empathizing with Alex, a student struggling to find focus music

## 📖 Introduction
As part of a UX research exercise, I was asked to explore the challenge: "Improve how Spotify users find music to listen to." The UX Research team provided three personas representing different user needs. I chose to focus on Alex, a student looking for music to help him study.
This post documents Part 1 of 3 of the project:

- Part 1 — Research (current)
- Part 2 — Prototype
- Part 3 — Validate

---

## 👤 The Persona: Alex

./images/Capture d'écran 2026-04-24 124147.png

**Alex — 28 yo, Seattle, WA**

- Student at Seattle University
- Music expertise: 2/3 · Software expertise: 3/3
- Lives in a dorm with a noisy roommate
- Studies ~3 hours per evening
- Recently bought noise-canceling headphones
- Gets distracted by song lyrics while studying
- Mellow music makes him feel sad → needs a motivating tempo

**Alex's goal**
Find a lyrics-free playlist with a good tempo in under 2 minutes to focus while studying.

---

## 🗺️ The User Journey Map

./images/Capture d'écran 2026-04-24 124401.png

The journey is split into 3 phases: Inquire → Compare → Decide, with pain points identified by the research team on the search results page and playlist selection steps.

---

## 🚶 Walking in Alex's Shoes
To understand Alex's experience, I reproduced his journey on the Spotify desktop app, step by step, setting aside my own habits.

**Context of the simulation:**
- 9pm, simulating a study session
- Noise-canceling headphones on
- Goal: find the right playlist in under 2 minutes

---

### Step 1 — Landing on Home

./images/Capture d'écran 2026-04-24 124609.png

I open Spotify. The Home screen shows "Made For You" recommendations, recently played items, and editorial carousels.

**Thinking:** "None of this tells me what's good for studying."
**Feeling:** 😐 unsure

⚠️ **Pain point:** Home is optimized for casual listening, not task-oriented use cases like studying.

---

### Step 2 — Hesitating between Browse and Search

./images/Capture d'écran 2026-04-24 124932.png

I hover over the left nav. "Browse" is no longer a dedicated tab — it's merged into Search.

**Thinking:** "Ok, Search it is."
**Feeling:** 😐 unsure → 🙂 confident

⚠️ **Pain point:** Entry points for intentional, activity-based discovery are not obvious.

---

### Step 3 — Typing "electro focus" in the search bar

./images/Capture d'écran 2026-04-24 125126.png

I type electro focus. Autocomplete suggests mostly songs and artists — no mood or activity-based suggestions.

**Thinking:** "This is gonna be easy."
**Feeling:** 🙂 confident

⚠️ **Pain point:** Search autocomplete doesn't propose activity/mood queries.

---

### Step 4 — Staring at the results page

./images/Capture d'écran 2026-04-24 125240.png

Results are ordered: Top Result → Songs → Artists → Albums → Playlists (far down the page).

**Thinking:** "Where are the playlists? I searched for a vibe, not a song."
**Feeling:** 😞 disappointed

⚠️ **Pain point:** Results hierarchy prioritizes Songs/Albums over Playlists, even for activity-based queries.

---

### Step 5 — Scrolling down to find playlists

./images/Capture d'écran 2026-04-24 125404.png

Only 3 playlists are visible by default.

**Thinking:** "3 results? That's it?"
**Feeling:** 😞 disappointed

⚠️ **Pain point:** Truncated playlist section forces extra navigation.

---

### Step 6 — Clicking "See all"

./images/Capture d'écran 2026-04-24 125458.png

Full grid appears.

**Thinking:** "Oh, there are more."
**Feeling:** 😌 relieved

---

### Step 7 — Reading playlist titles one by one

./images/Capture d'écran 2026-04-24 125458.png

I read titles: "Electronic Focus", "Deep Focus", "Chill Electronic", "Electro Mix"…
None of them tell me:
- If there are lyrics
- The tempo / BPM
- The energy level
- The overall mood

**Thinking:** "Why is this so difficult?! I'd have to click every single one."
**Feeling:** 😫 overwhelmed

⚠️ **Pain point (major):** Playlist titles carry no information about musical attributes.

---

### Step 8 — Opening a random playlist and previewing

📷 [SCREENSHOT ZONE 10 — Opened playlist "Deep Focus" playing a song]

I click "Deep Focus". First track = present memory. Too slow.

**Thinking:** "This is not what I'm looking for."
**Feeling:** 😤 frustrated

⚠️ **Pain point:** No way to preview a playlist's overall vibe without manually playing tracks.

---

### Step 9 — Giving up and compromising

./images/Capture d'écran 2026-04-24 130949.png

After ~5 minutes of opening and closing playlists, I settle on one that's "good enough".

**Thinking:** "This one will do."
**Feeling:** 😮‍💨 exhausted

⚠️ **Pain point:** The cost of continuing the search outweighs the benefit → the user settles. The <2 min goal is completely missed.

---

## 📝 My Notes & Sketches

./images/rn_image_picker_lib_temp_25422004-6968-4b55-bedb-6bb3fe1b15c0.webp

./images/rn_image_picker_lib_temp_1aaa54c8-f6a3-4af1-a9f7-90780f85f9fc.webp

---

## 💡 Opportunities for Improvement
From the journey simulation, I identified 8 opportunities:

1. **Activity-first entry point on Home** — surface rows like "Focus", "Study", "Deep work" based on context (time of day, history).
2. **Smart autocomplete** — suggest mood/activity queries ("focus", "no lyrics", "instrumental study") as the user types.
3. **Intent-aware results hierarchy** — when the query signals an activity or vibe, prioritize Playlists above Songs/Albums.
4. **Playlist metadata badges** — display `Instrumental · ~120 BPM · High energy · 2h30` directly on the playlist card.
5. **Audio preview on hover** — a 10-second sample of the playlist's overall sound without opening it.
6. **Filter panel on search results** — tempo range, with/without lyrics, mood, energy, duration.
7. **Negative filters** — exclude lyrics, exclude slow tracks (`-slow`, `-vocals`).
8. **"Still searching?" smart rescue** — after 2 minutes without playing anything, offer a curated playlist matching detected intent.

---

## 🧭 Problem Statement

> Alex, a focused student, needs to find a lyrics-free playlist with an energetic tempo in under 2 minutes — because Spotify's search surfaces results by type (songs, albums, playlists) rather than by musical attributes (tempo, vocals, energy), forcing him to manually open and sample playlists one by one until he gives up and settles.

---

## 🔜 Next Steps
In Part 2 — Prototype, I'll translate these opportunities into a Figma prototype focused on the most impactful pain points (metadata badges + filter panel).