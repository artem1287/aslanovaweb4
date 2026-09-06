# Editing Your Website with Google Sheets — Setup Guide

This replaces the earlier Builder.io plan (its content-editing tier required a paid subscription). This approach is completely free, and the "editor" is just a spreadsheet — something you likely already know how to use.

## The Big Picture

- **The design** (colors, layout, fonts, buttons, animations) lives in the website's code. It never changes no matter what's edited in the spreadsheet.
- **The content** (book titles, covers, news posts, bio text, contact info) lives in one Google Sheet. Edit a cell, publish the sheet, reload the site — done.

## Part A — One-time setup (you do this once)

### 1. Create the spreadsheet

1. Go to [sheets.google.com](https://sheets.google.com) and create a new blank spreadsheet. Name it something like "Yulia Aslanova Website Content."
2. Rename the default tab (bottom-left) to **Bio**. Add these column headers in row 1, exactly as written:
   ```
   Name | Bio | Photo URL
   ```
   In row 2, fill in one entry: her name, her bio paragraph, and the URL of her photo.
3. Click the **+** at the bottom to add a new tab. Name it **Projects**. Row 1 headers:
   ```
   Project title | Project description
   ```
   Add one row per project below that.
4. Add a tab named **Books**. Row 1 headers:
   ```
   Book title | Cover image URL
   ```
   One row per book.
5. Add a tab named **News**. Row 1 headers:
   ```
   News title | News description
   ```
   One row per news item.
6. Add a tab named **Contact**. Row 1 headers:
   ```
   Email | Agent email | Social platforms (comma separated)
   ```
   One row: her email, her agent's email, and something like `Goodreads, Facebook, Instagram, Youtube`.

Column names must match exactly (capitalization doesn't matter, but spelling does) — the website looks for these specific column names.

### 2. Publish each tab to the web

For **each of the 5 tabs** (Bio, Projects, Books, News, Contact), one at a time:

1. Make sure that tab is the active/selected one.
2. Go to **File → Share → Publish to web**.
3. In the dialog, use the first dropdown to select that specific sheet tab (not "Entire Document").
4. Use the second dropdown to choose **Comma-separated values (.csv)**.
5. Click **Publish**, confirm.
6. Copy the link it gives you — it'll look like:
   ```
   https://docs.google.com/spreadsheets/d/e/2PACX-.../pub?gid=123456&single=true&output=csv
   ```
7. Repeat for the other 4 tabs. You'll end up with 5 separate links.

### 3. Give the links to your developer

Send all 5 links, labeled by tab name. They get pasted into the website's code once (a five-minute change), after which the site reads live from your sheet automatically — no further code changes, ever, for routine content edits.

*(Developer note: paste each link into the matching entry in `SHEET_CSV_URLS` near the top of the `<script>` block in `index.html`.)*

## Part B — Editing content (this is what you'll do regularly)

1. Open the spreadsheet.
2. Edit a cell — fix a typo, change a description, swap an image URL, add a whole new row for a new book or news item.
3. That's it. Because the tab is already "published to web," changes save automatically — there's no separate publish button to click after the first-time setup. Just reload the actual website (Ctrl+R or Cmd+R) a few seconds after editing, and your change appears.

### Adding a new book

Go to the **Books** tab, click into the first empty row below your last book, type the title in one cell and the cover image URL in the next. Reload the site.

### Adding a new news post

Same idea on the **News** tab: title in one column, description in the next, in a new row.

### Where do image URLs come from?

Upload the image somewhere that gives you a direct link — Google Photos (right-click → "Copy image address" after opening it), imgur.com, or similar — then paste that link into the "Cover image URL" or "Photo URL" column.

## What to Never Touch

- Don't rename the column headers in row 1 — the website is looking for those exact words.
- Don't rename the tabs (Bio / Projects / Books / News / Contact) — if you do, re-publish and send your developer the new link.
- Don't touch anything your developer says is "in the code" — that's layout and design, separate from your spreadsheet entirely.

## If Something Looks Wrong

- **Edit didn't show up?** Wait ~30 seconds (Google Sheets takes a moment to refresh a published link) and reload the site again.
- **A row disappeared from the site?** Check you didn't leave a required cell blank — an empty title, for example, may cause that row to be skipped.
- **Still stuck?** Nothing you do in the spreadsheet can break the website's design — worst case, ask your developer to double check the published links still work.
