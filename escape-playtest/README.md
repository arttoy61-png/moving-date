# 자정의 기록실 — Second Edition 2.1

Standalone HTML/CSS/JavaScript game deployed at `/moving-date/escape-playtest/`.
Only this directory is changed. No build, backend or external image service is required.

## Changes

- Mobile: viewport-sized room, three camera zones, fixed inventory/notebook/hint/sound toolbar, bottom sheets, 44px+ principal controls, readable clue dialogs.
- Opening: main menu → START → three story panels → play, with resume and reset.
- Art: original Higgsfield room/character/items/ending preserved and stored locally as WebP. New opening cover, corridor and sealed-file art generated using built-in imagegen.
- Audio: quiet synthesized ambient tones; click, transition, acquisition, unlock, success and ending cues. Starts on the first user gesture due to browser autoplay restrictions. Toggle available on opening and game screens; hidden tabs suspend sound.
- Puzzles: introductory color lock, archive chronology restoration, clock combining book and archive evidence, final reverse-chronology seal lookup. Notes can be reviewed within code/clock dialogs. Hints reveal in stages only after confirmation.
- New save namespace `midnight_archive_ep00_v21`; prior V2 saves remain stored but are not imported because the puzzle chain changed.

## Spoiler: complete solution

1. Desk: blue 4 / red 2 / gold 7. Painting: red → gold → blue. Drawer code 274.
2. Select silver key and open cabinet. Select moon → moth → flame → star, then restore.
3. Archive time slots 23:05 / 23:10 / 23:20 / 23:25. Last transport is star, 23:25. Take spring.
4. Select spring and inspect clock. Torn note: hour = blue + gold = 11; minute = final transport + 15 minutes = 40. Set 11:40.
5. Select recovered tape and inspect exit. Transcript says reverse the restored chronology and map seals to storage numbers. Star 1 / flame 8 / moth 3 / moon 6 → 1836.

## Verification

Browser tests exercise real clicks from a fresh start to escape, wrong inputs, item use, note reading, reload/resume, reset/cancel and hint reveal. Mobile layout checks use 320×568, 360×740, 390×844 and 430×932. Test evidence and screenshots are delivered separately. Do not equate browser emulation with real-device or human difficulty testing.

## Assets

`assets/cover.webp`, `corridor.webp`, `sealed.webp`: new built-in imagegen artwork, 2026-10-14; production prompts delivered separately.
`room.webp`, `yuri.webp`, `items.webp`, `ending.webp`: existing project Higgsfield artwork, downloaded from the original URLs and decoded before WebP export.
No generated image contains puzzle-critical text. All clues are accessible HTML.
