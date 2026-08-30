# Code Smells — Learning Hour

A [Learning Hour] on code smells: recognizing them, classifying them, and knowing which refactoring resolves
each one.

This repository is generated from the [learning-hour-template] and includes:

- A [Jekyll] site configured with the [Just the Docs] theme, located in the `site` folder
- A copy of the [Creative Commons Attribution-ShareAlike 4.0 International License](LICENSE-CC-BY-SA-4.0) in the
  repository root. This license applies to all site documentation content
- A [GitHub Actions workflow] in the `.github/workflows` folder to build and deploy the site to GitHub Pages
- A Notice file for third-party attributions in the repository root

## Getting started

1. Go to Settings > Pages > Build and deployment > Source, and select GitHub Actions to serve the `site` folder
2. See [site/index.md](site/index.md) for the Learning Hour agenda

## GitHub Actions Workflows

- **Site Deployment:** `.github/workflows/pages.yml` builds and deploys the documentation site to GitHub Pages.

## Building and previewing your site locally

Assuming [Jekyll] and [Bundler] are installed on your computer:

1. Change your working directory to the root directory of your site.
2. Run `bundle install`.
3. Run `bundle exec jekyll serve` to build your site and preview it at `localhost:4000`.

Alternatively, run `./site/start_local_server.sh` from anywhere in the repository. It installs any missing
gem dependencies and serves the site with live reload at `localhost:4000`.

The built site is stored in the directory `site/_site`.

## Licensing and Attribution

This repository uses the [Just the Docs] theme for static site generation. A copy of their [MIT License] is included in
the `site/` folder.

The deployment GitHub Actions workflow is heavily based on GitHub's mixed-party [starter workflows]. A copy of their MIT
License is available in [actions/starter-workflows].

All documentation content within the `site/` folder is licensed under
the [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) License].

You are generally free to reuse or extend upon the code in this repository as you see fit, provided you comply with the
terms of the respective licenses for the code and documentation.



[Jekyll]: https://jekyllrb.com
[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[Learning Hour]: https://sammancoaching.org/reference/learning_hour_definition.html
[learning-hour-template]: https://github.com/ibanFR/learning-hour-template
[GitHub Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[Bundler]: https://bundler.io
[MIT License]: https://en.wikipedia.org/wiki/MIT_License
[starter workflows]: https://github.com/actions/starter-workflows/blob/main/pages/jekyll.yml
[actions/starter-workflows]: https://github.com/actions/starter-workflows/blob/main/LICENSE
[Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) License]: https://creativecommons.org/licenses/by-sa/4.0/
