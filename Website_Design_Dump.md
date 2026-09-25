# Design Considerations — Feel, Voice, and Detail

## 1. Design Philosophy — The Feel

**In one line:** *A trusted training partner, not a textbook.* Every screen should feel like it was made by people who lift, for people learning to lift — competent and calm, never clinical or condescending.

**Emotional register to hit:**
- **Confident, not intimidating** — a beginner should never feel like the app is showing off or assuming knowledge they don't have
- **Calm, not gamified** — no confetti, no streak-shaming, no "you're falling behind" nudges. Injury prevention is the point, not engagement metrics
- **Direct, not clinical** — form cues should read like a good coach talking to you ("Brace your core"), not a medical disclaimer ("Engage the abdominal musculature")

---

## 2. Voice & Tone (UI Copy)

- Second person, imperative mood for cues: "Keep your knees over your toes," not "The knees should track over the toes"
- Short sentences. If a cue needs a comma, it's probably two cues
- No fitness-bro slang ("crush it," "no pain no gain") — undermines the credibility goal from the main plan
- Error/empty states should sound human: "No exercises match those filters — try widening your search" instead of "0 results found"
- Never make the user feel behind. No "you haven't logged a workout in 5 days" — that's outside the tool's actual purpose anyway (this isn't a tracker)

---

## 3. Spacing & Layout System

- Base unit: **8px grid** (4px for tight internal spacing, 8/16/24/32 for everything else) — keeps rhythm consistent across cards, modals, and detail pages
- Generous whitespace around the video player and instruction list specifically — this is the "trust" content, it shouldn't feel cramped
- Card grid: consistent gutter (16px mobile / 24px desktop), 2 columns mobile → 3–4 desktop
- Line length for body/instruction text: cap around 60–75 characters even on wide desktop screens — long lines are harder to scan mid-workout

---

## 4. Sizing Details

- **Tap targets:** ≥44px — extends to filter chips and comment upvote buttons, not just primary CTAs
- **Type scale** (suggested, mobile-first):
  - Body/cues: 16px
  - Card title: 18px
  - Section headers (Detail page): 22–24px
  - Page title: 28–32px
- **Video player:** never smaller than ~280px wide on mobile even in a modal — legibility of the movement matters more than fitting more UI on screen
- **Icons:** 20–24px standard, 16px only for inline/secondary use (e.g., next to a tag)

---

## 5. Iconography & Visual Cues

- Use icons functionally, not decoratively — e.g., a small ⚠ only where it flags real injury risk (special-considerations content on the Detail page), not on every card
- Muscle group tags: consider simple colored dot or small icon per group (legs, back, push, pull) for fast visual scanning in the grid, in addition to text
- Difficulty badges: keep to a simple 3-tier visual (e.g., filled dots: ●○○ Beginner, ●●○ Intermediate) — avoid color-only coding (red/yellow/green) since that fails colorblind users; pair with shape or fill

---

## 6. Motion & Micro-interactions

- Keep motion minimal and fast (150–200ms transitions) — this is a utility app used mid-workout, not a showcase
- Card → detail transition: a subtle scale/fade is enough; avoid elaborate page transitions that delay getting to the video
- Loading states: skeleton cards for the grid (not spinners) so the layout doesn't jump
- No motion that could read as "gamified" (no bouncing badges, no celebratory animations) — consistent with the calm, non-gamified tone above
