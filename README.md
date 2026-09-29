# What Time Is It

A single-file, minimalist clock for a secondary monitor — designed for a tall, narrow window (about ⅓ of the screen, portrait), and it also adapts to wide windows.

**Live:** https://alden000.github.io/whattimeisit/ — or open `index.html` in your browser. There's nothing to install or build.

## What you get
- **Big stacked time.** Hours sit above minutes so you can read it from across the desk. Each digit blurs up into place when it changes.
- **The day as a tide.** A slow wave rises from the bottom at midnight to the top at the next midnight. The ruler on the left marks 06 / 12 / 18.
- **Colour that follows the sun.** The minutes and the tide change colour through the day: indigo at night, coral at dawn, gold in the morning, mint at midday, amber and rose at dusk.
- **Seconds rail.** A thin line down the right edge fills once a minute.
- **Alarms.** Set a time, a label, the days to repeat (or leave them blank for a one-off), and a sound (Glass, Marimba or Pulse). Click an alarm to edit it.
- **Quick reminders.** One tap for 5 min, 15 min, 30 min or 1 hour.
- **Chime.** An optional soft bell every 15 min, 30 min or hour, with a glow around the screen edge.
- **When an alarm rings** you get a full-screen alert with a looping sound, a browser notification and a flashing tab title. You can snooze for 5 minutes or dismiss it.
- **Quiet UI.** The buttons and cursor fade out after a few seconds without mouse movement.
- **Screen care (safe to leave on all day).** Each of these can be switched off in Settings:
  - *Pixel orbit:* the whole layout drifts in a slow loop of about ±16px (7- and 11-minute cycles), one pixel at a time, so nothing stays on the same pixels.
  - *Hourly pixel refresh:* at the top of each hour, an inverting band sweeps across the screen to clear image retention. You can also run it any time from Settings.
  - *Dim at night:* brightness fades down between 22:00 and 07:00.
  - Colours are off-white and softly tinted, never pure white on black. The minutes and the tide change colour through the day.
- **Settings.** 12/24-hour time, show or hide seconds, dark/light/system theme, keep the screen awake, and a custom place name.

Keys: `F` fullscreen (or double-click the time) · `A` alarms · `S` settings · `Esc` close · when ringing: `Enter` dismiss, `Z` snooze.

## Notes
- Browsers block sound until you interact with the page. After loading, click anywhere once. A small "Click to arm alarm sound" hint appears when this is needed.
- Allow notifications when asked so alarms still reach you when the window is behind others.
- Keep the tab open. Alarms, reminders and settings are saved in your browser (localStorage).
- To run it without browser chrome, open it as an app window, e.g. `chrome --app=file:///path/to/index.html`, or enable GitHub Pages on this repo and use "Install app" / "Create shortcut".
