<div align="center">

# IT WORK'S!

**A single self-contained HTML page that proves the pipeline is alive.**

[![Live demo](https://img.shields.io/badge/demo-live-22c55e?style=flat-square)](https://saumon.github.io/it-works/)
[![Built with Paperclip](https://img.shields.io/badge/built%20with-Paperclip-6366f1?style=flat-square)](#built-with-paperclip)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![Zero dependencies](https://img.shields.io/badge/dependencies-0-blue?style=flat-square)](#why-this-exists)
[![Last commit](https://img.shields.io/github/last-commit/saumon/it-works?style=flat-square)](https://github.com/saumon/it-works/commits/main)

[Live demo](https://saumon.github.io/it-works/) · [Quick start](#quick-start) · [Built with Paperclip](#built-with-paperclip)

</div>

---

## Overview

`it-works` is the smallest possible deployable web artifact: one `index.html` file that renders
a centered **IT WORK'S!** headline on a dark background. No build step, no package manager,
no runtime, no external request. Open the file and it works — that is the entire point.

It doubles as the reference project for a Paperclip-piloted software company: every commit in
this repository was planned, written and shipped by autonomous agents coordinated through
[Paperclip](#built-with-paperclip).

## Why this exists

A "hello world" page is the fastest honest end-to-end test of a delivery chain. Keeping it at
**zero dependencies** means that when this page renders, nothing can be blamed on a bundler,
a lockfile or a CDN — the repository, the pipeline and the host are all working.

## Features

- **Self-contained** — a single file, with CSS inlined in a `<style>` block.
- **Zero dependencies** — no npm, no CDN, no fonts to download, no network call at runtime.
- **Responsive typography** — the headline scales with the viewport via `clamp(2rem, 10vw, 6rem)`.
- **System font stack** — native look on every OS, nothing to load.
- **Instantly deployable** — any static host works; GitHub Pages is already serving it.

## Quick start

```bash
git clone https://github.com/saumon/it-works.git
cd it-works
```

Then pick whichever you prefer:

| Method | Command | Notes |
| --- | --- | --- |
| Open directly | double-click `index.html` | No tooling required |
| Python | `python3 -m http.server 8000` | Serves at <http://localhost:8000> |
| Node | `npx serve .` | Requires Node.js |

## Project structure

```text
it-works/
├── index.html   # the entire application: markup + inlined styles
└── README.md    # you are here
```

## Customization

Everything lives in `index.html`:

| What | Where |
| --- | --- |
| Headline text | the `<h1>` element |
| Background color | `body { background: #0f172a; }` |
| Text color | `h1 { color: #f8fafc; }` |
| Headline size | `h1 { font-size: clamp(2rem, 10vw, 6rem); }` |

## Deployment

The page is published with **GitHub Pages** from the `main` branch and is live at
<https://saumon.github.io/it-works/>.

Any other static host works the same way — upload `index.html` and you are done.
Netlify, Vercel, Cloudflare Pages and S3 all require zero configuration for this project.

## Built with Paperclip

This project was **created and piloted with Paperclip**, an agent-orchestration platform that
runs a software company as a set of coordinated AI agents.

How the work actually happened:

1. **Intent** — a goal is filed as a task in the Paperclip control plane (for example
   *"the README must be state of the art"*).
2. **Routing** — the chief-of-staff agent scopes the task, sets its title, and either does the
   work or delegates it to a specialized agent.
3. **Execution** — the assigned agent works in a real git checkout of this repository, with the
   task's approval gates enforced by the platform.
4. **Review** — changes are reported back on the task thread, where a human keeps final say
   before anything is shipped.

Everything you see in this repository — the page, the commits, and this README — is the output
of that loop. Nothing here was hand-written.

## Contributing

Issues and pull requests are welcome. Keep the spirit of the project intact:

- **One file.** Changes belong in `index.html`.
- **No dependencies.** No build tooling, no package manager, no external asset.
- **No network calls.** The page must render offline, with the file opened directly from disk.

## License

No license file is present yet, so default copyright applies — all rights reserved by the
repository owner. Open an issue if you need this released under an open-source license.
