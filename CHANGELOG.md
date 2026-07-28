# Changelog

## Unreleased

- Added a "Blank lines that stay" feature row: unlike most markdown
  editors, which silently collapse anything beyond one blank line,
  Notespice keeps extra empty lines — stored as literal `<br>` lines
  in the markdown, so GitHub renders them identically.

- Redesigned the whole page to match the app's 1.5.0 Material
  redesign: Urbanist replaces Inter (still embedded — no external
  font request), the app's own warm yellow-biased Material tokens
  replace the old flat grays, and the page now follows the system
  color scheme with a light and a dark theme, like the app itself.
  Buttons are pill-shaped, code renders in Urbanist (the app dropped
  its monospace face), and keyboard focus rings and
  `prefers-reduced-motion` support were carried over from the app's
  stylesheet.
- The demo card is now a scaled-down copy of the redesigned app
  chrome, piece by piece: a navigation drawer with pill-shaped note
  rows (yellow-tinted active state), a rounded Material search bar
  that really filters notes by name, drawer brand header,
  Export/Import pills and a footer link to the repo, a top app bar
  with the brand mark and round state-layer icon buttons, a
  segmented Writer/Markdown control, a live save indicator, an
  extended "New note" FAB bottom right (replacing the old tiny "+"
  in the sidebar), and the app's editor content styles — amber
  links, tinted callouts, accent-colored checkboxes. The app-bar
  menu button now actually collapses the drawer, and on phone
  widths the app bar wraps into two rows exactly like the real app.

- Fixed note title and content in the demo appearing center-justified
  (inherited from the hero section's centered layout) instead of
  left-justified, matching how markdown/notes actually render.
- Fixed the demo's Code and Checkbox-list toolbar buttons inserting
  visible placeholder text when nothing was selected, instead of
  leaving the cursor ready to type. Also fixed the footnote button
  using `innerHTML +=` to append its definition stub, which
  unnecessarily reparses the whole editor's content.
- Added a favicon (embedded, no extra file).
- Hero is now a single stacked column (text, then demo, then caption)
  instead of two-column, matching the requested layout.
- Demo card now has the full toolbar (heading levels, GitHub-style
  callouts, tables, footnotes, links/images/attachments) and a working
  Delete button with confirmation, ported directly from the real app —
  not a simplified stand-in.

## 1.0.0 — 2026-07-22

Initial release.

- One-page landing site: hero with a working embedded Writer/Markdown
  demo, "why" section, feature grid, Docker Compose get-started guide,
  footer links.
- Self-hosted Inter typeface and embedded logo — no external font or
  image requests at all.
- Monochrome window-control icons in the demo card (not macOS-style
  colored traffic lights).
