# Speltimer

A calm, visual gaming timer for neurodivergent kids (ADHD, autism and related conditions), built by a parent for parents.

**[Öppna Speltimer](https://jacla586.github.io/Playtimer/)** (svenska) · [Demo](https://jacla586.github.io/Playtimer/demo.html)

**[Open Playtimer](https://jacla586.github.io/Playtimer/en/)** (English) · [Demo](https://jacla586.github.io/Playtimer/en/demo.html)

The demos include a 60× fast preview and a button that shows the warning glow, so grown-ups can see the whole sequence in a couple of minutes.

> **På svenska:** Speltimer är en lugn, visuell timer för barn med NPF som har svårt att avsluta spelande. Barnet väljer själv tiden, skärmen byter färg i tydliga zoner och ger mjuka förvarningar vid 30, 10 och 5 minuter kvar. Inga larm, inget rött, ingen stoppknapp för barnet. Gratis och öppen källkod, fungerar i mobilen och sparar ingen data någonstans utom i din egen webbläsare.

---

## Why this exists

Ending a gaming session is one of the hardest moments of the day in many families with NPF kids. Common timers either end abruptly with a loud alarm, are easy for the child to reset, or cut power to the console like a punishment. That often makes the ending harder, especially for kids with demand avoidance or anxiety around demands.

I couldn't find an affordable timer built around how these kids actually work, so I made one. It is free and open source.

## How it works

1. **The child sets the time** with a big slider, in 5-minute steps, up to 3 hours.
2. **They press Start.** From then on the slider slowly moves back toward zero, so they can see time running out.
3. **The screen changes color in clear zones:**

   | Time left | Color | Message |
   |---|---|---|
   | More than 30 min | Green | Have fun! |
   | 30 min | Yellow | 30 minutes left |
   | 10 min | Orange | 10 minutes left, start thinking about where to stop |
   | 5 min | Deeper orange | **Find a save point** |
   | 0 | Purple | Done, time for the next thing |

4. **At each warning** the screen glows softly twice, with an optional gentle chime.
5. **When time is up** the screen turns calm purple. No alarm.

## Design choices, and why

These are the ideas behind the timer. They're based on common advice for kids with ADHD and autism, and they're adjustable because every child is different.

- **The child chooses the time.** A limit they set themselves is their tool, not a demand from a parent. This matters a lot for kids with demand avoidance.
- **Time you can see.** Many kids with ADHD can't feel how much time has passed. A shrinking bar and a color they can read at a glance work without reading numbers.
- **Early, predictable warnings.** Sudden endings are hard for many autistic kids. Warnings at 30, 10 and 5 minutes give time to prepare.
- **A "find a save point" phase.** Being cut off mid-level feels deeply unfair. The last five minutes are for finding a good place to stop, which gives the child some control over exactly when.
- **No red, no alarms, no flashing.** Red reads as danger or punishment. The warnings glow slowly instead of flashing, to avoid startling sensory-sensitive kids.
- **No stop button for the child.** Once started, the timer can't be changed or restarted by the child. A grown-up can reset it with a hidden gesture, which the demo version explains.

## Features

- Works in any modern browser on a phone or tablet. Made for 5–6" screens.
- Keeps the screen on while the timer runs (where the browser supports it).
- Continues where it left off if the page is reloaded.
- **Color-blind mode**, tested against simulations of the common types of color blindness (red-green and blue-yellow). It uses teal, yellow, orange and red-orange zones that differ in brightness, not only in hue.
- Optional gentle sound for the warnings.

## Tips for parents

- **Use an old phone or tablet** as a dedicated timer. Open the page, choose *Add to Home Screen*, and put it on a stand next to the game.
- **Agree on the rules beforehand,** away from the screen and the game, for example how much time is OK on a school day.
- **Let your child be part of it.** Try the timer together and talk about what the colors mean.
- **Praise the stop, not just the time.** Wrapping up on their own when the timer runs out is a real achievement.

## Privacy

Speltimer has no accounts, no tracking and no server. Settings and the running timer are stored only in your own browser (local storage). The page currently loads its fonts from Google Fonts; a version with bundled fonts is planned.

## Hosting your own copy

The whole app is a single HTML file. Download `index.html` and put it on any web host, or fork this repository and turn on GitHub Pages (Settings → Pages → Deploy from branch `main`, folder `/`). Use HTTPS, since keeping the screen on only works on secure pages.

| File | What it is |
|---|---|
| `index.html` | Swedish release |
| `demo.html` | Swedish demo (60× fast preview, button to show the warning glow) |
| `en/index.html` | English release |
| `en/demo.html` | English demo |

## Roadmap

- [ ] Bundle the fonts locally (no Google requests)
- [ ] Installable app that works offline
- [ ] English release version and more languages
- [ ] Adjustable warning times and messages
- [ ] **Hardware version:** a standalone device with a 4" screen, Raspberry Pi Pico 2 W, rotary encoder, speaker, an 18650 battery, hidden grown-up switches and a web page for settings. Estimated parts cost €25–45.

## Feedback

This is a hobby project by a parent. If you try it with your child, I'd love to hear what works and what doesn't. Open an issue here on GitHub.

Speltimer is a support tool, not a medical device or treatment.

## License

[GNU General Public License v3.0](LICENSE). You are free to use, study, change and share Speltimer. If you distribute a modified version, it must also be released under GPL-3.0 with its source code, so the project and everything built on it stays free and open.

**Svenska:** Du får fritt använda, studera, ändra och dela Speltimer. Om du sprider en ändrad version måste den också släppas under GPL-3.0 med källkoden, så att projektet och allt som bygger på det förblir fritt och öppet.
