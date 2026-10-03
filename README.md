# Manhwa Tracker

Type an AniList username and browse their manhwa, manga, manhua and novel list, with genre diagrams and reading stats. Static site, no build step.

## Pages
- **Library**: browse the list A-Z or grouped by recently read, year started, rating, status or type. Filter by type, status and genre, and search by title or alternate name.
- **Genres**: genres by type and which genres go together.
- **Stats**: chapters read per day over the last 30 days and the last 12 months.

## Data
- AniList is the only source for the list, progress, statuses, ratings and genres.
- MangaUpdates and MangaBaka are used only to look up alternate names for search.

## Files
| File | Purpose |
|---|---|
| `index.html` | Home and username search |
| `library.html` | Library |
| `genres.html` | Genre diagrams |
| `stats.html` | Reading stats |
| `site.css`, `site.js` | Shared styles and logic |
| `.github/workflows/pages.yml` | Deploys the site to GitHub Pages |

See [REQUIREMENTS.md](REQUIREMENTS.md) for what the site is meant to do.
