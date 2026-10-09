# Eren — personal bio website

A one-page personal site: cover, about, a song that plays by itself and keeps
looping, a short story in हिन्दी and English, and a Telegram contact.

## The files

| File | What it is |
| --- | --- |
| `index.html` | The whole page — all the words and sections live here |
| `styles.css` | All the colours, fonts, spacing and animations |
| `main.js` | Song auto-play/loop/seek, story language switch, share button |
| `assets/coast.jpg` | The black-and-white cover photo |
| `assets/eren-song.mp3` | The song ("Shuruat Dobara", 1:27) |
| `favicon.ico` | The little tab icon |
| `robots.txt` | Tells search engines the page is open to them |

Plain HTML, CSS and JavaScript. No Node.js, no build, no framework — open
`index.html` in a browser and it works.

## Edit something

- Change the words → `index.html`
- Change a colour → `styles.css`, look at the `:root` block at the top
  (`--background` is the page colour, `--primary` is the amber accent)
- Change the song → replace `assets/eren-song.mp3` with another file of the
  same name

## Host it yourself

Upload these files to any host that serves static files and you are done.
There is no server code, so nothing needs installing.

**Netlify** — drag this folder onto <https://app.netlify.com/drop>.
**Vercel** — `vercel` in this folder, or import the GitHub repo below.
**GitHub Pages** — repo → Settings → Pages → deploy from `main` / root.
**cPanel / shared hosting** — upload the contents of this folder into
`public_html`.

## Put it on GitHub

GitHub does **not** unpack a `.zip` — it stores it as one binary file, which is
why a zipped upload shows no code. Extract the zip first, then upload the
**folder's contents**:

1. Create an empty repository on GitHub.
2. On the repository page click **Add file → Upload files**.
3. Drag `index.html`, `styles.css`, `main.js`, `README.md`, `favicon.ico`,
   `robots.txt` and the `assets` folder in (not the zip).
4. Commit. The code is now readable in the repo, and Pages can serve it.

Or, with git on your own machine:

```sh
cd eren-website
git init
git add .
git commit -m "Eren bio site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

## Notes

- The song starts by itself. Some browsers block sound until the visitor taps
  once — the site then starts the song quietly and unmutes on that first tap.
- The song loops, so it keeps playing the whole time someone stays on the page.
- Fonts (Manrope, Space Grotesk, Tiro Devanagari Hindi) load from Google Fonts.
