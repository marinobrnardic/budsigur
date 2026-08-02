# budsigur

Source for my personal site — a static portfolio with no build step, no dependencies
and no framework. Plain semantic HTML, one stylesheet, deployed on GitHub Pages.

- `index.html` — the page
- `styles.css` — design tokens, layout, terminal theme

## Design direction

Old-school terminal: phosphor green on near-black, monospace throughout. The look is
the point, but it is **visual language only** — no fake shell, no typed commands, no
content hidden behind an interactive prompt. Everything is readable on arrival.

| Token | Value | Role |
|---|---|---|
| `--bg` | `#060a07` | near-black with a faint green cast |
| `--fg-bright` | `#7eff7e` | signature phosphor: headings, prompts, cursor |
| `--fg` | `#a9d9ae` | body copy — calmer green, easier over paragraphs |
| `--fg-dim` | `#57a066` | labels, years, chrome |
| `--accent` | `#ffb454` | amber: links and hover states |

Typeface is IBM Plex Mono (400/600).

Rules worth keeping:

- **Dark only, deliberately.** No light theme. A light terminal is a contradiction.
- **Glow on display type only.** `text-shadow` belongs on the `h1` and the cursor.
  On body copy at reading size it smears the text.
- **Lowercase is chrome, not content.** Section headings, tags and nav are lowercase;
  descriptions and prose keep normal sentence case so they stay scannable.
- **Hover inverts.** Background fills with the foreground colour, the way a terminal
  selection does — no lifts, no soft shadows.
- **One flourish.** A single blinking block cursor, disabled under
  `prefers-reduced-motion`. No typing animation, no scanlines.
- Every colour pair clears WCAG AA (4.5:1) against the background.

## Running locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000.
