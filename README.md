# Recite - painlessly swap bibliographies in a LaTeX document

*Recite* is a command line tool to automatically replace the citation keys in your LaTeX document when you replace a bibliography file. Very useful when merging work from separate documents with overlapping bibliographies that, chances are, refer to the same papers with different keys.

## Installation

```
pip install recite
```

## Usage

```
recite document.tex old.bib new.bib > document.tex
```

the `\cite{}` commands in `document.tex` will be edited to match the citation keys used in `new.bib`

## Expected questions

1. *What if paper titles aren't exactly the same in 2 bibliographies or authors' names are off by a diacritic?* `Recite` uses approximate matching with [unisim](https://github.com/google/unisim), so similarly titled references will be matched.
2. *Can't it make mistakes then?* Yes, yes it can. But you do read your documents before submitting them anywhere, don't you?