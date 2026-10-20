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
- **Launch calendar**: one continuous row of quarters across every year (scrolls sideways, opens on the current quarter). Pick a LoB with one click; within a quarter, campaigns with a known month come first. Switch between All, Launched and To come.
- **Launch timeline** by quarter and **by-LoB** chart, both split by status.
- **Campaign table**: sortable, groupable by LoB, status or quarter, with one-click *Mark live* and *Delete* (with Undo).

## Where data is saved

The GitHub Pages site saves campaigns to a shared Firebase Firestore database, so anyone who opens the
site can add, edit, mark live or delete campaigns and everyone sees the change live. No sign-in is needed.

- `firestore.rules` holds the database rules. Paste them into Firebase console → Firestore → Rules → Publish
  whenever they change.
- Only well-formed campaigns are accepted, and nothing is hard-deleted: Delete marks a campaign `deleted: true`,
  so it can be restored from the Firebase console.
- **Data → Export backup** saves a `.json` copy; **Data → Import backup** loads one.

The same page published as a claude.ai artifact uses the artifact's own shared database instead.
