# Jupyter Book 2 Demo Project

> A demo is a limited functionality version of a software designed to let users experience features, test performance, and gauge interest before using the full version. A demo is limited to a certain stage of adoption of the software. Demos typically feature a specific level of adjustable controls, allowing users to experience a limited subset of the capabilities of the software.

## About

A starter project to begin publishing with Jupyter Book 2.

This allows to go from a collection of Markdown and Jupyter Notebook documents to somethng (e.g. an online book) that can be browsed much more naturally.

All notebooks and Markdown files are used as-is in the online book version.

## Getting Started

### Pre-Requisites

1. [Python](https://www.python.org/)
2. [Pixi](https://pixi.prefix.dev/latest/) for package management

### Installation and Usage

1. Clone the Github repository
   ```bash
   git clone https://github.com/edesz/jupyter-book-2-demo.git
   ```
2. Start Jupyterlab for literate programming
   ```bash
   make jlab
   ```

   This command runs a Jupyterlab server and launches the web user interface in the default browser. The site will be available at http://localhost:8888.
3. Create and finalize Jupyter notebooks the `notebooks` folder and project scoping Markdown files in the `references` folder
4. Build the Jupyter Book
   ```bash
   make jb-build
   ```
5. Start the Jupyter Book server on a custom port (8081)
   ```bash
   make jb-start
   ```
6. Delete Jupyter Book local build artifacts
   ```bash
   make jb-clean
   ```
7. (optional) Create Jupyter Book Github Action, for deployment to Github Pages
   ```bash
   make jb-init-gh-pages
   ```

   The existing Github Action configuration file is the default one provided by following the [Jupyter Book 2 deployment instructions](https://jupyterbook.org/stable/get-started/publish/#github-pages) with a change required to [automatically add the updated date](https://jupyter-book.github.io/myst-plugins/page-last-updated/). If any changes were made to the default configuration, then running this command will over-write that Github Action configuration file at `.github/workflows/deploy_book.yml`.
8. (optional) Enable GitHub Pages on the Github repository, and [set its source to GitHub Actions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow)

Every command from above creates a virtual environment and installs the Python package(s) required to perform the relevant action into that environment.

### Available Commands

Run

```bash
make help
```

to see all available [`make` targets](https://www.gnu.org/software/make/manual/make.html#Phony-Targets)

```bash
Available rules:

jb-build            Build Jupyter Book HTML version 
jb-clean            Clean Jupyter Book HTML content and cache 
jb-init-gh-pages    Create a GitHub Action to deploy Jupyter Book 
jb-start            Start Jupyter Book server 
jlab                Run Jupyterlab 
p2c                 Export pixi environment to conda
```

## Community

Contributions are very welcome! If you encounter any problems, please [file an issue](https://github.com/edesz/jupyter-book-2-demo/issues) along with a detailed description.

You can also support the development of this project by volunteering to become a maintainer, which means you will be able to triage issues, merge pull-requests, and publish new releases. If you're interested, please submit a pull-request to add yourself to the list of maintainers and we'll get you started! 📘

Please note that **jupyter-book-2-demo** is released with a [Contributor Code of Conduct](https://github.com/edesz/jupyter-book-2-demo/blob/main/CODE_OF_CONDUCT.md). By participating in this project you agree to abide by its terms.

## License

Distributed under the terms of the [MIT license](https://opensource.org/license/mit), [jupyter-book-2-demo](https://github.com/edesz/credit-card-churn/issues) is free and open source software.
