# Article Rework
## Rubric Task List

20 tasks (`5 points` each) with 2 extra credit tasks.


### Markup & Style

`45 points`

- [ ] Use of lowercase alphabet for all markup, style, and file/folder names (also `class`, `id`, and file/folder names should not include spaces, instead use a hyphen `-` or an underscore `_` in place of a space).
  - For example: `<section id="section-1">` instead of `<section id="Section 1">`; `main.css` instead of `Main.CSS`
- [ ] Use of semantic section (`header`, `nav`, `section`, etc.) and semantic text-level elements (`strong`, `em`, `time`, etc.)
  - See HTML5 Doctor’s [HTML5 Element Index](http://html5doctor.com/#glossary)
- [ ] Use of `<link>` element for external style sheets and canonical content
  - `<link rel="stylesheet" href="css/main.css">` to link an external style sheet
  - `<link rel="canonical" href="http://…">` for search engines to index the original source of content
- [ ] Use of [accessible colors](https://accessible-colors.com) contrast ratios with a [cohesive color palette](https://www.smashingmagazine.com/2016/04/web-developer-guide-color/) throughout the page, from artwork to links
- [ ] Use of `:hover`, `:focus`, and `:active` [interactive state styles](https://css-tricks.com/css-basics-styling-links-like-boss/) for all links
- [ ] Use of basic [typographic](https://cssreference.io/typography/) and [box model layout](https://cssreference.io/box-model/) (focusing on `padding`, `border`, and `margin`) styles
- [ ] Use of [web safe fonts](https://www.fonts.com/content/learning/fyti/using-type-tools/fonts-on-the-web)
  - See [CSS font stacks](http://www.cssfontstack.com) for fallback replacements
- [ ] Use of similar `font-size` for paragraphs (`<p>`) and navigation list items (`<li>`) for readability
- [ ] Use of fluid, flexible, [responsive images](https://alistapart.com/article/fluid-images/) CSS
  - For example:
  ```
  img {
    width: auto;
    max-width: 100%;
    height: auto;
  }
  ```

### Artwork

`20 points`

- [ ] Create vector-based artwork (Illustrator, Sketch, etc.) with a 2:3 (4:6) aspect ratio
  - For example: 1920 x 1280
- [ ] Save artwork as PNG and SVG
  - Save as PNG; (PNG-128) at 1920 x 1280, but no larger than 2048 x 1365
    - <details>
      <summary>Export and Save for Web (Legacy…)</summary>

      ![Illustrator PNG Save Settings](https://user-images.githubusercontent.com/5142085/77106306-3e384300-69f5-11ea-8678-edb4ce8c85e4.png)

      </details>
  - Save as SVG
    - <details>
      <summary>Save As…</summary>

      ![Illustrator SVG Save Settings](https://user-images.githubusercontent.com/5142085/77106096-f6192080-69f4-11ea-8cb4-8fc55a228a20.png)

      </details>
- [ ] Optimize PNG with ImageOptim
  - <details>
    <summary>Enable these settings in ImageOptim > Preferences…</summary>

    ![ImageOptim Preferences](https://user-images.githubusercontent.com/5142085/77106359-54460380-69f5-11ea-959e-f62514018668.png)

    </details>
- [ ] Use of `<img>` element with the following attributes:
  - `alt` defines meaningful alternative text (alt text)
    - See [When writing alt text, ask yourself this question](https://www.centercentre.com/2016/06/09/2016-06-09-when-writing-alt-text-ask-yourself-this-question/)
  - `src` defines the default image (or fallback image when the `srcset` attribute is also in use)
    -  For example: PNG has [wide browser support](https://caniuse.com/#feat=png-alpha)
  - `srcset` defines the set of images we will allow the browser to choose between and what size each image is
    - For example: SVG has [partial browser support](https://caniuse.com/#feat=svg-img) and should not be used as a default image format
  - `width` and `height` defines the intrinsic width and height of an image
    - See [Setting Height and Width on Images is Important Again](https://www.smashingmagazine.com/2020/03/setting-height-width-images-important-again/)

### SVG

`10 points`

- [ ] Optimize with [SVGOMG](https://jakearchibald.github.io/svgomg/)
  - <details>
    <summary>Use these settings:</summary>

    ![SVGOMG settings](https://user-images.githubusercontent.com/5142085/77106431-72136880-69f5-11ea-9af2-7b185ae12155.png)

    </details>
  - **tl;dr:** Enable all options, then disable these 6 options:
    - Compare gzipped
    - Remove `xlmns`
    - Remove `viewBox`
    - Sort children of `<defs>`
    - Remove `<title>`
    - Remove `<desc>`
  - Note: Feel free to adjust the Precision slider from 0 to 8; 8 being the best quality
- [ ] Post production for better accessibility
  - See [Accessible SVGs](https://a11y-101.com/development/svg) and [production SVG markup](https://raw.githubusercontent.com/jgagne/article-rework/master/img/work-smarter-2020-2048w.svg) for details
    - Add ARIA `role="img"`
    - Remove `width` and `height` attributes; use `viewBox` attribute instead
    - Add `viewBox` attribute; `viewBox="min-x, min-y, width, height"`
      - For example: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1920 1280" role="img">`
    - Add `<title>`Illustration by…`</title>` element
    - Add `<desc>`Alternative text…`</desc>` element

### Validation

`15 points`

- [ ] [Validate HTML](https://validator.w3.org/nu/) (No errors; warnings are ok, but try to resolve)
  - URLs that end with `?` followed by parameter values; the query string can be removed for validation
    - For example: `https://www.nytimes.com/newsletters/smarter-living?module=inline` becomes `https://www.nytimes.com/newsletters/smarter-living`
- [ ] [Validate CSS](http://jigsaw.w3.org/css-validator/) (No errors; warnings are ok, but try to resolve)
- [ ] [Test My Site](https://web.dev/measure/) (Score a 100 in both the Performance and Accessibility categories)

### GitHub

`10 points`

Remember to use lowercase naming…

- [ ] Repo should contain only essential files:
  - `index.html`
  - `css` (folder containing an external stylesheet)
    - For example: `main.css`
  - `img` (folder containing images)
    - For example: `headshot-tim-herrera.jpg`
  - `wip` (_optional_ folder containing work in progress files, from original artwork to test pages)
    - For example: `9780762494125_TimHerrera_EarlWilson.psd`
  - `README.md`
    - Update this file with a proper heading (title) and paragraph (description)
    - Markdown [basics](http://daringfireball.net/projects/markdown/basics) and [dingus](http://daringfireball.net/projects/markdown/dingus)
- [ ] Add a [description and URL](https://i.imgur.com/CexeWBQ.gif) to your GitHub repo
  - Example description: Rework of the New York Times article 8 Ways to Work Smarter in 2020.
  - Example URL: [https://github.com/jgagne/article-rework](https://github.com/jgagne/article-rework)

### Extra Credit

`10 points`

- [ ] Use of mixing `font-weight`, `font-style`, and `text-transform` with one or more fonts for headings, paragraphs, captions, etc.
  - See [Mixing Fonts](https://practicaltypography.com/mixing-fonts.html)
- [ ] Use of jump (skip) links to the `<main>` content, at top and bottom, of the page
  - See [Anchors OK? Re-Assessing In-Page Links](https://www.nngroup.com/articles/in-page-links/)
