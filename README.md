# Ruchik Mishra — academic website

Built on [al-folio](https://github.com/alshedivat/al-folio) (Jekyll). Deploys to https://ruchikmishra.github.io.
The theme's original README is in `docs/AL-FOLIO-README.md`.

## Run it locally

Both options need **Docker Desktop** installed and running (https://www.docker.com/products/docker-desktop/).
On Windows, al-folio recommends running Docker through WSL; see `docs/INSTALL.md`.

### Option A: VS Code (recommended)

1. Install the **Dev Containers** extension in VS Code.
2. Open this folder in VS Code (File > Open Folder).
3. When VS Code asks, click **Reopen in Container**. (Or press Ctrl/Cmd+Shift+P and run
   "Dev Containers: Reopen in Container".)
4. The first time takes several minutes while it installs Ruby and Jekyll. When the terminal
   shows `Server running`, open http://localhost:8080.
5. Edit and save any file; the page reloads on its own. Changes to `_config.yml` need a
   restart of the server.

### Option B: terminal

```bash
docker compose pull
docker compose up
```

Then open http://localhost:8080. Stop it with Ctrl+C.

## Where things are

| To change                                     | Edit                                                  |
| --------------------------------------------- | ----------------------------------------------------- |
| Name, site description, settings              | `_config.yml`                                         |
| Bio, office address, photo position           | `_pages/about.md`                                     |
| Photo                                         | `assets/img/prof_pic.jpg`                             |
| Email, Scholar, ORCID, GitHub, LinkedIn       | `_data/socials.yml`                                   |
| Papers (and which ones show on the home page) | `_bibliography/papers.bib`                            |
| Abstracts and posters                         | `_bibliography/posters.bib`                           |
| Paper thumbnails                              | `assets/img/publication_preview/`                     |
| Venue badge colors                            | `_data/venues.yml`                                    |
| News items                                    | `_news/` (one file per item; copy one to add another) |
| TL;DR summary pages                           | `_projects/` (linked from papers via `tldr = {...}`)  |
| Teaching and mentoring                        | `_pages/teaching.md`                                  |
| CV                                            | replace `assets/pdf/Ruchik_CV.pdf` (keep the name)    |
| Menu order                                    | `nav_order` at the top of each file in `_pages/`      |
| Venue badge colors and text color             | `_data/venues.yml`                                    |

## Still to fill in

Search the folder for `TODO` and `DRAFT` (Ctrl/Cmd+Shift+F in VS Code):

- Bio on the about page and the research descriptions are drafts to rewrite
- Exact dates on news items marked TODO
- Abstracts: add `abstract = {...}` to entries in `papers.bib` to get an "Abs" button

## Local customization

`_layouts/bib.liquid` is a copy of al-folio's publication template (from `al_folio_core` 1.0.15) with two
additions: a `text_color` option for venue badges and a `tldr` field that adds a TL;DR button. If you upgrade
al-folio later, compare it with the new version of that file.

## Publishing

Pushing to the `main` branch runs `.github/workflows/deploy.yml`, which builds the site and
puts it on the `gh-pages` branch. In the repo's Settings > Pages, set the source to
"Deploy from a branch", branch `gh-pages`, folder `/ (root)`.
