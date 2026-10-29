# Moulshree × Search Atlas: application page

A single-page pitch for Search Atlas's **Product Engineer (PM)** role.

It has three parts:
1. **Intro and why hire me:** who I am, my impact numbers and four reasons I fit the role.
2. **Search Atlas breakdown:** what the product does, who it's for, customer pain points, nine feature tabs with small flowcharts, and where I think the friction is.
3. **30/60/90 day plan.**

A sticky "On this page" box on the right (desktop only) links to each section. The top bar links to my resume, LinkedIn and portfolio.

## Files
- `index.html`: the whole site. Inline CSS and JS, no build step, no dependencies.
- `README.md`: this file.

The only external request is the Google Fonts stylesheet for the serif font (Source Serif 4). If it fails to load, the page falls back to Georgia.

## Run locally
Open `index.html` in a browser, or run `python3 -m http.server 8000` in this folder and visit http://localhost:8000.

## Deploy to Vercel

**Option A: CLI**
1. Put `index.html` in its own folder, e.g. `searchatlas-pitch`.
2. In that folder, run `npx vercel login` and sign in.
3. Run `npx vercel` and answer the prompts:
   - Set up and deploy: Yes
   - Link to existing project: No
   - Project name: e.g. `moulshree-searchatlas`
   - Code directory: `./`
   - Build settings: accept the defaults.
4. Run `npx vercel --prod` to get the public URL.

**Option B: GitHub import**
1. Push `index.html` to a new GitHub repo.
2. At vercel.com/new, import the repo.
3. Framework Preset: **Other**. Build Command: empty. Output Directory: `.`
4. Click **Deploy**.

Optional: under Project → Settings → Domains, add a shorter address such as `moulshree-searchatlas.vercel.app`.

## After deploying, check
- The serif font shows on the "Along with applying…" line.
- The "On this page" box stays in view while scrolling on desktop.
- Resume, LinkedIn and Portfolio links in the top bar open.
- The page looks right on a phone (the sticky box is hidden there).

## Before sending
- **Numbers:** the impact boxes show 30x ARR ($10K → $300K), ~74% activation lift, 10+ zero-to-one launches and 1,000+ clients. Make sure they match your resume and portfolio, which have shown different figures (e.g. 7x, $30K → $200K, 4 launches).
- **Claims:** the first "fit" card mentions Django/React, SQL, REST APIs and Claude Code. Keep only what you're comfortable defending in an interview.
- **Product facts:** everything about Search Atlas comes from public pages, help docs and reviews. Items tagged "vendor claim" are their marketing. Pricing may have changed.
- **Availability:** the job post asks for EST availability. The page doesn't mention it. Add a line if it applies.
- **Disclaimer:** the footer says this page isn't affiliated with Search Atlas. Keep it.

## Secrets
There are none. The page has no API keys, env vars or private URLs, so it's safe to put in a public repo.

## Editing
Colors are CSS variables at the top of `index.html` (`--bg`, `--lav`, `--mint`, `--warn`). The impact boxes, fit cards, feature tabs and plan phases are plain HTML blocks, so you can edit the text in place.
