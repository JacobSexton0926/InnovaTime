# InnovaTime

Flask + SQLite time-tracking app for InnovaTek Solutions. The whole app lives
inside `InnovaTime 6-22-26.zip` — there are no loose source files in the repo.

## Working on the app

- Extract the zip, edit files under `InnovaTime 6-22-26/`, then update just the
  changed entries in place (run from the extraction's parent folder):
  `zip "InnovaTime 6-22-26.zip" "InnovaTime 6-22-26/templates/foo.html" ...`
- Never replace `timeslips.db` inside the zip — it's an old snapshot, and the
  live servers hold the real data.
- When telling the user how to deploy, list only the folders/files that
  changed (usually `static` and/or `templates`), remind them to restart the
  app, and warn them not to copy `timeslips.db` over the server's copy.

## Versioning — bump with every change

The version shows in the nav bar and is hardcoded in exactly one place:
`templates/layout.html` (the `<span class="brand-ver">` under the logo in the
sidebar).

Every change merged to `main` must bump it (semantic versioning, MAJOR.MINOR.PATCH):

- **PATCH** (1.5.0 → 1.5.1) — bug fixes, wording/layout tweaks, small
  adjustments to existing behavior.
- **MINOR** (1.5.1 → 1.6.0) — new features, screens, buttons, reports or
  workflows; resets PATCH to 0.
- **MAJOR** (1.x → 2.0.0) — only for changes that break things: data that
  needs manual migration, or removed/incompatible workflows. Ask the user
  before doing a major bump.

With each bump, add an entry at the top of `CHANGELOG.md` (version, date,
plain-language bullets) and tell the user the new version number.
Several changes in one pull request share a single bump.
