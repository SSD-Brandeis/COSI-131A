# COSI 131A — Fundamentals of Computer Systems

Course website for COSI 131A at Brandeis University, built with [Jekyll](https://jekyllrb.com/) and the [just-the-docs](https://github.com/just-the-docs/just-the-docs) theme (via the "just-the-class" collections pattern: staffers / modules / announcements). Structure mirrors [COSI-127B](https://github.com/SSD-Brandeis/COSI-127B).

- **Instructor:** Subhadeep Sarkar
- **TA:** Shubham Kaushik
- **Term:** Fall 2026 — Tue/Thu 3:55–5:15 PM lecture, Wed 5:40–7:40 PM recitation

## Structure

Each semester's site lives in its own top-level folder (`2026/`, and later `2027/`, etc.), so past semesters stay frozen and browsable. The root [`index.html`](index.html) redirects to the current semester. [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml) builds every year-folder into `_site/<year>/` and deploys the combined output to GitHub Pages on every push to `main`.

```
2026/
├── _config.yml       # site title, links (syllabus/piazza/gradescope/moodle), theme settings
├── _staffers/         # instructor/TA bios (photo, office hours, etc.)
├── _modules/           # schedule entries (one definition list per lecture/recitation)
├── index.md, schedule.md, assignments.md, policies.md, resources.md
├── assets/
│   ├── images/         # logos, staff photos
│   ├── pdf/             # syllabus PDF goes here
│   └── css/             # vendored just-the-docs assets
└── _sass/, _layouts/, _includes/   # theme + custom overrides (banner, colors, etc.)
```

## Local development

```bash
bundle install
bundle exec jekyll serve --source 2026 --baseurl ""
```

Then visit `http://localhost:4000`.

## Adding a new semester

1. Copy the current year's folder, e.g. `cp -r 2026 2027`.
2. Update `2027/_config.yml`: `baseurl`, `footer_content` year, `syllabus`/`piazza`/`gradescope`/`moodle` links.
3. Update `2027/_staffers/`, `2027/_modules/modules.md`, and the four content pages for the new term.
4. Add a matching build step in `.github/workflows/deploy.yml` (a template comment is left in the "Build 2026 Site" step) and update the root redirect + `2026/index.html`... etc. to point at the new latest year.

## Design

This site intentionally uses a different visual identity than COSI-127B: a teal/amber "circuit board" banner (pure CSS, no image assets — see `_sass/layout.scss` `.banner` and `_includes/components/banner.html`) and a teal accent color (`_sass/color_schemes/light.scss`) instead of COSI-127B's purple/photo banners, to visually distinguish a systems course from the database course.

## Outstanding TODOs before going live

These are marked inline with `<!-- TODO -->` comments in the relevant files:

- [ ] Course description, prerequisites, and learning goals on `2026/index.md` (currently drafted generically — replace with the official syllabus text)
- [ ] Lecture/recitation room numbers on `2026/index.md`
- [ ] Textbook(s) on `2026/resources.md`
- [ ] Real schedule dates/topics in `2026/_modules/modules.md`
- [ ] Piazza / Gradescope / Moodle links and syllabus PDF in `2026/_config.yml` (upload the PDF to `2026/assets/pdf/`)
- [ ] Instructor/TA office hours in `2026/_staffers/`
- [ ] Assignments in `2026/assignments.md`
- [ ] Confirm Late Policy / Contact Policy in `2026/policies.md` (carried over from COSI-127B as a starting point)
