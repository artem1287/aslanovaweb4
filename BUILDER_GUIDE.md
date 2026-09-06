# Editing Your Website — A Simple Guide

You do not need to know any coding, HTML, or "web design" to update your website. This guide matches the **current** version of Builder.io (2026) — it will walk you past the specific screens you'll actually see, not an outdated tutorial.

## The Big Picture

Your website has two parts:

- **The design** (colors, layout, fonts, buttons, animations) — this lives in code and only your developer touches it. It will not change no matter what you edit.
- **The content** (your book list, news posts, bio text, contact info) — this lives in a separate tool called **Builder.io**, and you can change it yourself, any time.

Think of it like a picture frame (the design, fixed) and the photo inside it (the content, swappable by you).

## Important: Builder.io Now Has Two Different Products

This trips people up, so read this part first. When you log into Builder.io today, you'll be offered (or land in) one of two very different tools:

| | **Fusion** | **Publish** |
|---|---|---|
| What it's for | AI writes/generates *code*, connects to GitHub | Editing *content* (text, images, dates) through simple forms |
| Who uses it | Developers | You |
| What you'll see | A screen asking "What should we build?" with a GitHub repo connector | A left-side menu with **Models** and **Content** |

**You want a Publish space, not Fusion.** Fusion is for writing app code with AI — not what we're doing here, since your site's design/code is already built and finished. If you land on a "What should we build?" AI prompt screen with a GitHub connector, that's Fusion — that's the wrong place for day-to-day content editing.

### How to get to a Publish space

1. In Builder.io, go to your **Organization** view.
2. Click **New Space**.
3. In the dialog, name it and choose **Publish** as the space type (not Fusion).

**If you don't see a "Publish" option** — some newer accounts default into a Fusion-only trial and hide this choice. This is a known issue. If it happens, contact Builder.io support directly and ask them to enable/move your account to a standard Publish space. Don't fight the UI trying to find a hidden setting — this specific snag needs their support team.

## Two Ways to Make Edits (once you're in a Publish space)

**Option 1 — Chat with an AI (recommended).** Builder.io has an official "MCP" connector that lets you talk to Claude in plain English and it makes the content changes directly:
- "Add a new book called [title] with this cover image."
- "Change the description of my latest book."
- "Add a news post about [event]."
- "Make this book featured."

**One-time setup (your developer should do this with you):**
1. In your Builder Publish space: **Integrations** → find the "Builder.io CMS" tile → **+ Connect** → pick this Publish space.
2. In Claude (claude.ai or the desktop app): **Settings → Connectors → Add custom connector**, paste in `https://mcp.builder.io/mcp/publish`.
3. A browser window opens asking you to log into Builder.io and confirm — after that, it's automatic every time.

After setup, you never need to open the Builder.io website at all — just talk to Claude.

**Option 2 — Fill in a simple form directly in Builder.io.** Log in, go to **Content** (left sidebar), pick "Books" or "News," click **+ New Entry**, and fill in labeled boxes (Book title, Book cover, Description, etc.). There's also a **Generate** tab inside each entry where you can type a description and let Builder's built-in AI fill the boxes for you, which you then review and accept.

Either way — chat or form — nothing shows up on your real website until you (or the AI) hits **Publish**, not just "Save."

## Adding a Book

1. Content → **Books** → **+ New Entry** (or just tell Claude "add a new book").
2. Fill in: title, subtitle, cover image, description, publication date, where to buy, featured status.
3. **Publish**.
4. Reload your website — the new book appears using your site's existing design, automatically.

## Editing or Removing a Book

- **Edit:** open the entry, change any field, **Publish**.
- **Remove:** prefer **unpublish** over delete — it hides the book from the live site but keeps it saved, so nothing is lost if you change your mind.

## Adding or Editing News

Same idea, under Content → **News**: title, image, short summary, full text, publication date. Fill in (or ask Claude), Publish, done.

## What You Should Never Touch

- **Models** (not Content) — this is the *shape* of the form itself, set up once by your developer. Editing this can break the site's design.
- Anything involving GitHub, code files, or a **Fusion** space — that's your developer's side, not yours.

If you stick to **Content** entries (forms or Claude chat) in a **Publish** space, you cannot break the site. Worst case is a typo — easy to fix, never a broken page.

## If Something Looks Wrong

- **Change didn't show up?** Make sure you (or Claude) actually clicked **Publish**, not just saved a draft. Then reload the site.
- **Can't find Models/Content, only see an AI prompt box?** You're in a Fusion space by mistake — see "How to get to a Publish space" above.
- **Still stuck?** Contact your developer, or Builder.io support for account/space issues — the design and code stay safe no matter what happens on the content side.
