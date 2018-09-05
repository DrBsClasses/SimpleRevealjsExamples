# Reveal.js Lecture Examples
Simple examples to illustrate Reveal.js usage for generating course slides.
These examples are currently based on [release 3.6](https://github.com/hakimel/reveal.js/releases/tag/3.6.0) of [Reveal.js](https://revealjs.com/#/), however, we will rename the Reveal release directory from something like `reveal.js-3.6.0` to just `reveal` so that the bulk of our work is independent of version.

Currently in our `reveal` directory is a minimal subset of the Reveal release needed for these demonstrations.

## Directory Structuring

A course will typically contain many topics, lectures will tend to be grouped into these topics, and each lecture may contain supplementary files, images, demonstration code. Hence to avoid a mess of files we group lecture materials into directories that are at the same level as the `reveal` directory. This affects how we reference the Reveal JavaScript and CSS resources from our slides.

We put our examples in the `LectureSlides` directory. You would come up with a descriptive name for your own directory based on the topic of the lecture(s).

## Lecture Slide Examples

In the `LectureSlides` directory you will find:

1. `Basic.html` -- Just bullet charts, and such. Does not need anything other than basic `reveal.js`
2. `basicMarkdown.html` -- Shows how to use [Markdown](https://commonmark.org/) internally to the HTML file for processing and rendering. This uses a markdown plugin for Reveal. 
3. `basicCode.html` -- Show how to include code samples with syntax highlighting.
4. `markAndCode.html` -- Show how to use Markdown and code syntax highlighting.

## Examples to be Written

1. Basic with Figures -- especially dealing with captions and figure size issues.
2. The above with markdown.
3. Probably should have "fragments" illustrated in the above. These are things like the incremental rendering of bullets in a bullet list.
4. Maybe external markdown use.

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
