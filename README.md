# Bullish Ideas

Bullish Ideas publishes early concepts, experiments, and writing about design
and technology. The site treats proposals as ideas to examine, not as completed
projects.

## Site structure

- content/_index.md sets the homepage sections and introduction.
- content/about/ and content/contact/ hold the main information pages.
- content/portfolio/ holds ideas and essays for Roxo Flex cards.
- .siteman/layouts/baseof.html adds canonical and social metadata.
- static/images/ holds the original mark, editorial artwork, and social card.
- .siteman/hugo.toml sets the theme, palette, navigation, and site metadata.

The theme expects cards in a portfolio section. Each idea page sets its own
public URL under /ideas/. The section index uses /ideas/ as its URL.

## Editorial content

Add a Markdown file to content/portfolio/ for each idea or essay. Set its
title, description, image, image alternative text, weight, and public URL in
front matter. Mark each piece as an essay or working idea in its opening
paragraph. State its premise and give readers details they can use.

Do not describe a proposal as a finished product or project. Keep claims tied
to the evidence in the piece.

## Theme and visual settings

The site loads github.com/Bullish-Design/roxo-flex before siteman-default.
The first theme supplies the page structure and cards. The fallback supplies
templates that Roxo Flex does not define.

The palette uses pale paper (#F6F2E8), charcoal text (#242724), and ochre
(#805500). Charcoal has 13.51:1 contrast on paper. Muted text has 6.24:1.
Ochre has 5.84:1 on paper and 5.40:1 on the surface color. White has 6.53:1
on ochre.

## Local verification

Run these commands from the repository root:

```sh
devenv shell -- siteman-serve
devenv shell -- siteman-build
devenv shell -- siteman-check
```

The build writes the site to public/. The check also validates Markdown,
prose, local links, and the GitHub Pages workflow.

## Deployment

The workflow deploys on each push to main. Add the SITEMAN_READ_TOKEN Actions
secret with read access to Bullish-Design/siteman. Set the Pages source to
GitHub Actions. The token lets Nix fetch the private siteman module.
