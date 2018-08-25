# Simple Reveal.js Examples
Simple examples to illustrate Reveal.js usage for generating course slides.
These examples are currently based on [release 3.6](https://github.com/hakimel/reveal.js/releases/tag/3.6.0) of [Reveal.js](https://revealjs.com/#/).

The files in the `js` and `css` directories are taken from the aforementioned Reveal release. We only include the minimum of these files to enable our examples to work. This way students know the minimum amount of extra files needed for their online presentations.

## Examples

1. `Basic.html` -- Just bullet charts, and such. Does not need anything other than basic `reveal.js`
2. `basicMarkdown.html` -- Shows how to use [Markdown](https://commonmark.org/) internally to the HTML file for processing and rendering. This uses a markdown plugin for Reveal. 
3. `basicCode.html` -- Show how to include code samples with syntax highlighting.
4. `markAndCode.html` -- Show how to use Markdown and code syntax highlighting.

## Examples to be Written

1. Basic with Figures -- especially dealing with captions and figure size issues.
3. The above with markdown.
4. Probably should have "fragments" illustrated in the above. These are things like the incremental rendering of bullets in a bullet list.
5. Maybe external markdown use.

## Issues and Fixes

**Issues #1** For our presentations on technical topics we need a bit more space than the templates seem to assume. One solution that seemed to work is to scale down the font size in the `theme` being used. For example in `theme/white.css` under *global styles* we see:

```
.reveal {
  font-family: "Source Sans Pro", Helvetica, sans-serif;
  font-size: 42px;
  font-weight: normal;
  color: #222; }
```
A modification for smaller (and more text):
```
.reveal {
  font-family: "Source Sans Pro", Helvetica, sans-serif;
  font-size: 36px;
  font-weight: normal;
  color: #222; }
```
