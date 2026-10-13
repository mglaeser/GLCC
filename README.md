# G.L. Capital & Consulting

[**glcc.berlin ↗**](https://glcc.berlin)

A quiet, monochrome home for G.L. Capital & Consulting. The original GL monogram sits above a changing selection of headlines on artificial intelligence, entrepreneurship and brighter AI.

Each headline fades in, stays for 2.5 seconds and fades out. Its source opens the original article. German headlines are presented as English translations; the linked publications remain the original sources.

## The page

White space, a black SVG monogram and system typography. Everything needed to draw and animate the page lives in `index.html`; there are no libraries, external fonts, trackers or build steps. The existing company details stay at the foot of the page.

The two-line “Capital & Consulting” signature uses Optima letterforms drawn as inline SVG paths, so it looks the same without installing or downloading a font. The visible width of “Consulting” is the original GL mark’s width divided by φ² (approximately 38.2%); placement and line spacing are optically balanced beneath the L. The original monogram paths and monogram-only favicon remain unchanged.

On a fresh visit, white bars rise in a quick left-to-right sequence while the chart glides left on black. They settle at their fixed heights before one bar opens like a hinged plane: four straight edges turn from a narrow perspective into the existing page. The full introduction takes about 1.75 seconds. This short introduction is drawn in inline SVG and driven by a single native JavaScript timeline; it adds no downloads or dependencies. The first headline’s reading time starts after the reveal. Escape or Tab skips the introduction; reduced motion, background visits and restored pages bypass it. If animation setup fails, a short safety timeout releases the ordinary page. All geometry and timing live beside the intro controller in `index.html`.

The headline area keeps a steady height as the text changes. The rotation continues while hovering; focusing a source link still pauses it so keyboard users can open an article comfortably. Inactive tabs pause too; reduced-motion preferences remove the fades. If the article data cannot be loaded, the monogram and company details remain available.

## The selection

[`articles.json`](articles.json) contains the headlines in display order. Each entry has a `title`, a `source` and an HTTPS `link`. The optional `logos` array selects a small, inline monochrome publisher mark. Set `sourceInLogo` to `true` only when the mark spells out the full source name; otherwise the source text remains visible. A missing or unavailable mark always falls back to text, and every link keeps the full source name for assistive technology. Edit this file to update the selection or add another article.

The publisher marks are used beside their corresponding source links. Publisher artwork is embedded locally, with provenance links beside the inline SVG definitions. The monochrome Axel Springer mark is adapted from [Axel Springer / ASUKomm’s SVG](https://commons.wikimedia.org/wiki/File:Logo_Axel_Springer_SE.svg), credited under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). All marks remain the property of their respective owners. The GL monogram also supplies the page’s favicon.

## Home on the web

Hosted on GitHub Pages from `main`, with the custom domain recorded in [`CNAME`](CNAME). The visual rhythm takes its cue from Carmen Tang’s [Fading Testimonials](https://codepen.io/carmentang/pen/egyPZo), implemented here with native CSS and JavaScript.
