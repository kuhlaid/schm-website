# About this site

This website code uses [Lume](https://github.com/lumeland/lume) static site generator.

## Getting Started

1. Make sure you have [Deno installed](https://deno.land/#installation) using 
`curl -fsSL https://deno.land/x/install/install.sh | sh`
2. Run Lume locally with `deno task serve`.
3. In any of the static pages where you want the search function to index, use `data-pagefind-body` (such as page.njk)

## Deployment

### GitHub Pages

Could not figure out how to best setup GitHub actions to build Lume against a custom domain (and rebuild the site witout breaking the pages) so switching to Netlify for hosting.
