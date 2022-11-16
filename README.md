# About this site

This website code uses [Lume](https://github.com/lumeland/lume) static site generator.

## Getting Started

1. Make sure you have [Deno installed](https://deno.land/#installation) using 
`curl -fsSL https://deno.land/x/install/install.sh | sh`
2. Run Lume locally with `deno task serve`.
3. Use `data-pagefind-body` where you want the search function to index.

## Deployment

### GitHub Pages

As of Oct. 2022 GitHub actions work well for the deployment of this static site if the build.yml is setup correctly.

- [Get your own Lume blog on Github Pages](https://github.com/lumeland/base-blog/generate)
- Open the file `.github/workflows/build.yml` and edit the `--location` option
  with the url of the site, for example
  `--location=https://[username].github.io/[repo]/`
- if the `.github\workflows\build.yml` script successfully builds the site and copies it to a GitHub `gh-pages` branch and you are able to go into the `gh-pages` branch and see you static content then the build action was successful. In GitHub you can now continue with configuring your repository to publish the content of the `gh-pages` branch to your default repository website (which should look like https://[gitUsername].github.io/[repositoryName]/). To publish this website, in your GitHub repository online, go to Settings/Pages/Build and deployment/Source and choose the `Deploy from branch`. Then just below that option choose `gh-pages` as the branch.
- [See a live demo](https://lumeland.github.io/base-bgh-pageslog/) -->

### Deno Deploy

- [Create a project in Deno Deploy](https://deno.com/deploy) and configure it.
  - Link to your git repository
  - Set the GitHub Actions deployment mode.
- Open the file `.github/workflows/deno_deploy.yml` and edit the following:
  - The `--location` option with the url of the site, for example:
    `--location=https://my-blog.deno.dev`
  - The project name in the `denoland/deployctl` step with the name of your
    project.
- [See a live demo](https://lume-blog.deno.dev)
