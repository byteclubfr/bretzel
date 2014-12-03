# Bretzel

Convert an ordered collection of markdown files into a PDF.

Ideal to easily generate books or slides.

## Usage

Create a directory containing .md files with *exactly* 3 leading numbers :

* book/001 Great introduction.md
* book/002 Fantastic story.md
* book/003 Tragic ending.md

Then run `gulp --src book`

And magic! You get a nice book.pdf

### Tree variants

You can have holes in the ordering, the header counter is adjusted for you at rendering time :

* book/001 Great introduction.md
* book/042 Fantastic story.md
* book/210 Epilogue.md
* book/211 Tragic ending.md

Subdirectories let you regroup similar pages by topic :

* book/01 - Middle Ages/001 Huge Battle.md
* book/01 - Middle Ages/003 Tall Castle.md
* book/02 - Victorian Times/001 Steam Machine.md
* book/02 - Victorian Times/345 Magic Train.md

When unsure about the ouput result, look at the feedback given on stdout.

### Add a title in the header of each pages

`DOC_TITLE="My wonderful title" gulp --src book`

See system.env.DOC_TITLE inside runnings.js

### Options

* **Format**
  * landscape : `--orientation=landscape`
  * portrait (default) : `--orientation=portrait`
* **Disable automatic title**
  * `--no-auto-h1`
  * Note : in this case you need to add H1 tags on each page.

### Markdown support

* `Github Flavored Markdown` is used for syntax highlighting.
* Intentional page-break are triggered by adding `…/…` or `.../...` to the document.
