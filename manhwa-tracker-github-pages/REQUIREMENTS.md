# Website requirements

What this site must do. Use this as the checklist when changing it.

## Data
- Look up any AniList username and show that user's manga-type list: manhwa, manga, manhua and novels.
- AniList is the only source for tracking (list, progress, status, covers, genres, ratings).
- Only show titles with one of five statuses: Reading, Completed, On hold, Plan to read, Dropped.
- Ratings mean AniList's average score, never the user's own score.
- Changes on AniList appear without reloading (live refresh, with a Pause button).
- MangaUpdates and MangaBaka are used only to find alternate names, for titles with no English name on AniList. They are never used for tracking.
- No MangaDex.

## Pages
- **Home**: username search, recent searches. No placeholder example name.
- **Library**: A-Z by default; "Organize by" dropdown (Title A-Z, Recently read, Year started, Rating, Status, Type); filters for type, status and genres (multi-select, all must match); title search that also matches alternate names and your own nicknames; pagination with per page 24 / 48 / 96 (default 24). No reverse-order button.
- **Genres**: genres by type (bar diagram), genres that go together (heatmap and pairings list), status filter, table alternative.
- **Stats**: chapters per day for the last 30 days (line chart), last 12 months (daily heatmap), summary tiles, most-read titles. Counts come from the AniList activity feed.

## Look
- Dark gothic violet manhwa style. Works on phones with no sideways page scrolling.
- Charts: accessible colors, tooltips, keyboard focus and a table alternative.

## Technical
- Static files only (no build step, no server). All links are relative.
- Files: `index.html`, `library.html`, `genres.html`, `stats.html`, `site.css`, `site.js`.
