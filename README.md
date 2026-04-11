# Yale AI Workshop 2026

Workshop site for **Toward AI with Human-Level Efficiency**, April 29–30, 2026.

Live at: https://cncLgithub.github.io/yale-ai-workshop-2026

---

## How to update the site

You only ever need to edit two files. You do not need to know any web development.

---

### Adding talk recordings (most common update)

Open `data/talks.js` in any text editor.

For each talk, find the speaker's entry and fill in the `youtubeId` field:

```
1. Upload the recording to YouTube
2. Copy the video ID from the URL
   e.g. youtube.com/watch?v=dQw4w9WgXcQ  →  the ID is dQw4w9WgXcQ
3. Paste it in:
```

```js
{
  tag:          "learning",
  speaker:      "Tom Griffiths",
  organization: "Princeton University",
  date:         "Apr 29",
  time:         "9:10",
  title:        "My Talk Title Here",     ← add the talk title
  description:  "A short abstract...",    ← optional
  youtubeId:    "dQw4w9WgXcQ"            ← paste the YouTube ID here
},
```

Save the file, commit, and push. The site updates automatically.

---

### Updating site-level info (title, dates, RSVP, organizers)

Open `data/config.js`. All the top-level workshop info is there — dates, location, RSVP link, organizers list, sponsors. Edit in plain text, save, commit, push.

To **hide the RSVP banner** once the deadline has passed, change:
```js
showRsvpBanner: true
```
to:
```js
showRsvpBanner: false
```

---

## Publishing changes

After editing a file:

```bash
git add .
git commit -m "add recordings" 
git push
```

The site updates within ~60 seconds.

---

## File structure

```
yale-ai-workshop-2026/
├── index.html        ← page layout and styles (don't edit)
├── data/
│   ├── talks.js      ← talk cards: speakers, YouTube IDs, titles, descriptions
│   └── config.js     ← workshop metadata: dates, RSVP link, organizers
└── README.md         ← this file
```
