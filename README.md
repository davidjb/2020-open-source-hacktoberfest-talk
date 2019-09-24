# History of (an) emoji

A lightning talk presented at DevNQ.

Slides PDF: <https://github.com/davidjb/2019-devnq-devs-alive/raw/master/slides-web.pdf>

## Setup

```bash
yarn
yarn start
```

This starts the presentation server at <http://localhost:8080> and
automatically opens a browser.

## Creating a PDF

```bash
yarn pdf
```

Look for the `.pdf` file in the current directory.  To optimise the file for the web:

```bash
brew install ghostscript
yarn optimise-pdf
```

## Stack

* `yarn`
* `reveal.js`
* `live-server` (for serving/reloading on changes)
* `decktape` (for creating PDFs from the slides)
* `GhostScript` (for optimising the PDF output)

## References

* https://www.unicode.org/versions/Unicode7.0.0/
* https://unicode.org/~asmus/web-wing-ding-ext.pdf
* https://www.newsweek.com/2016/05/06/secret-ska-history-man-business-suit-levitating-emoji-442192.html
* http://2-tone.info/articles/label.html
* https://en.wikipedia.org/wiki/Peter_Tosh
* https://en.m.wikipedia.org/wiki/Webdings
