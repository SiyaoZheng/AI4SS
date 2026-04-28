# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

AI4SS (AI for Social Science) — a 90-minute online lecture in reveal.js format. Single-file HTML presentation (`ai4ss.html`) targeting 研究生 + 青年学者 audience.

## Architecture

- **`ai4ss.html`** — Self-contained reveal.js 5.1 presentation (CDN-based, no local dependencies)

## Key Constraints

- **Language**: 中文为主，代码和术语用英文
- **Style**: 现代清新风 (white base + accent colors), no emoji
- **No live demo**: Pure slides only
- **De-AI writing**: Avoid AI-flavored patterns — no emoji, use 中文「」引号, avoid bold+description list patterns, avoid promotional language
- **No personal info**: Do not include Adrian's real name, institutional affiliation, or contact details in slides without explicit instruction

## Working with the HTML

The presentation is a single `ai4ss.html` file. To preview, open it directly in a browser. All reveal.js assets load from CDN (`cdn.jsdelivr.net/npm/reveal.js@5.1.0/`).

When editing slides, each `<section>` is one slide. Speaker notes go in `<aside class="notes">`.

CSS custom properties: `--accent`, `--accent-light`, `--text`, `--muted`, `--bg-card`, `--green`, `--amber`, `--red`.

Utility classes:
- Layout: `.grid-2`, `.grid-3`, `.center`, `.title-slide`
- Content boxes: `.card`, `.highlight-box`, `.good-box`, `.bad-box`, `.versus`
- Text: `.muted`, `.accent`, `.section-title`, `.footnote`
- Components: `.tag`, `.level-bar` + `.level-badge` (with optional `.active`)
- Animations: use `class="fragment"` (reveal.js built-in) for progressive disclosure
