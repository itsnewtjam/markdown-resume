# markdown-resume

Simple script to generate a `.pdf` resume from a markdown file, styled with CSS. Example markdown content and stylesheet are included.

## Setup

Clone repo then install [Pandoc](https://github.com/jgm/pandoc/releases/latest) and [wkhtmltopdf](https://wkhtmltopdf.org/downloads.html).

## Usage

Edit `resume.md` with resume content.

Customize styling in `style.css`.

Convert to `.html` by running:

```
pandoc -o resume.html -c style.css -s resume.md
```

Confirm CSS styles by viewing `resume.html`, then convert to `.pdf` by running:

```
wkhtmltopdf --enable-local-file-access resume.html resume.pdf
```

Once you're happy with the CSS, you can make future resume edits more easily by running `make-pdf.bat` to convert straight to `.pdf`.
