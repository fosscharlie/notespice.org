# Changelog

## 1.5.2 — 2026-07-28

- Removed the awwwe credit entirely — the mark and the "powered by"
  text alongside it. The footer credit is back to plain "Notespice —
  vibe-coded with Claude."

## 1.5.1 — 2026-07-28

- Added a "Sponsored by Lightmorphic" credit, bottom right, stacked
  directly above the version badge. The whole badge — text, logo, and
  a small "opens in a new tab" icon — is a single link; the logo is
  the real Lightmorphic wordmark (light-theme and dark-theme files),
  embedded as base64 the same way every other image on this page is,
  so the site stays a single self-contained file with zero external
  requests. Not a link yet — needs the Lightmorphic destination URL.

## 1.5.0 — 2026-07-28

- Footer credit now reads "...vibe-coded with Claude - powered by
  awwwe", with an inline awwwe mark: the full a-WWW-e wordmark in
  light theme, and the WWW badge alone in dark theme (the wordmark's
  dark lettering would disappear against the dark canvas). Drawn as
  inline SVG using the site's own embedded Geist font — no separate
  image files, no external request, consistent with how every other
  asset on this page is embedded. This is a redrawn approximation of
  the supplied awwwe logo, not a pixel copy of a source file (none
  was available to embed directly). The credit isn't a link yet —
  add the awwwe destination URL to wire that up.

## 1.4.1 — 2026-07-28

- Moved the "SELF-HOSTED · OPEN SOURCE" eyebrow down to sit directly
  above the View on GitHub / Get started buttons, instead of above
  the headline.

## 1.4.0 — 2026-07-28

- Typeface switched from Urbanist to Geist, site-wide — including the
  live demo card (Writer, Markdown, and toolbar all inherit the body
  font, so nothing was left on the old face). Urbanist is gone
  completely: both `@font-face` rules, the base64 payload, and every
  mention of the name were removed, not just superseded. Geist is
  self-hosted the same way — fetched once, embedded as base64 in
  `index.html` — so there's still no request to any font service at
  runtime, ever.
- Added a small site-version badge, bottom right of the page, linking
  to this release's GitHub notes.

## 1.3.0 — 2026-07-28

- New dark-theme palette: cool navy neutrals — `#10141C` page
  background, `#19212B` surfaces (app window, cards, code blocks),
  with matching blue-gray drawer, inputs, borders, and text tints —
  replacing the warm yellow-biased darks inherited from the app. The
  brand yellow accent and the light theme are unchanged.
- Versioned releases, the same way the notespice app repo does them:
  every update now gets its own `## X.Y.Z — YYYY-MM-DD` changelog
  section, and pushing the version tag creates the matching GitHub
  release automatically (new `release.yml` workflow — tag = bare
  version, title from the changelog heading, body = the section
  verbatim). Releases 1.0.0 through 1.2.1 backfilled, each tagged at
  the commit where that version went live.

## 1.2.1 — 2026-07-28

- Added a "Blank lines that stay" feature row: unlike most markdown
  editors, which silently collapse anything beyond one blank line,
  Notespice keeps extra empty lines — stored as literal `<br>` lines
  in the markdown, so GitHub renders them identically.

## 1.2.0 — 2026-07-28

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

## 1.1.0 — 2026-07-22

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
