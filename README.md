# StoryShelf Tracker

A fast, read-only viewer for your **AniList** manga, manhwa and manhua list. Type any AniList username and get a searchable library, genre diagrams and reading stats. It is a static site: plain HTML, CSS and JavaScript, no build step, no backend, no accounts.

**Live site:** https://amongbuss91-alt.github.io/Manhwa-Tracker/

## Features

### Home
- Username lookup with a wood-table design and a list of recent searches.
- Remembers the last user you looked up.

### Profile header
- Shows the user's AniList banner, avatar and name on every page. The name links to their AniList profile.
- The top bar is transparent over the banner and turns solid when you scroll or hover.

### Library
- A to Z by default, with an **Organize by** menu: Title A to Z, Recently read, Recently added, Year started, Rating (AniList average) and Type.
- Filters: type (manhwa, manga, manhua, novel), the five AniList statuses, and genres (a title must match all selected genres).
- Search by title or **alternate name**, so a title you know by another name still turns up.
- Pagination with 24, 48 or 96 titles per page.
- **Adult** and **Suggestive** labels. Suggestive cards are tinted with a label under the progress bar.
- Tag filtering by opening a tag from the Stats page.
- Refreshes itself about every 30 seconds while the tab is open.

### Genres
- Genres broken down by type.
- A pairing heatmap showing which genres show up together.

### Stats
- Reading activity tiles: today, this week, this month and current streak.
- A last 30 days line chart and a last 12 months heatmap of chapters read.
- Tags broken down by type, with long tag names shortened. Select a bar to open those titles in the Library.

## Data sources
- **AniList** is the only source for the list, progress, statuses, scores, genres and tags.
- **MangaUpdates** and **MangaBaka** are used only to look up alternate titles for search. They never affect tracking.

## How it works
- Everything runs in the browser and talks directly to the public AniList GraphQL API (`https://graphql.anilist.co`). Only public lists can be viewed.
- The user is selected with a `?user=` URL parameter.
- Browser storage used:

| Key | Storage | Purpose |
|---|---|---|
| `lastUser`, `recentUsers` | localStorage | Last and recent searches |
| `altNames.v2` | localStorage | Cached alternate titles |
| `act.v1:<name>` | localStorage | Cached activity for the Stats page |
| `list:<name>` | sessionStorage | Cached list for the current session |

Nothing is sent anywhere except the AniList, MangaUpdates and MangaBaka requests above.