
# LaTeX Thesis Template

Template for easily getting started with writing a good looking thesis using LaTeX.

It contains some example content from my own thesis (university logo & name, chapter structure, example tables & data) so you can get a picture of how the [final document](thesis.pdf) might look.

By default all sections are outsourced into their own numbered file in `src` to keep the project organized.

This is not a tutorial and a little prior knowledge of LaTeX is beneficial.

## Features

- Produces a well formatted pdf
- with toc, bibliography & glossar
- Organized folder structure
- Option to programatically generate a table with primer sequences from a csv file (Code can easily be adapted to other purposes or removed if not needed)



## Usage
- Setup LaTeX (e.g. TeX Live Full & TeX Studio)
- Clone repo/download project
- Chage title, author, metadata in `thesis.tex` and `src/00a-title_page.tex`
- Get writing, you can keep the example structure or modify it by adding new sections to `thesis.tex` and `src/`.
- Cite your sources (`\cite{citekey})`
- Define acronyms in `src/06-abbreviations.tex` and use them inline with `\ac{}`
- Put figures you want to include into `graphics`
- Provide your referenes in biblatex format in `references.bib`
- Optionally, provide a list of primer sequenes as csv in `data/` to automatically produce a list in the materials section

### Optional: Enable .svg support
If you want to include .svg files as figures (like the university seal in the example) do the following:
1. Make sure you have inkscape installed (It's used for a .svg to .pdf conversion in the background. The generated .pdf is cached in `svg_inkscape/`.)
2. Have inkscape in your PATH (manually on windows, linux does this automatically)
3. add `--shell-escape` to your pdfLaTeX command

Use it like this: `\includesvg[height=45mm]{seal_lmu.svg}` 
