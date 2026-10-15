# Forward Looking Campaigns

An interactive dashboard for tracking upcoming and live campaigns. Open `index.html` in a browser, or enable
GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).

It starts with **no campaigns**; add them with **Add campaign**.

## What it tracks

Name, description, line of business, type (Campaign / Event-in-a-box / Activation Kit, or custom),
New vs. Refresh, segment (Corporate / Enterprise), motion (Net New / Install Base),
status (Planning / In Progress / Live), estimated launch date or target window (Q1–Q4, H1/H2),
fiscal year, language versions, owner, tags and notes.

## Features

- **Year tabs** (2026, 2027, plus any other year a campaign uses). Everything on the page follows the selected tab.
- **Toggles** for every LoB, segment, motion, New/Refresh, type, status and tag, plus search and a launch-date window.
- **Summary tiles**: upcoming (campaigns vs. EiaB), net new, refreshed, live, past target date, next launch.
- **Launch timeline** (Jan–Dec) and **by-LoB** chart, both split by status.
- **Campaign table**: sortable, groupable by LoB, status or quarter, with one-click *Mark live*.

## Where data is saved

Opened as a plain web page, campaigns are saved in the viewer's browser (localStorage). Use
**Data → Export backup** to save a `.json` file and **Data → Import backup** to load it elsewhere.

The same page published as a claude.ai artifact uses the artifact's shared database instead,
so everyone with access sees the same campaigns.
