# PhD Thesis

This repository is a modular LaTeX thesis project based on the formatting structure of `bunnech/phd_thesis`, while keeping thesis-specific content, metadata, bibliography content, and chapter text separate from the reference repository.

## Structure

- `thesis.tex`: main document entrypoint
- `preamble/`: shared formatting, metadata, notation, and reusable macros
- `frontbackmatter/`: title pages and thesis-wide front/back matter
- `chapters/`: main chapter files
- `figures/`: image assets used in the thesis
- `tables/`: table source files or exported assets
- `papers/`: source papers to be integrated into thesis chapters
- `bib/`: bibliography files

## Build

If you have `latexmk` installed, the simplest command is:

```bash
latexmk -pdf thesis.tex
```

This repository includes a `latexmkrc` file that sends build artifacts to `build/`.

If you prefer a manual build, use:

```bash
pdflatex thesis.tex
bibtex thesis
pdflatex thesis.tex
pdflatex thesis.tex
```

## First Edits

1. Update the thesis metadata in `preamble/meta.tex`.
2. Replace the placeholder front matter in `frontbackmatter/`.
3. Duplicate `chapters/paper-template.tex` for each paper-based chapter you want to add.
4. Put your papers in `papers/` so they can be mapped into chapters.
5. Add references to `bib/references.bib` as you write.

## Notes

- The formatting infrastructure now reuses and adapts the template family from `bunnech/phd_thesis`, which itself credits `ClassicThesis` under GPLv2.
- Thesis-specific text, bibliography content, figures, and metadata should remain your own.
