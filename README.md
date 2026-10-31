# Minseop Shin — Academic Website Prototype

An editable, responsive Jekyll website with a minimalist lavender-blue palette inspired by [Chaewon Moon's academic homepage](https://chae1m.github.io/). This implementation is independently authored.

**This is a draft, not a validated professional CV.** Please review personal and academic details before publicizing it. The notes section includes a clearly marked demonstration article.

## Edit information

| Field | File |
| --- | --- |
| Bio, contact, education, experience and links | `_data/profile.yml` |
| Publications and preprints | `_data/publications.yml` |
| Research interests | `_data/research.yml` |
| Articles and mathematical notes | `_posts/YYYY-MM-DD-title.md` |
| Color scheme, typography and layout | `assets/css/style.css` |
| Homepage structure | `index.html` |

The homepage and printable web CV at `/cv/` read the same YAML data files. An external LaTeX CV is **not** automatically parsed by this prototype.

## Deployment

The repository is presently named `MSShin03.github.io.` **including the extra final period**. GitHub Pages ordinarily requires precisely `MSShin03.github.io` (without that trailing period) to serve the user homepage at `https://msshin03.github.io/`.

To publish as a user homepage:

1. Rename the repository to exactly `MSShin03.github.io` in GitHub Settings → General.
2. Change `baseurl: "/MSShin03.github.io."` to `baseurl: ""` in `_config.yml`. Keep `url: "https://msshin03.github.io"`.
3. In Settings → Pages, set **Deploy from a branch**, `main`, `/(root)`.
4. Wait for a successful Pages build and then visit `https://msshin03.github.io/`.

For local preview: install Ruby and Bundler, then run `bundle install` and `bundle exec jekyll serve`.

## Prototype limitations

Education and experience details, email, public links, workshop information, and research summaries still require personal review. The demo math note is not presented as a published article. A printable CV is provided, but no actual CV PDF has been uploaded.
