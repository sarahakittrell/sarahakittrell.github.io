# About this site

This page describes how I built and publish this portfolio, using a docs-as-code workflow.

## Tools

The site uses the following tools:

- **Zensical** builds the site from Markdown files.
- **Git and GitHub** store the source and track changes.
- **GitHub Actions** builds the site on every push to the main branch.
- **GitHub Pages** hosts the published site.

## Workflow

Each update follows the same steps:

1. I edit Markdown pages in Visual Studio Code and preview them locally.
2. I commit the changes and push them to GitHub.
3. A GitHub Actions workflow builds the site and deploys it to GitHub Pages.

## Problems I solved

- **Build tool compatibility:** Zensical wouldn’t install on the newest version of Python, because one of its components wasn’t yet available for that version. I installed an earlier supported version of Python and set up a virtual environment for the project, which keeps the site’s tools separate from the rest of my computer and gives me the same setup every time I preview the site.
- **Choosing a supported build tool:** I started with Material for MkDocs, a widely used theme for documentation sites. While setting up the project, I found that Material had reached the end of its maintenance period, so I switched to Zensical, its successor from the same team. Zensical reads the same configuration file, so the switch didn’t require restructuring the site.
- **Embedding a legacy help system:** One sample is a help system built in Adobe RoboHelp, which has its own navigation, search, and stylesheet. Rather than converting it to Markdown, I published the RoboHelp output inside the site as is, so it works the way it did for customers. An intro page gives the sample’s context and opens the help system in a new tab.