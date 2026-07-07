# ॐ Spouse Match Scorecard — Astro-Gyani Calculator

A cinematic, single-file web app that computes Vedic marriage compatibility from two people's birth details and presents it as an interactive scorecard out of 100.

**Live demo:** enable GitHub Pages (Settings → Pages → Deploy from branch → `main` / root) and the app will be served at `https://smayankthakur.github.io/Spouse-Match-Scorecard-Mayank/`

## What it does

1. **Enter both persons' birth details** — name, date, time, and timezone of birth.
2. **Real astrological calculations** — a built-in astronomy engine computes sidereal planetary positions (Moon ±0.3°, planets ~±1°, Lahiri ayanāṁśa) and runs the classical rules:
   - Full 36-point **Aṣṭakoota Guṇa Milan** — Varṇa, Vaśya, Tārā, Yoni, Graha Maitrī, Gaṇa, Bhakūṭa, Nāḍī
   - **Maṅgal Doṣa** from the Moon chart, with cancellation check
   - **Planetary dignities** (exalted / own / friend / neutral / enemy / debilitated) for the 7th lord, Jupiter, Venus, Mercury, and Saturn
3. **A unique scorecard per couple** — Section A comes directly from the chart math; Sections B–D (Loyalty, Temperament, Life & Family) are astrological suggestions derived from the Moon sign, Gaṇa, and dignities.
4. **Tweak & restore** — every score is adjustable by slider (tweaked values are marked); one click restores the calculated originals. All state auto-saves in the browser.

## Features

- **Constancy Gate** — if Loyalty & Constancy scores below 15/30, the verdict is overridden with a caution regardless of the total.
- Radian-style cinematic presentation: full-screen layered parallax hero, masked line-reveal typography, a pinned scroll-scrubbed section cycling the eight kootas (01/08 → 08/08), word-by-word statement reveals, film grain, glassmorphism cards, animated score gauge, and confetti for a gate-passing 80+.
- Computed chart summary: each person's rāśi, nakṣatra + pada, Gaṇa / Nāḍī / Yoni, and manglik status with animated koota bars.
- Print / Save-PDF with a clean light layout.
- Zero dependencies, fully offline — everything (astronomy engine, artwork, animations) is in one `index.html`.

## Running locally

Just open `index.html` in any modern browser. No build step, no server needed.

## Accuracy & disclaimer

Planetary positions use low-precision series (Meeus / JPL approximate elements), accurate to about a degree — sufficient for sign and nakṣatra placement except very close to boundaries. Maṅgal Doṣa is judged from the Moon chart (Chandra Kuṇḍalī) since birth-place coordinates are not collected. If exact birth time is unknown, 12:00 works on most days but the Moon sign can shift on transition days.

This is a reflective tool built on a traditional interpretive craft — not a substitute for a professional jyotiṣī, and never a substitute for genuine mutual love, respect, and your own judgment. Score both ways: each person should find the other their best fit.

## License

[MIT](LICENSE.md)
