# Sarah Kittrell – Technical writing portfolio

This repository contains the source for my technical writing portfolio, built with [Zensical](https://zensical.org/) and published with GitHub Pages.

## Browse the samples

Each sample page includes the audience, my role, and how I verified the content:

- [Content strategy](docs/samples/content-strategy/)
- [API documentation and standards](docs/samples/api/)
- [Training](docs/samples/training/)
- [Release notes](docs/samples/release-notes/)
- [Online help](docs/samples/online-help/)

## Repository structure

The repository follows the standard Zensical layout:

| Path | Contents |
| --- | --- |
| `mkdocs.yml` | Site settings, theme, and navigation |
| `docs/` | Markdown pages for the site |
| `docs/assets/files/` | PDFs linked from sample pages |
| `docs/assets/images/` | Screenshots and slide images |
| `docs/samples/online-help/help/` | RoboHelp output, published as is |
| `.github/workflows/docs.yml` | Builds and publishes the site on every push to `main` |

## Build the site locally

To preview the site on your computer, do the following:

1. In a terminal, install Zensical:

    ```
    pip install zensical
    ```

2. In the repository folder, start the preview server:

    ```
    zensical serve
    ```

3. In a browser, open `http://localhost:8000`.

## Publish changes

The site publishes automatically. When you push a commit to the `main` branch, the GitHub Actions workflow builds the site and deploys it to GitHub Pages.
