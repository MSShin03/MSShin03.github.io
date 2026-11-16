# Minseop Shin — Academic Website Prototype

An editable, responsive Jekyll website with a **blue, dark ink, and white** palette (with original layout inspiration from [Chaewon Moon's academic homepage](https://chae1m.github.io/)). This implementation is independently authored.

**This is a draft, not a validated professional CV.** Please review personal and academic details before publicizing it. The Notes section and navigation link are automatically hidden when no posts exist.

## Edit information

| Field | File |
| --- | --- |
| Bio, contact, education, experience and links | `_data/profile.yml` |
| Publications and preprints | `_data/publications.yml` |
| Research interests | `_data/research.yml` |
| Articles and mathematical notes | `_posts/YYYY-MM-DD-title.md` |
| Color scheme, typography and layout | `assets/css/style.css` |
| Profile portrait | `assets/img/profile.webp` |
| Homepage structure | `index.html` |

The homepage and printable web CV at `/cv/` read the same YAML data files. An external LaTeX CV is **not** automatically parsed by this prototype.

## Deployment

This repository is named `MSShin03.github.io` (without a trailing period), and its Jekyll `baseurl` is empty. It is configured for the homepage at **https://msshin03.github.io/**.

To publish updates, commit changes to the `main` branch. GitHub Pages rebuilds automatically; check **Actions → pages build and deployment** for status.

To preview locally, install Ruby and Bundler and run `bundle install` followed by `bundle exec jekyll serve`.

## Profile image and section headings

The homepage currently uses the owner-supplied JPEG at `assets/img/1712297899143.jpg`. To replace it, upload a new photo and update the source path in `index.html`.

The homepage now returns to the uploaded reference's serif typography and two-column section layout: grey section numbers only on the left, with descriptive titles on the right. The original reference's content width and section/hero spacing are restored. Colors remain white, sky blue, and dark ink. Notes numbering remains automatic.

The hero's Google Scholar and LinkedIn icons temporarily point to **name searches**, not verified personal profiles. Add your actual URLs under `links.google_scholar` and `links.linkedin` in `_data/profile.yml`; the icon links update automatically. The email icon uses the configured address.

## Prototype limitations

Education and experience details, email, public links, workshop information, and research summaries still require personal review. A printable CV is provided, but no actual CV PDF has been uploaded.

## Notes visibility

The homepage Notes section, its surrounding divider, and the Notes navigation link are automatically hidden when `site.posts.size == 0`. When a valid Jekyll post is added under `_posts/`, they appear automatically on the next successful build. The `/notes/` page displays an empty state if visited directly while there are no posts.
