# Open Source: Hands-on & Hacktoberfest

A live-coding workshop and talk presented at DevNQ.

Slides PDF: <TBD>

## Setup

```bash
yarn
yarn start
```

This starts the presentation server at <http://localhost:8080> and
automatically opens a browser.

## Creating a PDF file

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

