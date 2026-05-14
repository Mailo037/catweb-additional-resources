# Submission Template

Every submission lives in its own folder inside `library/`. Create the folder there, then copy the blocks below into the matching files.

```
library/your-folder-name/
├── info.md          (required)
├── content.md       (required)
└── credits.md       (optional — to credit the creator(s) of this submission)
```

A blank `CREDITS.md` lives next to this file — copy it into your folder as `credits.md` and fill it in (or leave it out entirely if you're a solo author and `info.md`'s `author:` field is enough).

---

## `info.md` — copy this block

```markdown
---
title: "Short, descriptive title"
author: "@your-handle"
category: "site"               # site | page | component | snippet
catweb_version: "2.17.3.0"
site: "your-site.rbx"          # optional, if uploaded on a CatWeb site
tags: [tag1, tag2, tag3]
type: "json"                   # json | upload-code | json,upload-code
requires: []                   # optional, e.g. [cookies, premium]
updated: "YYYY-MM-DD"          # optional
---

One paragraph describing what this is, when to use it, and anything the
reader should know before importing it. Keep it tight — two or three
sentences are usually enough.
```

---

## `content.md` — JSON, upload code, or both

Include whichever you have. If you ship both, label each section with a heading so it's clear which is which. Set `type` in `info.md` accordingly (`json`, `upload-code`, or `json,upload-code`).

````markdown
## Upload code

```
ABC123
```

## JSON

```json
[
  {
    "class": "frame",
    "globalid": "container-main",
    "size": "{1,0},{1,0}",
    "background_color": "#1a1a1a"
  }
]
```
````

Drop either section if you don't need it.

---

## `credits.md` — optional, copy this block if you need it

Plain Markdown, no frontmatter. Use this file to credit the **person (or people) who made the submission**, including profile links (GitHub / Discord / Roblox) and where the site was uploaded. Handy when there's more than one creator, or you want richer info than `info.md`'s `author:` field allows.

```markdown
# Credits

## Made by

- **@your-handle** — role / what they did
  - GitHub: [@your-handle](https://github.com/your-handle)
  - Discord: `@your-handle`
  - Roblox: [YourName](https://www.roblox.com/users/123456789/profile) (ID: `123456789`)
- **@second-person** — role / what they did
  - Discord: `@second-person`
  - Roblox: [TheirName](https://www.roblox.com/users/987654321/profile) (ID: `987654321`)

## Uploaded on

- `your-site.rbx` (CatWeb)
```

Drop any section / line you don't need. Skip the file entirely if `info.md`'s `author:` already covers it.

A pre-filled blank version of this file lives at [`template/CREDITS.md`](./CREDITS.md) — copy it into your folder as `credits.md` and edit.

---

## Quick checklist before opening a PR

- [ ] Folder is placed inside `library/` and named in `kebab-case`
- [ ] `info.md` frontmatter is fully filled in
- [ ] `type` in `info.md` matches what's actually in `content.md` (`json`, `upload-code`, or `json,upload-code`)
- [ ] JSON is valid and tested inside CatWeb
- [ ] No comments inside the JSON (CatWeb's parser breaks on them)
- [ ] `catweb_version` reflects the version you tested against
- [ ] If there are multiple creators / you want profile links, you've added a `credits.md`
