# Editor snippets

Reusable content blocks that **editors** insert into posts and pages from the
Ghost editor — the closest equivalent to a custom card, since themes cannot
register new Koenig cards.

These are **not** loaded by the theme. They live here as the version-controlled
source of truth; installing them is a one-time action in Ghost Admin.

> **Handlebars does not run inside post content.** Snippet files are plain,
> static HTML (loader SVG and Mailchimp action inlined). They rely on the
> theme's existing CSS classes (e.g. `.subscribe-form` in
> `assets/css/screen.css`) for styling. For template-level reuse inside `.hbs`
> files, use the matching partial in `partials/` instead.

## Available snippets

| File | Purpose | Partial equivalent |
|------|---------|--------------------|
| `email-capture.html` | Mailchimp newsletter signup form | `partials/email-capture.hbs` |

## How to install a snippet in Ghost

1. In Ghost Admin, create or open any post/page.
2. Add an **HTML card**: click `+`, choose **HTML** (or type `/html`).
3. Paste the full contents of the snippet file (everything below the top comment).
4. Click outside the card to render it, then check it displays correctly.
5. Select the card (click its edge so the whole card is highlighted).
6. Click the **snippet icon** (the `{}`-style "Create snippet" button in the
   floating toolbar), give it a name (e.g. `Email capture`), and save.

The snippet is now available to all editors: type `/` in the editor and search
for its name, or open the snippets menu, to insert it into any post or page.

## Updating a snippet

Snippets are copies — editing the file here does **not** update snippets already
saved in Ghost. To roll out a change: update the file, then in Ghost delete the
old saved snippet and re-create it from the new HTML (steps above).
