# the.roadmap

A personal learning roadmap tracker for **UofL Speed School PD Modules Summer 2026**.

Single-file static site (HTML + CSS + JS, no build step, no dependencies) that helps me track progress toward the 100-hour upskilling requirement, with a curated catalog of full-stack web development courses pulled from LinkedIn Learning, freeCodeCamp, IBM, AWS, and more.

**Live site:** https://veriteigiraneza.github.io/PD-Module-Road-Map/ *(update this URL once Pages is enabled)*

---

## What it does

- **Dashboard** — days remaining until July 10 deadline, total hours logged vs. 100, technical hours vs. 25-hour minimum, professional hours vs. 25-hour minimum, weekly pace needed
- **My Path** — a personal roadmap prefilled with ~100 hours of recommended courses for a full-stack focus
- **Browse Catalog** — full library of ~50 curated courses; filter by category, type, free-only, or recommended-only
- **Completed** — checked-off course history
- **Custom courses** — add anything not in the catalog (YouTube playlists, books, tutorials)
- **Export** — generates a `.txt` progress report for Blackboard upload proof
- **Dark / light mode** — toggle in header, persists across sessions
- **Progress saving** — all state stored in browser `localStorage`, no account or backend needed

---

## How to use it

1. Open the site in your browser (mobile or desktop)
2. Review the prefilled courses in **My Path** — remove anything you don't want with the `−` button
3. Visit **Browse Catalog** to add other courses to your path
4. As you finish each course, click its checkbox to mark it complete
5. Watch the dashboard fill up as you log hours

Progress saves automatically. Clearing browser data wipes it — use the **Export** button periodically to back up.

---

## Deploy to GitHub Pages

1. Fork or clone this repo
2. Push to your own GitHub repo
3. Go to **Settings → Pages**
4. Set Source to `main` branch, root folder, save
5. Wait ~1 minute, then open `https://<your-username>.github.io/<repo-name>/`

That's it. No build step, no CI, no config.

---

## Customize the course catalog

All courses live in a single `COURSES` array inside `index.html`. Each entry looks like:

```javascript
{
  id: 'unique-id',
  title: 'Course Name',
  vendor: 'Provider',
  category: 'Web Dev',
  type: 'technical',       // or 'professional'
  hours: 5,
  free: true,
  recommended: true,        // shows in starter path
  desc: 'Short description.',
  url: 'https://...'
}
```

Edit, add, or remove courses freely — just keep the `id` unique.

---

## Tech stack

- Vanilla HTML, CSS, JavaScript (no frameworks)
- Google Fonts: Fraunces (display), DM Sans (body), JetBrains Mono (numbers)
- `localStorage` for persistence
- Hosted free on GitHub Pages

No dependencies. No build. One file.

---

## Background

The **PD Modules** program at UofL Speed School lets engineering students complete 100 hours of self-directed upskilling in lieu of a co-op rotation. Minimum 25 technical + 25 professional hours, deadline July 10, 2026.

This site is my personal execution tool for that requirement — a focused, mobile-friendly alternative to maintaining a spreadsheet.

---

## License

Personal project. Feel free to fork and adapt for your own learning track.