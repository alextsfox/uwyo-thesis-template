# LaTeX Template for University of Wyoming Dissertations and Theses
Template Author: Alexander S. Fox

This template is *not* officially endorsed by the University of Wyoming, but is intended to comply with UWyo's thesis formatting guidelines:

https://www.uwyo.edu/registrar/_files/docs/thesis_dissertation_guide2020.pdf

This template is divided up into five sections:

1. Main files
2. Front matter
3. Main text
4. End matter
5. References
6. Backend

# Using the Template
You can use this template locally or duplicate it on Overleaf at https://www.overleaf.com/read/cnrfxvvxnktw#6fe1b8. Alternatively, you can manually upload it to an empty project on Overleaf. If you do so, make sure to go into the menu (on the top-left when inside the project), change the `Compiler` option to "pdfLaTeX", and set `Main Document` option to "main.tex". 

# Main Files
The main files are what is used to set up the structure and formatting of the document. 

* `main.tex` is where you you link your individual chapters and write your name, dissertation title, committee member names, and any other important information. Start here!
* `macros.tex` includes any user-defined macros you might use in your text. I recommend placing any macros you define in this file. Includes several pre-defined macros to help debug text, insert citations, place sideways figures, and insert a glossary section.
* `README.md`, this file
* `LICENSE`, the software license.

# Front matter
The committe page, abstract, acknowledgments, copyright, dedication, table/figure list, table of contents, and title page are included in the `front/` directory. These should auto-configure themselves.  

# Text
The main text of your dissertation (ie your chapters) sits in the `text/` directory: the introduction, body chapters, and conclusion live here.

# End
You can put any appendix information in here, in the `appendix.tex` file in the `end/` directory.

# References
The `references/` directory contains any `.bib` files you will need. You can paste the files in directly, or import them from zotero, mendeley, etc. to here. It is recommended that you use biblatex rather than bibtex as `.bib` format.

# Figs
Any figures or tables can be placed in the `figs/` directory. This is not required, but is recommended for organization.

# Backend
Files used in the backend of the template are included in the `backend/` directory. They are reasonably well-commented, and you are encouraged to modify these files if necessary. Currently, this includes:
* `preamble.tex` contains document imports and formatting information, such as margins, spacing, bibliography formatting, etc.
* `bibformat.tex` defines how bibliography entries are formatted. Currently there is bespoke formatting for article, book, report, software, misc, thesis, and inproceedings types. All other types are automatically handled by biber.
* `trackchanges.sty` defines the track changes package. This is currently unused, but you may enable it manually if you wish.

# Formatting, Citations, Etc
`macros.tex` already define several commands that allow for many different citations styles. This allows users to easily copy-paste their manuscripts if they have already been formatted for a target journal (e.g. the AGU template uses the `\cite` command, but the Elsevier template uses the `\citep` command). 

* Parenthetical citations: `\cite{...}` `\parencite{...}`, or `\citep{...}`.
* In-line citations: `\citeA{...}`, `\textcite{...}`, or `\citet{...}`.

The bibliography is set up by default to use numerical citations, sorted by reference order, but provides the option to change this to author-year citations easily.

This template uses the `report` document type by default, which provides the `\part{...}` (not used), `\chapter{...}`, `\section{...}`, `\subsection{...}`, `\subsubsection{...}` and `\paragraph{...}` headings, among others.

By default, line numbers are turned off. You can turn them back on in `main.tex` for distributing drafts.


