# Eglīšu rotājumu veikals

## Stack

- **Language / Runtime**: HTML5, CSS, and browser JavaScript. No server, no bundler.
- **Framework**: none. Static site built on the HTML5 UP "Escape Velocity" template.
- **Key dependencies**: jQuery with the dropotron dropdown plugin, breakpoints.js, Font Awesome for icons, Google Fonts (Source Sans Pro).
- **Package manager**: none. There is no install step and no build tooling.

## Build approach

<TBD, set by /scope>

## Commands

```bash
# Install
# none, there is nothing to install

# Preview locally
python -m http.server 8000
# then open http://localhost:8000

# Rebuild CSS from Sass (read the warning in Rules first)
sass assets/sass/main.scss assets/css/main.css

# Test
# none, there is no test runner
```

## Specs

Stored in `docs/specs/`. Format: `docs/specs/NNNN-title.md`.

## Rules

- All visible copy is in Latvian. Write new page text in Latvian, matching the tone of `index.html`.
- Each page is a complete HTML file at the repo root (`index.html`, `katalogs.html`, `galerija.html`, `par-mums.html`). Every page loads `assets/css/main.css` in the head and the same six scripts at the end of the body, in this order: `jquery.min.js`, `jquery.dropotron.min.js`, `browser.min.js`, `breakpoints.min.js`, `util.js`, `main.js`.
- The header nav block is repeated in every page. Change it in all four files together.
- `assets/css/main.css` is the live stylesheet and has drifted from `assets/sass/main.scss`. The `.snow` rules and the `animatedBackground` keyframes exist only in the CSS, and no page uses them today. Edit `main.css` directly. If you ever compile the Sass, port those rules in first, or the compile will drop them.
- Treat `assets/js/jquery.min.js`, `assets/js/jquery.dropotron.min.js`, `assets/js/browser.min.js`, `assets/js/breakpoints.min.js`, `assets/css/fontawesome-all.min.css`, and `assets/webfonts/` as vendor files. Do not edit them.
- Page images live in `images/` and are referenced relative to the page, for example `images/pic01.jpg`.
- The design derives from the HTML5 UP Escape Velocity template under the CC BY 3.0 license. Keep the credit in `README.txt` and `LICENSE.txt`.

## Agent skills

- [add-icon](.agents/skills/add-icon/): `fortawesome/fontawesome-agent-tools`, adds Font Awesome icons with the correct markup for this CSS setup.
- [fa-help](.agents/skills/fa-help/): `fortawesome/fontawesome-agent-tools`, answers Font Awesome questions from the official docs.

## Context files

<!-- Nested AGENTS.md files are listed here as they are created -->

_Drafted by /audit from the repo, worth a quick human pass. Edit freely: once a line stops matching this draft, later runs treat it as curated and will flag rather than overwrite it._
