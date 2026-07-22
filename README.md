# The Infinite Rugby League Stadium

A self-contained browser app that simulates an endless single-elimination tournament across every rugby league team from every era, competition, and country. The 1908 South Sydney Rabbitohs can face the 2023 Penrith Panthers. The 1995 Wigan Warriors can meet the 1960 St George Dragons. Every match is commentated via speech synthesis. Every result is remembered forever.

## What it does

- **615 teams** drawn from over 90 clubs across NRL, Super League, QRL, international sides, and defunct competitions, each appearing at multiple points in their history
- **Single-elimination knockout** with a full bracket tree, running continuously until a champion is crowned, then resetting and starting again
- **Live commentary** via the Web Speech API with play-by-play of tries, conversions, penalties, field goals, and golden point
- **Permanent records layer** tracking champions, franchise win rates, all-time leading scorers, biggest cross-era upsets, and dynasty streaks across every tournament ever played on your machine
- **"While you were away" digest** so leaving it running overnight is productive, not wasteful
- **History export/import** so your records survive a browser wipe

## How to use it

Open `index.html` in any modern browser. That's it. No server, no install, no build step, no dependencies.

Pick a speed from the dropdown (×600 is a good starting point), toggle audio on if you want commentary, and leave it running. Check the Records page after a few tournaments to see what's accumulating.

Everything is saved to your browser's local storage automatically. Refresh the page and it picks up where it left off.

## Live site

Hosted on Vercel: [infinite-rugby-league.vercel.app](https://infinite-rugby-league.vercel.app)

## Technical constraints (by design)

- **Single file.** The entire app, every team, every roster, every logo, every line of CSS and JavaScript, lives inside one HTML file. This is the point, not a limitation.
- **No backend.** All state lives in localStorage.
- **No external APIs.** No network requests of any kind.
- **No build step.** Download the file, open it, done.

## Credits

Built with Claude. Fonts: IBM Plex Mono, Bebas Neue, Share Tech Mono (loaded from Google Fonts, the only external resource).
