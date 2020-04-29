# Recipe Review
## Rubric Task List

20 tasks (`5 points` each) with 2 extra credit tasks.

### Content First

`5 points`

- [ ] Content Inventory
  - Recipe title
  - Headshot and byline of author
  - Hero photo or illustration (Entice us!)
  - Description list of cooking time and serving size
  - Navigation to sections (Maybe a back to top link too?)
  - Introduction (history, info, etc.)
  - Ingredients list/section
  - Preparation list/section
  - _Optional_ photos or illustrations to show steps or final presentation of the recipe
  - About the author section (Maybe link byline to about section?)

### Layout

`5 points`

- [ ] Responsive Design
  - Use of a mobile first, single-column layout (for small screens)
  - Use of a media query `@media` for wide-to-wider, multi-column layout (for laptop and desktop screens)

### Markup & Style

`45 points`

- [ ] Use of lowercase alphabet for all markup, style, and file/folder names (also `class`, `id`, and file/folder names should not include spaces, instead use a hyphen `-` or an underscore `_` in place of a space).
  - For example: `<section id="Sauce Preparation">` instead of `<section id="sauce-preparation">`; `main.css` instead of `Main.CSS`
- [ ] Use of semantic section (`header`, `nav`, `section`, etc.) and semantic text-level elements (`strong`, `em`, `time`, etc.)
- [ ] Use of proper [typographical characters](http://htmlarrows.com) for fractions, punctuation, symbols, etc. (Use human-readable characters only, not the code/entity; for example: Use `½`, instead of `1/2` [faux fraction] or `&frac12;` [code/entity])
  - See HTML5 Doctor’s [HTML5 Element Index](http://html5doctor.com/#glossary)
- [ ] Use of `<link>` element for external style sheets and canonical content
  - `<link rel="stylesheet" href="css/main.css">` to link an external style sheet
  - `<link rel="canonical" href="https://www.bonappetit.com/recipe/basic-crepes">` for search engines to index the original source of content
- [ ] Use of [accessible colors](https://accessible-colors.com) contrast ratios with a [cohesive color palette](https://www.smashingmagazine.com/2016/04/web-developer-guide-color/) throughout the page for typography, borders, background colors, links, and imagery
- [ ] Use of basic [typographic](https://cssreference.io/typography/) and [box model layout](https://cssreference.io/box-model/) (focusing on `padding`, `border`, and `margin`) styles
- [ ] Use of [web safe fonts](https://www.fonts.com/content/learning/fyti/using-type-tools/fonts-on-the-web)
  - See [CSS font stacks](http://www.cssfontstack.com) for fallback replacements
- [ ] Use of similar `font-size` for paragraphs (`<p>`) and navigation list items (`<li>`) for readability
- [ ] Use of `:hover`, `:focus`, and `:active` [interactive state styles](https://css-tricks.com/css-basics-styling-links-like-boss/) for all links
  - We can do better than default blue links — _please…_ Thank-you!

### Images

`20 points`

- [ ] Use of `<img>` element with the following attributes:
  - `alt` defines meaningful alternative text (alt text)
    - See [When writing alt text, ask yourself this question](https://www.centercentre.com/2016/06/09/2016-06-09-when-writing-alt-text-ask-yourself-this-question/)
  - `src` defines the default image (or fallback image when the `srcset` attribute is also in use)
    -  For example: JPG and PNG has [wide browser support](https://caniuse.com/#feat=png-alpha)
  - `srcset` (_optional_ attribute for SVG or various JPG or PNG images at different widths) defines the set of images we will allow the browser to choose between and what size each image is
    - See [Responsive Images the Simple Way](https://cloudfour.com/thinks/responsive-images-the-simple-way/) for details
    - Support: SVG has [partial browser support](https://caniuse.com/#feat=svg-img) and should not be used as a default image format
  - `width` and `height` defines the intrinsic width and height of an image
    - See [Setting Height and Width on Images is Important Again](https://www.smashingmagazine.com/2020/03/setting-height-width-images-important-again/)
- [ ] Use of fluid, flexible, [responsive images](https://alistapart.com/article/fluid-images/) CSS
  - For example:
  ```
  img {
    width: auto;
    max-width: 100%;
    height: auto;
  }
  ```
- [ ] Save images for the web as a JPG (photographs), PNG and SVG (illustrations),
  - Save bitmap (raster) images using Photoshop, export `Save for Web (Legacy)…` photographs as a JPG (`.jpg`) using the preset `JPEG High` or `JPEG Medium` (depending on quality and file size) and illustrations as a PNG (`.png`) using the preset `PNG-8 128 Dithered` (less colors [max 256]) or `PNG-24` (more colors [millions])
  - Save vector images, illustration and typography-based artwork, using Illustrator, `Save As…` > `SVG` (`.svg`)
    - When using SVG use the `src` (to embed the `.png`) and `srcset` (to embed the `.svg`) attributes for providing fallback and future-friendly image formats
      - For example: `<img alt="A short description of what I should be seeing here." src="img/artwork.png" srcset="img/artwork.svg">`
- [ ] Optimize all images using [ImageOptim](https://imageoptim.com/mac), [Squoosh](https://squoosh.app) (web-based) or similar software for [Windows](https://sourceforge.net/projects/nikkhokkho/) and/or [SVGOMG!](https://jakearchibald.github.io/svgomg/) for SVG
  -  Note: Ideal file size per image should be under `200 KB`

### Validation

`15 points`

- [ ] [Validate HTML](https://validator.w3.org/nu/) (No errors; warnings are ok, but try to resolve)
- [ ] [Validate CSS](http://jigsaw.w3.org/css-validator/) (No errors; warnings are ok, but try to resolve)
- [ ] [Test My Site](https://web.dev/measure/) (Score a 100 in both the Performance and Accessibility categories)

### Git Organized

`10 points`

Remember to use lowercase naming…

- [ ] Repo should contain only essential files:
  - `index.html`
  - `css` (folder containing an external stylesheet)
    - For example: `main.css`
  - `img` (folder containing images)
    - For example: `yummy-cakes.jpg`
  - `wip` (_optional_ folder containing work in progress files, from original artwork to test pages)
  - `README.md`
    - Update this file with a proper heading (title) and paragraph (description)
    - Markdown [basics](http://daringfireball.net/projects/markdown/basics) and [dingus](http://daringfireball.net/projects/markdown/dingus)
- [ ] Add a [description and URL](https://i.imgur.com/CexeWBQ.gif) to your GitHub repo
  - Example description: A tasty HTML & CSS recipe.
  - Example URL: [https://jgagne.github.io/recipe-markup](https://jgagne.github.io/recipe-markup)


### Extra Credit

`10 points`

- [ ] Use of original artwork (photography, illustration, etc.) with inclusion of credit byline
  - Credit byline example: `<figcaption class="photo-credit">`Photo by Jane Doe`</figcaption>`
- [ ] Use of one or more web fonts via Google fonts
