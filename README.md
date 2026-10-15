# Forward Looking Campaigns

An interactive dashboard for tracking upcoming and live campaigns. Open `index.html` in a browser, or enable
GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).

It starts with **no campaigns**; add them with **Add campaign**.

## What it tracks

Name, description, line of business, type (Campaign / Campaign in a Box), New vs. Refresh,
segment (Corporate / Enterprise), motion (Net New / Install Base), status (Planning / In Progress / Live),
estimated launch month or quarter (this also sets the year tab), language versions, owner and notes.

## Features

- **Year tabs** (2026, 2027, plus any other year a campaign uses). Everything on the page follows the selected tab.
- **Toggles** for every LoB, segment, motion, New/Refresh, type and status, plus search and a launch window (this month, this quarter, next quarter, past target).
- **Summary tiles**: upcoming (campaigns vs. campaigns in a box), net new, refreshed, live, past target, next launch.
- **Exec summary** view that recreates the exec deck's summary slide (launched / net new / refreshed, then upcoming) from the live data.
- **Launch timeline** by quarter and **by-LoB** chart, both split by status.
- **Campaign table**: sortable, groupable by LoB, status or quarter, with one-click *Mark live* and *Delete* (with Undo).

## Where data is saved

Opened as a plain web page, campaigns are saved in the viewer's browser (localStorage). Use
**Data → Export backup** to save a `.json` file and **Data → Import backup** to load it elsewhere.

The same page published as a claude.ai artifact uses the artifact's shared database instead,
so everyone with access sees the same campaigns.
