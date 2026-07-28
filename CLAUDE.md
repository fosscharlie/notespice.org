# Claude working notes for notespice.org

## Workflow: push directly to main, no pull requests

The repo owner (fosscharlie) has given standing permission
(2026-07-28) to commit directly to `main` and push, without opening
pull requests and without waiting for their input — the same workflow
used for the fosscharlie/notespice app repo. Do not create PRs for
changes to this site unless the owner asks for one.

## About this site

- The whole site is one self-contained `index.html` served by GitHub
  Pages: fonts (Urbanist, matching the app), logo, CSS, and the live
  demo's JS are all embedded. Keep it zero-external-request.
- The design mirrors the app's own stylesheet
  (fosscharlie/notespice `static/style.css`) — when the app's design
  changes, the site follows it, not the other way around.
- Update `CHANGELOG.md` (Unreleased section) with each change.
- Verify visual changes in a real browser before pushing (Chromium is
  preinstalled; Playwright works with
  executablePath /opt/pw-browsers/chromium).
