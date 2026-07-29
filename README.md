# 🧩 Word Cross / Woord Puzzel

**A tiny, native Android crossword game** — pure Kotlin, no ads, no trackers, ~66&nbsp;KB. Every
puzzle is a generated interlocking ("Zweedse") crossword, and every clue is a real dictionary
definition with the answer masked out. One daily puzzle for everyone, plus free play in three sizes.
**The words, the definitions and the interface are Dutch.**

[![Download APK](https://img.shields.io/badge/download-APK%20v1.0-16a34a)](https://github.com/abons/wordpuzzle/releases/download/v1.0/com.hrbons.wordpuzzle_1.apk)
[![F-Droid repo](https://img.shields.io/badge/F--Droid-add%20repo-1976d2)](https://abons.github.io/wordguesser/)
![size](https://img.shields.io/badge/APK-66%20KB-brightgreen)
![Android](https://img.shields.io/badge/Android-5.0%2B-3ddc84)
![no ads](https://img.shields.io/badge/ads-none-black)

<p align="center">
  <img src="assets/puzzle.png" alt="The daily puzzle, two-thirds filled in, with the clue for the selected word under the grid" width="250">
  &nbsp;&nbsp;
  <img src="assets/clues.png" alt="The full clue list, horizontaal and verticaal" width="250">
</p>

## Install

**Direct APK** — [com.hrbons.wordpuzzle_1.apk](https://github.com/abons/wordpuzzle/releases/download/v1.0/com.hrbons.wordpuzzle_1.apk)
from the [latest release](https://github.com/abons/wordpuzzle/releases/latest), then open it (you may
need to allow "install unknown apps" for your browser).

**Via F-Droid (recommended — updates arrive automatically):** add this repository in the
[F-Droid](https://f-droid.org/) client (*Settings → Repositories → +*):

```
https://abons.github.io/wordguesser/fdroid/repo?fingerprint=C74E4BC48DBE3CCF800A859BC5A9118B23A19BA38C8B33573DBA1BDEB7E456EE
```

Then search for **Word Cross** and install. That repository is shared by all four sibling games — one
URL, one fingerprint — so a new game shows up without adding anything. Each APK is signed by its
**own** app key; Word Cross's certificate is SHA-256
`24:05:A1:0D:35:24:40:37:9A:88:91:82:9F:02:BE:7C:B1:26:D1:55:6C:D7:33:92:93:8B:A9:FE:A2:AD:D8:CA`.

## What it is

- 🧩 **A generated interlocking crossword.** Words cross each other in a freeform grid — numbered,
  cropped to what is actually used, and different every time.
- 📖 **The clues are dictionary definitions.** Every answer is a Dutch word, and its clue is that
  word's own definition with the answer masked out, so a puzzle teaches as much as it tests.
- 📅 **A daily puzzle.** One fixed grid per day, the same for everyone, derived from the date — so
  it is reproducible across launches and comparable with anyone else playing that day.
- 📐 **Three sizes in free play:** klein (±8 words), normaal (±16) and groot (±24). The daily
  ignores the choice on purpose: it has to be the same challenge for everybody.
- ✅ **Controleer and Hint.** Check marks wrong letters red; the hint menu reveals a single letter
  or the whole word — and the statistics count solving without hints separately.
- 📊 **Statistics and streaks:** solved, solved without hints, dailies, current and best day streak.
- 🏞️ **Eight drawn backdrops** — mountains, ocean, forest, desert, city, night, meadow, autumn —
  built entirely from canvas shapes, so there is not a single image file in the APK.
- 🔊 **Usable with a screen reader.** The grid is one hand-drawn canvas, so it is published as a
  virtual view tree: every open cell is its own focusable node that says where it is, what is in it
  and which clues run through it. Walked through with TalkBack by ear, not just checked in a dump.
- ✈️ **Offline after the first start.** The word list is downloaded once and cached; after that the
  app never needs the network again.

## Why so small?

It is written in **pure Kotlin on the Android framework only** — no AppCompat, Compose, Material or
third-party runtime libraries, and the whole UI is built in code. Result: a ~66&nbsp;KB APK that runs
on Android 5.0+.

## Verify the download

`com.hrbons.wordpuzzle_1.apk` — 67,127 bytes, SHA-256:

```
92fa281ba45ba3be1f05d3a0bcd54aba70a0879dc90cbed91c99d2ff11145c84
```

## Privacy

No ads, no analytics, no accounts, no third-party library in the build. The APK asks for INTERNET
and ACCESS_NETWORK_STATE, and they are there for one thing: downloading the Dutch word list and its
definitions on first start. Nothing is uploaded, and your puzzles, statistics and streaks stay on
the device.

## Word data

The answers and their definitions come from the Dutch Wiktionary (CC BY-SA 3.0), with a small number
of gap fills released as CC0. They are prepared into a word list that is hosted alongside the sibling
games; provenance and licences per file are listed in
[SOURCES.md](https://abons.github.io/wordguesser/wordlists/SOURCES.md).

## Support

If you enjoy it, you can [☕ support the developer on Ko-fi](https://ko-fi.com/hrbons).

---

*This repository is the public download for Word Cross: the signed APK, attached to a release per
version. The source is kept in a private repository. Updates are served through the shared hrbons
F-Droid repository linked above.*
