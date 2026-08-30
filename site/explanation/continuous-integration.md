---
title: Continuous Integration
layout: default
parent: Explanation
nav_order: 2
---

# Continuous Integration
{: .no_toc }

This repository leverages [GitHub Actions] to automate the "{{ site.title }}" documentation site's deployment.
{: .fs-6 .fw-300 }

With each push to the `main` branch, the workflow defined in the `.github/workflows/` directory is triggered to
build and publish the site.

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Pages workflow

To publish your software documentation to GitHub Pages, configure your repository by following the steps in
[Publishing with a custom GitHub Actions workflow].

After the configuration is complete, the [`.github/workflows/pages.yml`]({{ site.github.repository_url }}/blob/main/.github/workflows/pages.yml) workflow will automatically build and deploy the
documentation site to GitHub Pages whenever changes under the [`site/`]({{ site.github.repository_url }}/tree/main/site) directory are pushed to the `main` branch.

[GitHub Actions]: https://docs.github.com/en/actions

[Publishing with a custom GitHub Actions workflow]: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow
