# Editing Your Website with Google Sheets — Setup Guide

This replaces the earlier Builder.io plan (its content-editing tier required a paid subscription). This approach is completely free, and the "editor" is just a spreadsheet — something you likely already know how to use.

The website is now connected to: **"Yulia Aslanova Website Sheet."**

## The Big Picture

- **The design** (colors, layout, fonts, buttons, animations) lives in the website's code. It never changes no matter what's edited in the spreadsheet.
- **The content** (book titles, covers, project/news posts, bio text) lives in the Google Sheet. Edit a cell, reload the site — done. There's no separate "publish" button to click; as long as the sheet stays shared as "Anyone with the link can view," edits go live automatically.

## Current Tabs and Their Columns

The sheet already has 4 tabs set up and connected:

| Tab | Columns (must match exactly) |
|---|---|
| **Bio** | `Name`, `Bio`, `Photo URL` |
| **Projects** | `Project Title`, `Project Description`, `Project Image URL` |
| **Books** | `Book Title`, `Cover Image URL`, `Book Description`, `Book Price`, `Buy URL` |
| **News** | `News Title`, `News Description`, `News Image URL` |

Each row below the header row is one entry (one book, one news post, etc.). The **Image URL** columns are optional — leave a row's image cell blank and that entry just shows a plain placeholder box instead of a photo.

Clicking any book on the Books page opens its own page showing the title, cover, `Book Description`, and `Book Price`. If you fill in `Buy URL` (a real link to where people can buy it), the "Оформить заказ" button links straight there in a new tab; leave it blank and the button just sends people to the Contact page instead. `Book Description` and `Book Price` are optional too — until you fill them in, that book's page shows a note explaining which column to fill in, instead of just leaving a confusing blank space.

**There's no "Contact" tab yet**, so contact info (email, agent email, social links) still shows the original hardcoded text rather than being editable. If you want that editable too, tell your developer — it's a 5-minute addition once a Contact tab exists with columns `Email`, `Agent email`, `Social platforms (comma separated)`.

## Adding or Editing Content

1. Open the sheet.
2. To edit an existing entry: click a cell, type the new text, press Enter.
3. To add a new book/project/news item: click the first empty row below the last one, fill in each column.
4. Reload the actual website (Ctrl+R / Cmd+R). Your change appears within a few seconds — no extra "publish" step.

### Where do image URLs come from?

Upload the image somewhere that gives you a direct link — Google Photos (open the image, right-click → "Copy image address"), imgur.com, or similar — then paste that link into the matching "Image URL" column.

## Adding a Whole New Section (e.g. a Contact tab)

If you ever add a new tab yourself, it won't automatically connect to the site — your developer needs to add its link to the code once. Tell them the tab name and its columns, and they'll wire it up.

## What to Never Touch

- Don't rename the column headers in row 1 (`Name`, `Bio`, `Book Title`, etc.) — the website looks for those exact words.
- Don't rename the tabs (Bio / Projects / Books / News) — if you do, tell your developer so they can update the connection.
- Don't change the sheet's sharing setting to "Restricted" — it needs to stay "Anyone with the link can view" for the website to read it. (This doesn't let anyone *edit* it — only you and anyone you explicitly share edit-access with can change it. "Anyone with the link" here only controls who can *view*.)
- Don't touch anything your developer says is "in the code" — that's layout and design, kept completely separate from your spreadsheet.

## If Something Looks Wrong

- **Edit didn't show up?** Reload the site again after a few seconds — sometimes the browser caches the old version briefly.
- **A row disappeared from the site?** Check you didn't leave the title cell blank — an entry with no title may get skipped.
- **Still stuck?** Nothing you do in the spreadsheet can break the website's design — worst case, ask your developer to double-check the sheet's sharing setting is still "Anyone with the link can view."
