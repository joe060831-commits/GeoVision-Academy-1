# GeoVision Academy — Website

A static, framework-free site (HTML/CSS/JS) implementing the GeoVision Academy brief: Home, Courses, Certificate Verification, and About pages.

## Project structure
```
geovision-academy/
├── index.html        Home
├── courses.html       Courses (all 5 programs, filterable)
├── verify.html         Certificate verification (try ID: GVA-GIS-0001)
├── about.html           Mission, vision, founder story, roadmap
├── vercel.json
└── assets/
    ├── css/style.css
    ├── js/main.js
    └── img/logo.svg
```

## Deploying to your Vercel account

I don't have direct access to your Vercel account, so deployment needs one quick step on your end. Two options, pick whichever is easier:

### Option A — Vercel CLI (fastest, ~2 minutes)
1. Download this project folder.
2. Open a terminal in the folder and run:
   ```
   npm i -g vercel
   vercel login
   vercel --prod
   ```
3. Accept the defaults when prompted (no framework / static site). Your live URL will be printed at the end.

### Option B — Vercel Dashboard
1. Go to [vercel.com/new](https://vercel.com/new).
2. Either drag-and-drop this folder directly, or push it to a GitHub repo first and import that repo.
3. Leave the framework preset as "Other" — no build command is needed since this is a static site.
4. Click **Deploy**.

Either way, every future change just needs `vercel --prod` again (CLI) or a new push to the connected GitHub repo (dashboard).

## Before going live — things to wire up
- **Waitlist form**: currently shows a front-end success message only. Connect it to an email service or a small serverless function (e.g. a Vercel Function that writes to a database or sends to Resend/Mailchimp) to actually capture signups.
- **Certificate verification**: currently checks against one sample record (`GVA-GIS-0001`) in `assets/js/main.js`. Replace the `SAMPLE_RECORDS` object with a real lookup (API call or database) once you're issuing real certificates.
- **Testimonials**: the three quotes on the home page are placeholders labeled "Beta cohort, 2026" — swap in real learner feedback once available.
- **Social links**: footer social icons currently point to `#` — update with real profile URLs.
- **Contact email**: replace `hello@geovisionacademy.com` with your real inbox address everywhere it appears.
