
---
title: Github Workflow
author: kokic
date: 2025-1-15
---

一个可供参考的 Github Workflow 配置 [^hongjr03-workflow] 如下. 
唯一需要注意的是环境变量 `$PAGE_URL`, 用于 [指定待部署页面的 URL](/tutorials/compile), 
你可以在仓库的 `settings/variables/actions` 设置 [它们](https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/store-information-in-variables). 

```
name: Deploy Kodama site to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches: ["main"]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
concurrency:
  group: "pages"
  cancel-in-progress: false

# Default to bash
defaults:
  run:
    shell: bash

jobs:
  # Build job
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Install Kodama & Typst
        run: |
          cargo install --git https://github.com/kokic/kodama.git
          sudo snap install typst
      - name: Checkout
        uses: actions/checkout@v4
        with:
          submodules: recursive
      - name: Setup Pages
        id: pages
        uses: actions/configure-pages@v5
      - name: Build with Kodama
        run: |
          kodama c index.md -b=$PAGE_URL
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./publish

# Deployment job
  deploy:
    environment:
      name: github-pages
      url: $PAGE_URL
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

[^hongjr03-workflow]: 由 [Hong Jiarong](https://github.com/hongjr03) 提供. 
