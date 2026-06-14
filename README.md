# Foundation Agents Google-Style LaTeX Template

A compact LaTeX template for Foundation Agents community papers. The class is
adapted from the Google DeepMind open-access paper template and localized with a
Foundation Agents first-page header, author block, footer, and technical-report
style typography.

## Quick Start

```bash
latexmk -pdf main.tex
```

The generated PDF will be `main.pdf`.

If your paper uses `minted`, compile with shell escape:

```bash
latexmk -pdf -shell-escape main.tex
```

## Files

- `foundationagents.cls`: shared paper class.
- `main.tex`: minimal example paper.
- `references.bib`: example BibTeX file.
- `assets/`: Foundation Agents logo assets used by the header.

## Class Options

```tex
\documentclass[11pt, a4paper, logo, copyright]{foundationagents}
```

Common options:

- `logo`: show the Foundation Agents header mark on the first page.
- `copyright`: add the Foundation Agents community preprint footer.
- `twocolumn`: use two-column layout.
- `nonumbering`: hide section numbering.
- `internal`: mark as internal/confidential.
- `address`: add Foundation Agents to the first-page footer.

## Author Metadata

Use `authblk` syntax:

```tex
\title{Your Paper Title}

\author[1,2]{First Author}
\author[2$\dagger$]{Corresponding Author}

\affil[1]{University A}
\affil[2]{Foundation Agents}

\correspondingauthor{Corresponding Author (\texttt{author@example.com})}
\keywords{Agent learning; evaluation; scalable environments}
```

The `\dagger` marker is used by the footer text for corresponding authors.

## Notes

- Keep paper-specific macros in `main.tex`.
- Keep reusable layout changes in `foundationagents.cls`.
- The wordmark is included as a raster asset so users do not need to install a
  custom font to compile the template.

## License

This template follows the license notice in the original class source:
Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0).
