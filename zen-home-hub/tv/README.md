# Zen Home Hub

A calm, Japanese-inspired home screen for an LG OLED G4 (webOS 26), with live wallpapers that follow Singapore time and two notes from home.

| File | What it is |
|---|---|
| `tv/index.html` | The TV display. Four live wallpapers (Three.js + GSAP), clock, two notes, app dock. Open it in the TV's web browser and press OK for full screen. |
| `wallpaper-lab.html` | Preview page for the four wallpapers, with a switcher and the scene schedule. |
| `spec.html` | The original UX spec. |

## Wallpaper schedule (Singapore time)

| Time | Wallpaper |
|---|---|
| 06:00 | 朝焼け Asayake: sunrise over a sea of clouds, light rays, cranes |
| 12:00 | 鯉 Koi pond: sunlit blue pond, blooming lotus, darting koi |
| 18:00 | 夜桜 Yozakura: twilight sakura branch, rising moon, petal gusts |
| 21:00 | 星座 Seiza: zodiac wheel with Cancer (Yi Shiean) and Capricorn (Chee Chung), comet and gold sparkles |

## Notes

The TV shows at most two notes, one from Yi Shiean and one from Chee Chung. A new note replaces that person's previous one.

The notes backend is not built yet. The TV page reads `tv/config.js`:

```js
window.ZEN_CONFIG = { notesUrl: "https://<notes-service>/notes", anonKey: "" };
```

Without it, the wallpapers and clock still run and the TV shows "Notes are not connected yet". The notes service must check the house PIN (sent as the `x-house-pin` header) on the server. Never put the PIN in this repo.

## Changelog

- v0.7 · 27 Oct 2026 · Follows Singapore time. Asayake rebuilt as a sunrise. Seiza gets gold accents, a glowing crab and sea-goat.
- v0.6 · 27 Oct 2026 · Wallpapers mapped to morning, afternoon, evening and night.
- v0.5 · 27 Oct 2026 · Koi pond becomes a sunlit blue pond with detailed lotus.
- v0.4 · 27 Oct 2026 · GSAP choreography on all wallpapers. New swaying sakura branch.
- v0.1 to v0.3 · 27 Oct 2026 · First spec, wallpaper experiments, personalised zodiac.
