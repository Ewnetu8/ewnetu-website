# Personal Website — Ewnetu Abebe Kassie

A simple, dependency-free static site: plain HTML + CSS, no build step.

## Files
- `index.html` — Home
- `cv.html` — CV (now populated from your uploaded CV PDF)
- `research.html` — Research (publications, interests, theses)
- `teaching.html` — Teaching (positions, training & mentoring)
- `styles.css` — shared styling for all pages
- `assets/Ewnetu_Abebe_CV.pdf` — your CV, linked as a download on the CV page

## What was left out on purpose
Your CV PDF also includes your phone number, date of birth, and gender, and
phone numbers for your three references. I left those off the public website
pages as a privacy precaution — search-engine-indexed personal contact
details are hard to take back once published. If you want any of them
included, just add the line back into the relevant HTML file.

## Before you deploy
1. Put your photo in `assets/ewnetu_p.jpg` (or update the `<img src>` paths in each HTML file).
2. Double check the employment dates and publication details render the way you want.

## Editing in VS Code
1. Open this folder in VS Code: `code .`
2. Install the **Live Server** extension (optional) to preview with auto-reload — right-click `index.html` → "Open with Live Server".
3. Edit any `.html` file's text directly; shared look-and-feel lives in `styles.css`.

## Deploying to Netlify
**Option A — drag and drop (fastest):**
Go to https://app.netlify.com/drop and drag this whole folder in.

**Option B — connect a Git repo (recommended for ongoing edits):**
1. Create a new GitHub repo and push this folder to it:
   ```
   git init
   git add .
   git commit -m "Update site with real CV content"
   git branch -M main
   git remote add origin <your-repo-url>
   git push -u origin main
   ```
2. In Netlify: **Add new site → Import an existing project** → pick the repo.
3. Build command: leave blank. Publish directory: `/` (root).
4. Every future `git push` will auto-redeploy the site.
