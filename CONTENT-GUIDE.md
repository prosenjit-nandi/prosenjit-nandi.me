# Editing this site

This site is built with Jekyll and hosted on GitHub Pages, which builds it
automatically on every push to `main` — no build step, no plugin, and no
Claude session required for routine content updates. Everything below can be
done straight from github.com, including from your phone.

## Add a project

Edit `_data/projects.yml` (click the pencil icon on that file on github.com)
and add an entry in the same format as the existing ones:

```yaml
- name: your-repo-name
  url: https://github.com/prosenjit-nandi/your-repo-name
  description: "One or two sentences on what it does and why it's interesting."
  tags: [TAG ONE, "TAG TWO", "TAG THREE"]
```

Commit straight to `main`. The Projects section on the homepage picks it up
automatically and the grid re-flows to fit however many projects are
listed — no need to touch any HTML, and no limit on how many you add.

Don't add `prosenjit-nandi.me` (this repo) to the list — it's the site
itself, not a project to showcase.

## Publish an article

Add a new file in `_posts/` named `YYYY-MM-DD-a-short-title.md` — the date
and the slug in the *filename* both matter: Jekyll uses the date to sort
entries (newest first) and the slug to build the page's URL. Start the file
with a front-matter block, then write the article in Markdown underneath:

```markdown
---
title: "Your Article Title"
---

Your article, written in Markdown. Use `##` for headings, `**bold**`,
`[links](https://example.com)`, blank lines between paragraphs, and so on —
standard Markdown throughout.
```

Commit straight to `main`. It appears in the Writing section automatically,
newest first, and gets its own page at
`prosenjit-nandi.me/writing/your-short-title/`. The Writing section's
"nothing published yet" placeholder disappears on its own once there's at
least one post — nothing else to change.

## Anything about layout, colors, fonts, or the overall design

That's a design change, not a content change — bring that back to Claude.
The look and feel lives in `_layouts/default.html`, `_layouts/post.html`,
and `assets/css/style.css`.
