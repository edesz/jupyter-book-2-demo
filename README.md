# Jupyter Book 2 Demo Project

> A demo is a limited functionality version of a software designed to let users experience features, test performance, and gauge interest before using the full version. A demo is limited to a certain stage of adoption of the software. Demos typically feature a specific level of adjustable controls, allowing users to try experience the capabilities of the software.

## About

A starter project to begin publishing with Jupyter Book 2. Go from a collection of documents to somethng (an onlne book) that can be browsed much more naturally.

## Getting Started

### Pre-Requisites

1. [Python](https://www.python.org/)
2. [Pixi](https://pixi.prefix.dev/latest/) for package management

### Installation and Development

1. Clone the Github repository
   ```bash
   git clone https://github.com/edesz/jupyter-book-2-demo.git
   ```
2. Create virtual environment for literate programming using Jupyterlab and start the server
   ```bash
   pixi run jlab
   ```

   This command runs a Jupyterlab server and launches the web user interface in the default browser. The site will be available at http://localhost:8888.
3. After notebooks and project scoping Markdown files in `references` are ready, build Jupyter Book
   ```bash
   pixi run jb-build
   ```
4. Start the Jupyter Book server on port 8080
   ```bash
   pixi run jb-start
   ```
5. Delete Jupyter Book local build artifacts
   ```bash
   pixi run jb-clean
   ```
6. (optional) Create Jupyter Book Github Action, for deployment to Github Pages
   ```bash
   pixi run jb-init-gh-pages
   ```

   which will over-write the existing Github Action configuration file at `.github/workflows/deploy.yml`.
7. (optional) Enable GitHub Pages on the Github repository, and [set its source to GitHub Actions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow)

### Available Commands

Run

```bash
pixi task list
```

to see all available tasks

```bash
Tasks that can run on this machine:
-----------------------------------
jb-build, jb-clean, jb-init-gh-pages, jb-start, jlab
Task              Description
jb-build          Build Jupyter Book HTML version
jb-clean          Clean Jupyter Book static HTML content and cache
jb-init-gh-pages  Create a GitHub Action to deploy Jupyter Book HTML
jb-start          Start Jupyter Book Server
jlab              Launch Jupyterlab
```

## Community

Contributions are very welcome! If you encounter any problems, please [file an issue](https://github.com/edesz/jupyter-book-2-demo/issues) along with a detailed description.

You can also support the development of this project by volunteering to become a maintainer, which means you will be able to triage issues, merge pull-requests, and publish new releases. If you're interested, please submit a pull-request to add yourself to the list of maintainers and we'll get you started! 📘

Please note that **jupyter-book-2-demo** is released with a [Contributor Code of Conduct](https://github.com/edesz/jupyter-book-2-demo/blob/main/CODE_OF_CONDUCT.md). By participating in this project you agree to abide by its terms.

## License

Distributed under the terms of the [MIT license](https://opensource.org/license/mit), [jupyter-book-2-demo](https://github.com/edesz/credit-card-churn/issues) is free and open source software.
