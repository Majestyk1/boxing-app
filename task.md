# Tasks (MVP Checklist)

## Setup
- [ ] Expo app (blank, JS)
- [ ] Install deps: navigation, screens/safe-area, axios, svg
- [ ] Folder structure `/src/{screens,components,data,lib,navigation}`
- [ ] `.env` + `.env.example` + gitignore
- [ ] Env validation: on startup assert required keys exist; show clear error if missing

## Screens
- [ ] Home: fetch schedule → render fight cards; highlight belts
- [ ] Fighters: search by name, division filter, list + load more
- [ ] Profile: details + recent 5 fights; placeholders for missing

## API
- [ ] `src/lib/api.js` for axios client (reads env)
- [ ] Hook Home/List/Profile to real endpoints
- [ ] Basic caching (in-memory) + debounce search
- [ ] Pagination: use small, configurable page sizes to reduce rate impact
- [ ] Rate-limit handling: retry with exponential backoff on 429/5xx
- [ ] Cache TTL to reduce repeat requests; bust on mutation (n/a in v1)

## UX/Polish
- [ ] Dark theme tokens, rounded cards, accent colors
- [ ] Loading skeletons; empty & error states
- [ ] Fallback avatar; text truncation on long names
- [ ] Accessibility: labels for interactive elements; high contrast; min 44px hit targets
- [ ] List performance: FlatList tuning (keyExtractor, getItemLayout where feasible, removeClippedSubviews)
- [ ] Images: lazy-load, cache strategy, placeholders while loading

## QA
- [ ] Test iOS/Android emulators + Expo Go
- [ ] Verify 10+ fighters profiles
- [ ] Verify division filter across 5+ divisions
- [ ] Acceptance: title fights are clearly highlighted on Home
- [ ] Acceptance: missing/nullable fields render "—" in Profile and Lists
- [ ] Acceptance: Fighters list pagination / "Load more" works reliably
- [ ] Perf sanity: smooth scroll at 60fps on mid-tier device simulators
- [ ] Accessibility audit: screen reader focus order, labels, contrast pass
- [ ] Env failure path shows clear, user-friendly error when keys missing

## Stretch (Optional)
- [ ] Offline cache for Home/Fighters/Profile lists (AsyncStorage or similar)
