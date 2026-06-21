# CLAUDE.md

Guidance for Claude Code working in this repository (the shamiatrestaurant.com static site).

## Coding guidelines

ALWAYS follow the `karpathy-guidelines` skill when writing, reviewing, or refactoring code — think before coding, simplicity first, surgical changes, goal-driven execution. The skill lives in `.claude/skills/karpathy-guidelines/`.

## Site notes

- This is a single-page static site: `index.html` holds all markup, CSS (inline `<style>`) and JS (inline `<script>`). Hosted on GitHub Pages (`CNAME` → shamiatrestaurant.com).
- Media is heavy (multi-MB hero/reel videos). Keep videos `preload="none"` so mobile devices are not forced to download them before the page renders.
