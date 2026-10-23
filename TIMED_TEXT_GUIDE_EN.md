# Universal Timed Text Style Guide (TTSG) — Streaming Standard

> **Global Technical and Editorial Reference for Professional Subtitling & Captioning**  
> Covers universal timing standards, shot change rules, formatting, SDH (Subtitles for Deaf and Hard of Hearing), and Forced Narratives (FN).

---

## 1. Core Technical Limits

| Parameter | Specification |
| :--- | :--- |
| **Max Lines** | **2 lines** per subtitle event (always prefer a single line when possible). |
| **Max Characters per Line** | **42 characters** (Latin-based scripts). |
| **Min Duration** | **5/6 second (~833 ms)** $\rightarrow$ **20 frames** at 24 fps (25 frames at 30 fps). |
| **Max Duration** | **7 seconds** per subtitle event. |
| **Min Frame Gap** | **2 frames** between consecutive subtitles across all frame rates. |
| **Reading Speed (CPS)** | **Adults:** Up to **17–20 CPS** \| **Children:** Up to **13–17 CPS** *(includes spaces & punctuation)*. |
| **Alignment** | **Center-justified**, bottom of the screen. Move to the top if lower-third on-screen graphics or burned-in text exist. |

$$\text{CPS} = \frac{\text{Total Characters (including spaces and punctuation)}}{\text{Duration in seconds}}$$

---

## 2. Timing to Shot Changes

* **Snap to Cut (Red Zone — 1 to 7 frames):**
  * If dialogue starts within 1–7 frames after a cut, snap the in-time to the first frame of the new shot.
  * If dialogue ends within 1–7 frames before a cut, snap the out-time to **2 frames before the cut**.
* **Green Zone (8 to 11 frames):**
  * Cushion with a half-second margin (12 frames at 24 fps) to avoid micro-flashes near edit points.
* **Crossing Shot Changes:**
  * Subtitles may cross a shot change only if speech is continuous across the cut and splitting the event would violate minimum duration (20 frames) or reading speed limits. **Legibility always takes precedence over camera cuts.**

---

## 3. Line Breaks & Syntax Rules

* **Inverted Pyramid Rule (Bottom-Heavy):** The second line should be equal to or longer than the first line for ergonomic eye-tracking.
* **Never separate:**
  * Article from Noun
  * Adjective from Noun
  * Subject Pronoun from Verb
  * Auxiliary Verb / Negation from Main Verb
  * Preposition from its object
  * First Name from Surname / Title from Name
* **Preferred break points:** After strong punctuation, before coordinating/subordinating conjunctions, or before prepositions.

---

## 4. Typography & Punctuation

* **Ellipsis:** Always use the single smart Unicode character **`…`** (`U+2026`). Never type three consecutive dots (`...`).
  * Never use ellipses or dashes to link continuous sentences across sequential subtitles.
* **Dual Speakers:** Use a hyphen followed by a space (`- `) on each line. Maximum one speaker per line.
* **Italics:**
  * Off-screen narrator and voice-overs.
  * Electronic devices (phone, radio, loudspeaker, AI) when the speaker is not in the physical room.
  * Sung song lyrics.
  * Foreign words and phrases not assimilated into the target language.
* **Song Lyrics:**
  * Enclose each subtitle event with single music notes and spaces: `♪ Lyric line ♪`.
  * Capitalize the first letter of each lyric line.
  * Do not use trailing periods or commas on lyric lines (retain `?` and `!` if needed).

---

## 5. Forced Narratives (FN)

* Used for un-dubbed foreign dialogue and plot-pertinent on-screen graphics (letters, signs, smartphone texts).
* **On-screen graphics translation:** Must be formatted in **ALL CAPS**.
* **Foreign spoken dialogue:** Formatted in sentence case.
* Never combine dialogue and on-screen graphic translations within the same subtitle block.
* Delete redundant FNs if the viewer can naturally read the on-screen text or if a character reads it aloud.

---

## 6. SDH (Subtitles for Deaf & Hard of Hearing)

* **Speaker Identifiers:** In square brackets with title case for names: `[John]`, `[officer]`.
* **Sound Effects:** In square brackets with lowercase letters: `[screaming]`, `[engine revs]`, `[whispering]`.
* Describe sound qualities rather than obvious visual actions.
* Higher reading speed allowance: up to **20 CPS** for adults and **17 CPS** for children.
