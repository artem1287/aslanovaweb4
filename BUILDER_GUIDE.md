# Editing Your Website — A Simple Guide

You do not need to know any coding, HTML, or "web design" to update your website. This guide explains everything in plain language.

## The Big Picture

Your website has two parts:

- **The design** (colors, layout, fonts, buttons, animations) — this lives in code and only your developer touches it. It will not change no matter what you edit.
- **The content** (your book list, news posts, bio text, contact info) — this lives in a separate tool called **Builder.io**, and you can change it yourself, any time, without asking anyone.

Think of it like a picture frame (the design, fixed) and the photo inside it (the content, swappable by you).

## Two Ways to Make Edits

**Option 1 — Chat with an AI.** If your developer set up the Claude connector for you, you can just type in plain English:
- "Add a new book called [title] with this cover image."
- "Change the description of my latest book."
- "Add a news post about [event]."
- "Make this book featured."

The AI does the work and shows you the result before anything goes live.

**Option 2 — Fill in a simple form.** Log in to [builder.io](https://www.builder.io), go to **Content**, pick "Books" or "News," click **+ New Entry**, and fill in labeled boxes (Book title, Book cover, Description, etc.) — like filling out a form, not writing code.

Either way, nothing shows up on your real website until you press **Publish**.

## Adding a Book

1. Go to Builder.io → Content → **Books**.
2. Click **+ New Entry**.
3. Fill in: title, subtitle (if used), cover image, description, publication date, where to buy, and whether it's "featured."
4. Click **Publish**.
5. Reload your website — the new book appears in the same design as all your other books.

## Editing a Book

1. Go to Builder.io → Content → **Books**.
2. Click the book you want to change.
3. Edit any field (fix a typo, swap the cover image, update the buy link).
4. Click **Publish**.

## Removing a Book

You don't have to delete anything by accident-proofing it. Instead of deleting, you can **unpublish** an entry (keeps it saved, just hides it from the live site) — safer than permanent deletion. If you do want it gone for good, delete the entry and confirm.

## Adding or Editing News

Same steps as Books, under Content → **News**: title, image, short summary, full text, and publication date. Fill in, Publish, done.

## What You Should Never Touch

- Anything in Builder.io labeled **Models** (not Content) — that's the *shape* of the form itself (which boxes exist), set up by your developer. Editing this can break the site's design.
- Anything involving GitHub, code files, or the word "React" — that's your developer's side.

If you only ever use the **Content** section (not Models), you cannot break anything. Worst case, a typo — easy to fix, never a broken site.

## If Something Looks Wrong

- **Change didn't show up?** Make sure you clicked **Publish**, not just saved a draft. Then reload the page (Ctrl+R or Cmd+R).
- **Site shows old/placeholder content instead of your edit?** Double-check you edited the entry that's actually marked "featured" or in the right order — there may be more than one entry.
- **Still stuck?** Contact your developer — nothing you can do in Builder.io's Content section can permanently break the site; the design and code are separate and safe.
