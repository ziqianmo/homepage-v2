# Ziqian Mo — Academic Homepage (Jekyll / AcadHomepage)

Jekyll academic homepage for [Ziqian Mo (莫子谦)](https://ziqianmo.github.io/homepage-v2/), based on [AcadHomepage](https://github.com/RayeRen/acad-homepage.github.io).

This repository is published as a **GitHub Project site** at:

**https://ziqianmo.github.io/homepage-v2/**

The previous Apple-inspired static site from `homepage-v2` is preserved on branch `backup/static-v2-before-swap`.

## Local preview

```bash
bundle install
bundle exec jekyll serve --livereload --baseurl ""
# open http://127.0.0.1:4000/
```

To preview with the production subpath:

```bash
bundle exec jekyll serve --baseurl "/homepage-v2"
# open http://127.0.0.1:4000/homepage-v2/
```

## GitHub Pages configuration

After merging, ensure **Settings → Pages**:

| Setting | Value |
| --- | --- |
| **Build and deployment → Source** | **GitHub Actions** (not “Deploy from a branch”) |
| **Custom domain** | *(empty)* |

The workflow [`.github/workflows/pages.yml`](.github/workflows/pages.yml) builds with Jekyll (`github-pages` gem) and deploys via `actions/deploy-pages`.

`/_config.yml` sets `url: https://ziqianmo.github.io` and `baseurl: /homepage-v2` for correct asset and canonical URLs on the project path.

## Google Scholar crawler

Optional workflow [`.github/workflows/google_scholar_crawler.yaml`](.github/workflows/google_scholar_crawler.yaml) from the original user-site repo; configure secrets if you use it.
