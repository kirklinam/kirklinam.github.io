# Editing this site

Your site is one file — `index.html` — plus an `assets/` folder of images and
fonts. Most changes never touch the code: you edit a Google Doc or drop a file
in Drive and the site updates itself. Here is everything, shortest first.

---

## 1. The weekly "This Week" board — edit from your phone

1. Make a Google Doc (call it **This Week**).
2. Share it: **Share → General access → Anyone with the link → Viewer**.
3. Copy the link. It looks like
   `https://docs.google.com/document/d/`**`1AbC…XyZ`**`/edit` — the **bold middle
   part is the ID**.
4. Open `index.html`, find the `LINKS` block at the very top, and paste the ID:
   `thisWeek: "1AbC…XyZ",`
5. Save, commit, done — **once**. From then on you just edit the Doc; the site
   shows the latest version live. No code, no upload.

## 2. Post the syllabus, Family Guide, or an answer key

Same idea, with a Drive **file** instead of a Doc:

1. Upload the PDF to Google Drive.
2. Share it **Anyone with the link → Viewer**.
3. Copy the link: `https://drive.google.com/file/d/`**`1AbC…XyZ`**`/view` — the
   bold part is the ID.
4. Paste it into the matching line in `LINKS`:
   - `syllabus:` — Syllabus 26–27 (shows on the Home page)
   - `familyGuide:` — Family Guide 26–27 (Family page)
   - `key1A:` / `key1B:` — the Topic 1A / 1B worked keys (Answers page)
5. **To update later, re-upload to the *same* Drive file** (right-click →
   Manage versions, or keep the same file). The site updates itself — you never
   touch the code again.

Empty lines just show a friendly "posts here" placeholder — never an error.

## 3. Add the Google Classroom link

In `LINKS`, set `classroom:` to the full Classroom URL (the whole
`https://classroom.google.com/…` address). It wires every "Open Google
Classroom" button and the replacement-guides folder (`guidesFolder:`).

## 4. Swap a picture (unit cover, headshot, hero photo)

Replace the file in `assets/img/` with a new one **of the same name** — e.g.
drop a new `unit-3.jpg` over the old one. Nothing else to change.
Names: `home-hero.jpg`, `family.jpg`, `quarter-1-cover.jpg`, `headshot.jpg`,
`unit-1.jpg` … `unit-8.jpg`.

## 5. Change wording, dates, a module row, a Khan link

That lives in `index.html`. Search the file for the text you want to change and
edit it in place. The module rows on the Quarter 1 page are plain blocks of
`Artifact / date / links` — copy an existing one to add another.

---

## Publishing a change (the no-copy-paste part)

This folder is a git repo connected to GitHub. GitHub Pages rebuilds every time
you push. From this folder:

```
git add -A
git commit -m "what changed"
git push
```

Your live site updates in under a minute. That's the whole loop — no zip files,
no re-pasting into the browser. (Ask Claude to run these three lines and it will
push for you.)
