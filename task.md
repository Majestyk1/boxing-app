# Tasks (MVP Checklist)

## Setup
- [ ] Expo app (blank, JS)
- [ ] Install deps: navigation, screens/safe-area, axios, svg
- [ ] Folder structure `/src/{screens,components,data,lib,navigation}`
- [ ] `.env` + `.env.example` + gitignore

## Screens
- [ ] Home: fetch schedule → render fight cards; highlight belts
- [ ] Fighters: search by name, division filter, list + load more
- [ ] Profile: details + recent 5 fights; placeholders for missing

## API
- [ ] `src/lib/api.js` for axios client (reads env)
- [ ] Hook Home/List/Profile to real endpoints
- [ ] Basic caching (in-memory) + debounce search

## UX/Polish
- [ ] Dark theme tokens, rounded cards, accent colors
- [ ] Loading skeletons; empty & error states
- [ ] Fallback avatar; text truncation on long names

## QA
- [ ] Test iOS/Android emulators + Expo Go
- [ ] Verify 10+ fighters profiles
- [ ] Verify division filter across 5+ divisions
