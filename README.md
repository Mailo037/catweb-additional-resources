# CatWeb Additional Resources

Premade JSONs and entire sites for **CatWeb** (Roblox) — the Roblox game where you build 2D websites with JSON-based UI and a visual block-scripting system.

This repo is the companion to [`catweb-docs`](https://github.com/mailo037/catweb-docs). While `catweb-docs` is the official reference (CatDocs, JSONScript, UIGPT), this repo is a community drop-box of **ready-to-import JSONs and full sites** you can grab and use.

> Targeting CatWeb version **v2.17.3.0**

---

## Table of Contents

1. [How submissions are stored](#how-submissions-are-stored)
2. [The three files](#the-three-files)
3. [Submitting your own](#submitting-your-own)
4. [I want my stuff gone](#i-want-my-stuff-gone)
5. [Related Repos](#related-repos)
6. [Credits](#credits)

---

## How submissions are stored

Every JSON or site is its **own folder** inside [`library/`](./library/). Each folder contains two required files and one optional file. The `template/` folder at the repo root holds the copyable submission template — keep it separate from the library so newcomers can find it.

### Layout

```
catweb-additional-resources/
│
├── README.md
├── template/                ← copy this into library/your-folder/ when submitting
│   ├── TEMPLATE.md          ← instructions + copyable blocks
│   └── CREDITS.md           ← blank credits template (copy → credits.md)
│
└── library/
    ├── cool-login-page/
    │   ├── info.md          ← what is this
    │   ├── content.md       ← the JSON (or an upload code)
    │   └── credits.md       ← (optional) who made it
    │
    ├── neon-button-pack/
    │   ├── info.md
    │   └── content.md
    │
    └── full-portfolio-site/
        ├── info.md
        ├── content.md
        └── credits.md
```

### Inside a folder

```
┌──────────────────────────────────────────────────────────────┐
│  <folder-name>/                                              │
│  ───────────────────────────────────────────────────────     │
│                                                              │
│   ┌─────────────┐    ┌─────────────┐    ┌─────────────┐      │
│   │  info.md    │    │ content.md  │    │ credits.md  │      │
│   ├─────────────┤    ├─────────────┤    ├─────────────┤      │
│   │ title       │    │ ```json     │    │ Made by:    │      │
│   │ category    │    │ [ … ]       │    │ - @person1  │      │
│   │ version     │    │ ```         │    │   GH/DC/RBX │      │
│   │ site        │    │   - OR -    │    │ - @person2  │      │
│   │ tags        │    │             │    │             │      │
│   │ description │    │ ABC123      │    │ Uploaded on │      │
│   └─────────────┘    └─────────────┘    └─────────────┘      │
│                                                              │
│     metadata           actual upload      (optional)         │
│     (required)         (required)         who made it        │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

---

## The three files

| File         | Required | What it holds                                                                                       |
| ------------ | :------: | --------------------------------------------------------------------------------------------------- |
| `info.md`    |    ✓     | YAML frontmatter (title, author, category, version, site, tags, type, …) + a one-paragraph summary. |
| `content.md` |    ✓     | Either the raw CatWeb JSON in a ` ```json ` block, **or** a 6-character upload code. Nothing else.  |
| `credits.md` |          | Multiple creators / profile links (GitHub, Discord, Roblox name + ID) and the catweb link. |

> **Copyable templates** live in [`template/`](./template/) — see [`template/TEMPLATE.md`](./template/TEMPLATE.md) for the full content of each file, and [`template/CREDITS.md`](./template/CREDITS.md) for a blank credits file to copy into your folder.

---

## Submitting your own

1. Create a new folder inside `library/` (e.g. `library/neon-button-pack/`).
2. Copy the blocks from [`template/TEMPLATE.md`](./template/TEMPLATE.md) into `info.md` and `content.md`.
3. Fill in the frontmatter and drop in your JSON or upload code.
4. *(optional)* Copy [`template/CREDITS.md`](./template/CREDITS.md) into your folder as `credits.md` and fill it in.
5. Test the JSON inside CatWeb first.
6. Open a PR with a one-line description.

---

## I want my stuff gone

If you find your JSONs or sites in here and want them removed:

- Open a **PR that deletes the affected folder(s)**.
- Include **proof of ownership** in the PR description — a Discord message, a screenshot from inside CatWeb showing the same site under your account, or any other clear link between you and the content.

We'll merge promptly once ownership checks out.

---

## Related Repos

- [`catweb-docs`](https://github.com/mailo037/catweb-docs) — official reference (CatDocs, JSONScript, UIGPT)
- [`catweb-mcp`](https://github.com/Mailo037/catweb-mcp) — MCP server that indexes this repo + `catweb-docs` so AI agents (Claude, etc.) can search templates by tag/author/type and pull the JSON directly into chat. See its README for setup.

## AI / agent usage

If you're an AI assistant or pointing one at this repo, you can either:

1. **Read the folders directly** — every submission lives under `library/`; `info.md` has YAML frontmatter (title, author, category, tags, type, source) and each `content.md` holds the upload-code and/or JSON in fenced blocks.
2. **Use the [`catweb-mcp`](https://github.com/Mailo037/catweb-mcp) MCP server** — adds `search`, `find_templates`, `get_template`, etc. tools so you don't have to crawl every folder. Recommended for non-trivial queries.

---

## Credits

Big thanks to everyone submitting stuff.
