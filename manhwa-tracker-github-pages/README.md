# Manhwa Tracker

Type an AniList username and browse their manhwa, manga, manhua and novel list, with genre diagrams and reading stats. Static site, no build step.

See [REQUIREMENTS.md](REQUIREMENTS.md) for what the site does.

## Put it on GitHub Pages

1. **Create the repo.** On GitHub, create a new empty repository (for example `manhwa-tracker`). It can be public. Don't add a README there.
2. **Upload these files.** Unzip this package, then in that folder run:
   ```
   git init -b main
   git add -A
   git commit -m "Manhwa tracker"
   git remote add origin https://github.com/<your-username>/<repo>.git
   git push -u origin main
   ```
   (Uploading through the website works too, but its drag-and-drop skips hidden folders. Make sure `.github/workflows/pages.yml` ends up in the repo.)
3. **Turn on Pages.** In the repo go to **Settings → Pages** and set **Source** to **GitHub Actions**. You only do this once.
4. **Wait for the deploy.** Open the **Actions** tab; the "Deploy to GitHub Pages" run takes about a minute. If it didn't start, open it and press **Run workflow**.
5. **Open the site** at `https://<your-username>.github.io/<repo>/`.

Every later `git push` to `main` redeploys automatically.

### No Actions? Use the branch instead
Settings → Pages → Source: **Deploy from a branch**, branch `main`, folder `/ (root)`. The included `.nojekyll` file makes this work.

## Files
| File | Purpose |
|---|---|
| `index.html` | Home and username search |
| `library.html` | Library with filters, search, grouping, pagination |
| `genres.html` | Genre diagrams |
| `stats.html` | Reading stats |
| `site.css`, `site.js` | Shared styles and logic |
| `.github/workflows/pages.yml` | Deploys the site |

## Notes
- Your recent searches, nicknames and cached data live in your browser per web address, so they start fresh on a new URL.
- Alternate names come from MangaUpdates and MangaBaka. If a browser blocks those requests, the page shows a note and search uses only the names AniList has.
- Local preview: `python3 -m http.server` in this folder, then open `http://localhost:8000`.
