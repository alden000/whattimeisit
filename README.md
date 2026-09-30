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
- **Screen care, built for old LCDs left on all day.** Every option below is in Settings:
  - *Wander:* every 12 minutes the clock glides (over 10 s) to a new spot and a slightly different size. Even the centres of the thick digits land on fresh pixels, which small drifts alone can't do.
  - *Pixel orbit:* the whole screen also drifts in a slow ±16px loop, one pixel at a time.
  - *Soft contrast:* the digits are slightly dimmer and thinner, so the same pixels hold less brightness.
  - *Pixel refresh* (every 30 min, 1 h or 2 h, or on demand): a 45-second colour cycle. It shows a negative of the screen, then white, red, green and blue, then a spinning spectrum. A wipe opens it, and a small caption with the time floats across it. Any click or key skips it. It never starts right before an alarm.
  - *After hours:* between two times you choose (default 22:00–07:00), either **Dim** the screen or **Sleep** it. Sleep turns the screen fully black and releases "keep awake" so the OS can power the display off. Move the mouse to peek for a minute. Alarms still ring.
- **Time zone** comes from your system automatically. If you change it (for example, when travelling), the clock picks it up within a minute without a reload.
- **Settings.** 12/24-hour time, show or hide seconds, dark/light/system theme, keep the screen awake, and a custom place name.

Keys: `F` fullscreen (or double-click the time) · `A` alarms · `S` settings · `Esc` close · when ringing: `Enter` dismiss, `Z` snooze.

## Hide the browser UI (so it can't burn in either)
The page can't paint over the browser's own tabs, address bar or title bar, so run it as an app instead:

1. Open the live page in Chrome or Edge, then click **Install** in Settings → Display, or the install icon in the address bar.
2. The clock opens in its own window, with no tabs or address bar.
3. Click the **⌃** arrow in that window's title bar. The title bar is hidden and the clock draws edge to edge. Only the small minimize/maximize/close buttons remain, and you can still drag the window by its top edge.

The title bar colour (while it's visible) follows the time of day. It goes black in Sleep mode and cycles colours during Pixel refresh. The window title shows the current time, so even that text changes every minute. The installed app also works offline.

Outside the browser, set your OS taskbar to auto-hide, or keep it on the main monitor only.

## Light on your GPU
- Only a thin strip around the water's surface is redrawn. The water below it and the background are static and painted once.
- The water and the seconds line redraw at a fixed rate that you choose in **Settings → Display → Motion**: *Eco* (8 fps), *Balanced* (20 fps, the default) or *Smooth* (60 fps). Everything else only changes when the time does.
- Overlays that aren't showing (alarm screen, settings panel, pixel refresh, dimmer) are fully removed from rendering, not just made transparent.
- To keep the clock off a dedicated GPU on Windows, run it in a browser you don't otherwise use (for example Edge), then go to **Settings → System → Display → Graphics**, add that browser and choose **Power saving**. This needs your CPU's integrated graphics to be enabled. Alternatively, turn off **Use graphics acceleration when available** in that browser's settings; the clock is light enough to run without it.

## Notes
- Browsers block sound until you interact with the page. After loading, click anywhere once. A small "Click to arm alarm sound" hint appears when this is needed.
- Allow notifications when asked so alarms still reach you when the window is behind others.
- Keep the tab open. Alarms, reminders and settings are saved in your browser (localStorage).
