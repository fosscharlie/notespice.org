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
  changes, the site follows it, not the other way around. One
  deliberate exception (owner request, 2026-07-28): the site's dark
  theme uses cool navy neutrals (#10141C canvas, #19212B surfaces)
  instead of the app's warm darks.
- Every update is a release, the same way the notespice app repo
  does it: add a `## X.Y.Z — YYYY-MM-DD` section to the top of
  `CHANGELOG.md` (patch bump for tweaks/fixes, minor for features or
  visual changes), commit and push to main, then
  `git tag -a X.Y.Z -m "notespice.org X.Y.Z" && git push origin X.Y.Z`
  — the `release.yml` workflow turns the tag into the GitHub release
  (title from the changelog heading, body = the section verbatim).
  No "Unreleased" section; nothing sits unversioned.
- Verify visual changes in a real browser before pushing (Chromium is
  preinstalled; Playwright works with
  executablePath /opt/pw-browsers/chromium).
