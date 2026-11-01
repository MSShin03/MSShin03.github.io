# Minseop Shin — Academic Website Prototype

An editable, responsive Jekyll website with a minimalist **Fresh Teal** color palette (with original layout inspiration from [Chaewon Moon's academic homepage](https://chae1m.github.io/)). This implementation is independently authored.

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

The hero portrait is a compressed WebP version of the owner-supplied photograph, kept in `assets/img/profile.webp`. To replace it, upload a new file at that path, or change the image path in `index.html`.

Section labels (for example, "01 / About me") sit above their headings in the main content column. Heading colors and typography can be adjusted in `assets/css/style.css`. The Fresh Teal palette uses `#20A69B` for decorative highlights, `#0B7169` for high-contrast links and buttons, `#FAFDFC` for the page background, and `#D9F4ED` for light accents. Change the `:root` CSS variables to customize it. Headings remain dark, non-italic text.

## Prototype limitations

Education and experience details, email, public links, workshop information, and research summaries still require personal review. A printable CV is provided, but no actual CV PDF has been uploaded.

## Notes visibility

The homepage Notes section, its surrounding divider, and the Notes navigation link are automatically hidden when `site.posts.size == 0`. When a valid Jekyll post is added under `_posts/`, they appear automatically on the next successful build. The `/notes/` page displays an empty state if visited directly while there are no posts.
