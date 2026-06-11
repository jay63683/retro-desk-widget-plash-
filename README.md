# Desk

A paper-and-pixels desktop dashboard for macOS: **calendar · events · goals · tasks · diary**, plus a card for your own art. Cross-stitch logo, serif body, dot-matrix display, terminal footer. One self-contained HTML file — no build, no accounts, no server, no tracking.

<!-- screenshots: add light/dark side-by-side here -->

## Features

A bento home grid with a clickable month calendar (click any day to add an event with one-tap time chips), a next-event countdown, a red dot-matrix "up next" display, a live analog clock, mini views of tasks and goals, and quick actions. Sub-pages manage tasks (type to add, click to complete), goals with ASCII progress bars, events with native date/time pickers, and a lined-paper diary with one page per day. Clicking a calendar day opens a composer for both that day's tasks and events. The art card shows any image you drop in — it auto-inverts to match light or dark mode based on the image's polarity. Optional alerts ping you 10 minutes before each event. Keyboard shortcuts: `h t g e a n` to navigate, `d` for dark mode.

All data lives in your browser's localStorage. Nothing leaves your machine. The only network request is Google Fonts.

## Install — pick one

### 1. Plash (true desktop widget, recommended)

[Plash](https://apps.apple.com/app/plash/id1494023538) (free) pins a web page to your desktop, under all windows.

1. Clone or download this repo; keep the folder somewhere permanent.
2. Plash menu-bar icon → **Add Website…** → **Local Website…** → select the repo folder (it loads `index.html`).
3. The card sits at the right edge with your wallpaper around it. Toggle Plash's **Browsing Mode** to interact, off to send it back to the desktop.

Position it by adding a hash to the URL in Plash: `#left`, `#right`, `#center`, with `-top` variants (e.g. `#center-top`). Note: Plash's WebView cannot show native macOS notifications — use the app below if you want alert banners.

### 2. Desk Zone.app (interactive window + notifications)

In `app/`. Move `Desk Zone.app` anywhere, right-click → Open the first time (unsigned). It opens `widget.html` as a chromeless Chrome/Edge/Brave app window. If developer tools (python3) are present it serves over localhost, which enables real macOS notification banners; otherwise you get in-window toasts.

### 3. Übersicht (display only)

In `ubersicht/`. Drop `desk-zone.widget` into Übersicht's widgets folder. macOS desktop widgets never receive keyboard focus, so treat this one as glanceable decor.

Or just open `widget.html` in any browser.

## Files

`widget.html` is the full app (open it anywhere). `index.html` is the same file defaulting to widget mode: transparent around the card, pinned right — what Plash loads.

## Privacy & security notes

No analytics, no external JS, no cookies. User content is HTML-escaped before rendering. The optional localhost server in the app launcher binds to 127.0.0.1 and serves only the app's own resources directory. Fonts (Jacquard 12, VT323, Doto) load from Google Fonts; vendor them locally if you'd rather make zero network requests.

## License

MIT — see [LICENSE](LICENSE). Fonts are under the SIL Open Font License via Google Fonts.
