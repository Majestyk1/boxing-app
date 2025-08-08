# Boxing App — v1 Plan

## Vision
Unify boxing data into a clean, fast mobile app. On launch, show eye-catching **upcoming fight cards**. Let users **search fighters by name** or **browse by division**. Tapping a fighter opens a **profile** with core details and recent bouts. v1 uses general data from the Boxing Data API.

## Scope (MVP)
- **Home (Landing):** list of upcoming fights (title fights highlighted).
- **Fighter List:** search by name, filter by division (17 pro classes).
- **Fighter Profile:** photo, name/nickname, weight class; record (W/L/D, KOs); stance, height, reach, debut year, nationality, DOB; last 5 fights (opponent, result, date). Show “—” if missing.

## Non-Goals (v1)
- Rank tiers, conditioning engine, uploads/sensors, accounts, notifications, real-time, charts/AR/ML.

## Tech
- **Mobile:** React Native + Expo (JS)
- **Backend (later):** Convex for queries/sync
- **Data:** Boxing Data API (RapidAPI)
- **State/fetch:** simple `api.js` (swap to Convex later)

## Milestones
1) **Scaffold (Day 0–1)**
   - Expo app, navigation (Home, Fighters, FighterProfile)
   - Mock data wired, dark theme
2) **Integrate API (Day 1–2)**
   - Home: `/events/schedule`
   - Fighters list: `/fighters/search`
   - Profile: `/fighters/{id}` + last fights
3) **Search & Filter (Day 2)**
   - Debounced **name** search
   - **Division** dropdown (17 classes)
4) **Polish (Day 2–3)**
   - Empty/error/loading states
   - Basic offline cache (optional later)
   - Accessibility pass & performance

## Acceptance Criteria
- Home loads fight cards and highlights title fights.
- Fighters list search/filter works; pagination or “load more”.
- Profile shows accurate record and recent bouts.
- API keys not committed; app handles missing fields gracefully.

## Risks & Mitigations
- **Data gaps:** nullable fields → display “—”.
- **Rate limits:** cache list/profile responses; small page sizes.
- **Images:** fallback avatar; defer CDN proxy to v2.

## Post-MVP (v2 ideas)
- Favorites, rankings, conditioning score, notifications, real-time updates, charts, AR overlays.
