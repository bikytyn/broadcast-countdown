# Broadcast Countdown

A single-file countdown / count-up timer for live video production. Open `countdown.html` in a browser: the timer fills the top of the page so you can crop it into your video composite (OBS, vMix, a hardware switcher's capture input, …), and the controls sit below it.

No install, no build step, no dependencies, no server.

## Quick start

1. Download or clone this repo.
2. Open `countdown.html` in Chrome, Edge or another modern browser.
3. Set the time, press **Start** (or hit <kbd>S</kbd>).
4. Capture the top **display area** of the page and crop it in your switcher, or press **Open fullscreen tab** to get a clean, controls-free window to capture.

## Features

**Timer**
- Countdown or count-up (stopwatch) mode
- Start time in hours / minutes / seconds
- Quick adjust while running: −1m, −10s, +10s, +1m
- Start, Pause and Reset, with a live status indicator

**Look**
- Background colour, text colour, font and size
- Fractions of a second: off, tenths (0.1) or hundredths (0.01)
- Green-screen background option, if you prefer keying over cropping
- Fonts: a short built-in list, any font installed on the computer (see below), or type any font name

**Label**
- Optional text shown above or below the time
- Its own size, font and spacing to the time, independent of the timer text

**Blink warning**
- Optionally blinks the display when the countdown gets close to zero
- Configurable threshold (seconds remaining), blink colour and blink speed

**Saved times**
- Press **Save current time** (with an optional label) to log the current value together with the wall-clock time, for example when a team finishes
- Delete single rows, clear the log, or **Export CSV**

**Fullscreen tab**
- **Open fullscreen tab** opens a second window showing only the timer, while the controls stay in the original tab
- The fullscreen tab keeps its own clock, so it keeps running accurately even when the control tab is in the background

## Keyboard shortcuts

| Key | Action |
| --- | ------ |
| <kbd>S</kbd> | Start |
| <kbd>P</kbd> | Pause |
| <kbd>R</kbd> | Reset |

They work in the control tab and in the fullscreen tab, and are ignored while you are typing in a text box, number field or dropdown.

## Notes and limitations

- **Installed fonts:** the **Load installed fonts** button uses the browser's Local Font Access API, which is available in Chromium-based browsers only (Chrome, Edge, Brave, Opera) and asks for permission once. In other browsers, type the font name into the "Or type any font name" field instead. The font has to be installed on the computer that runs the page.
- **Fullscreen tab:** it receives its settings from the control tab, so keep the control tab open. If you reload the control tab, close and reopen the fullscreen tab. Your browser may ask you to allow pop-ups the first time.
- **Saved times** live in the page's memory and are lost when the tab is closed or reloaded. Use **Export CSV** to keep them.
- **Size of the display area:** the display box keeps a fixed size. If you make the text larger than the box, the overflow is clipped rather than the box growing.
- Developed and tested in Chromium. Everything is plain HTML, CSS and JavaScript, but other browsers have not been tested.

## Project layout

```
countdown.html   the whole app: markup, styles and script in one file
README.md        this file
```

## Changelog

See the commit history for individual updates.
