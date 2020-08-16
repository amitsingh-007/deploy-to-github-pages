# GitHub Action: Deploy React code to GitHub Pages

GitHub action to automate the process of deploying your code to GitHub Pages.
Use only if you want deploy React code to GitHub Pages. It deploys `/build` folder to branch named `gh-pages`.

## Inputs

None

## Example workflow

```yaml
name: Deploy to Github Pages

on: push

jobs:
  deploy:
    name: Deploying to Github Pages

    runs-on: ubuntu-latest

    steps:
      - name: Checkout branch
        uses: actions/checkout@v2

      - name: Authorizing Github action
        with:
          token: "${{ secrets.GITHUB_TOKEN }}"
        uses: oleksiyrudenko/gha-git-credentials@v1

      - name: Doploy to GitHub Pages
        uses: amitsingh-007/deploy-to-github-pages@v1.1
```
