# OhMyQuad — Website UI Research & Design Plan

## 1. Purpose

OhMyQuad's UI needs to make one thing easy: a beginner-to-intermediate lifter should be able to find an exercise, see correct form fast, and trust what they're looking at. Every design decision below is filtered through that goal — clarity and speed over decoration.

## 2. Target User & Design Implications

| User trait | UI implication |
|---|---|
| Beginner-to-intermediate, may feel intimidated by gyms | Friendly, non-clinical tone; avoid dense jargon in the UI copy |
| Looking up form *during* a workout (phone in hand, maybe mid-set) | Mobile-first, large tap targets, minimal typing required |
| Comparing exercises / building a routine | Easy browsing — filters, categories, visual library grid |
| Wants to trust the guidance | Clean, credible visual style; avoid a "meme fitness app" look |

## 3. Visual Style Direction (recommendation)

**Overall feel:** Modern athletic-minimal — closer to Strava or Nike Training Club than a bodybuilding forum. Confident, clean, a little bit of energy in the accent color, but mostly whitespace and clear typography so the video/instructional content is the star.

### Color palette (starting point)
- **Primary:** Deep charcoal / near-black (`#1A1A1A`) — backgrounds, primary text
- **Accent:** Electric orange or lime (`#FF5A1F` or `#C6FF3D`) — CTAs, active states, "start workout" buttons. Pick one, not both.
- **Secondary:** Cool gray (`#6E6E76`) — secondary text, dividers
- **Surface:** Off-white (`#F7F7F5`) for light mode background, keeping cards white for contrast

Rationale: dark + one bright accent reads as "performance app" rather than "medical pamphlet," while staying legible for long reading (form cues, research citations).

### Typography
- **Headings:** A geometric sans-serif (e.g., Inter, Poppins, or Sora) — feels modern and gym-app-appropriate
- **Body:** Inter or system-ui for readability at small sizes on mobile
- Keep form-cue text large (16px+) since it may be read mid-set, at arm's length

### Imagery
- Video thumbnails should be consistent aspect ratio (16:9) with a play-icon overlay
- Use real photos/video stills over illustrations — credibility matters more than personality here

## 4. Key Screens

### 4.1 Home / Landing
- Short value prop (the "why" from the README, condensed to one line)
- Prominent CTA into the exercise library
- Maybe 3-4 featured exercises or a "recently added" row

### 4.2 Exercise Library (core screen)
- Grid or list of exercise cards: thumbnail, name, muscle group tag, difficulty tag
- Filter/search bar: by muscle group, equipment, difficulty
- This is the highest-traffic screen — keep load fast, keep filtering obvious

### 4.3 Exercise Detail Page
- Embedded YouTube video (via API) front and center
- Form cues as a clear, scannable list — not a wall of text (research-backed cues from the README should be presented as short bullet points, e.g., "Brace core," "Knees track over toes")
- Common mistakes section (if content supports it) — high value for injury prevention framing
- Comment/feedback section below the fold, so it doesn't compete with the primary content

### 4.4 Comment/Feedback Section
- Keep lightweight — this isn't a social feed, it's feedback + discussion
- Consider a simple upvote or "helpful" marker on comments so useful form tips surface

## 5. Reference Apps / Inspiration
- **Nike Training Club** — clean video-first exercise detail pages
- **Strava** — dark theme, bold accent color, confident typography
- **StrongLifts / Hevy** — simple, uncluttered exercise library UX for lifters specifically

*(Swap in whatever the team actually looks at — this is a starting point, not a locked list.)*

## 6. Accessibility & Responsiveness Notes
- Mobile-first: most usage will likely be phone-in-hand at the gym
- Sufficient contrast between accent color and background (check against WCAG AA, especially with a bright accent on light backgrounds)
- Video should have captions/transcripts where feasible, both for accessibility and because gyms are loud
- Tap targets ≥44px for anything used mid-workout

## 7. Open Questions for the Team
- Light mode, dark mode, or both?
- Final accent color — orange vs. lime vs. something else?
- Do we want difficulty ratings (beginner/intermediate/advanced) as a filter, or keep the library flat for now?
- How much of the "common mistakes" content do we have ready vs. need to script?

## 8. Next Steps
- [ ] Team picks/adjusts color palette and typography above
- [ ] Low-fidelity wireframes for Library and Exercise Detail pages
- [ ] Confirm YouTube embed behavior (autoplay? related videos shown or hidden?)
- [ ] Align comment section scope with backend capabilities (feature/backend branch)
