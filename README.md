# G.L. Capital & Consulting

[**glcc.berlin ↗**](https://glcc.berlin)

A quiet, monochrome home for G.L. Capital & Consulting. The original GL monogram sits above a changing selection of headlines on artificial intelligence, entrepreneurship and brighter AI.

Each headline fades in, stays for three seconds and fades out. Its source opens the original article. German headlines are presented as English translations; the linked publications remain the original sources. The Washington Post item is identified as BrandStudio content.

## The page

White space, a black SVG monogram and system typography. Everything needed to draw and animate the page lives in `index.html`; there are no libraries, external fonts, trackers or build steps. The existing company details stay at the foot of the page.

The headline area keeps a steady height as the text changes. Hovering over it or focusing a source link pauses the rotation so an article can be opened comfortably. Inactive tabs pause too; reduced-motion preferences remove the fades. If the article data cannot be loaded, the monogram and company details remain available.

## The selection

[`articles.json`](articles.json) contains the headlines in display order. Each entry has a `title`, a `source` and an HTTPS `link`. The optional `logos` array selects a small, inline monochrome publisher mark; an empty array shows the source as text only. Edit this file to update the selection or add another article.

The publisher marks are used beside their corresponding source links. Publisher artwork is embedded locally, with provenance links beside the inline SVG definitions. The monochrome Axel Springer mark is adapted from [Axel Springer / ASUKomm’s SVG](https://commons.wikimedia.org/wiki/File:Logo_Axel_Springer_SE.svg), credited under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). All marks remain the property of their respective owners. The GL monogram also supplies the page’s favicon.

## Home on the web

Hosted on GitHub Pages from `main`, with the custom domain recorded in [`CNAME`](CNAME). The visual rhythm takes its cue from Carmen Tang’s [Fading Testimonials](https://codepen.io/carmentang/pen/egyPZo), implemented here with native CSS and JavaScript.
