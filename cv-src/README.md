# CV source

`cv.tex` is the source for the top-level `CV.pdf`. It is plain LaTeX
(Computer Modern, `article` class) and compiles with any standard
distribution — including Overleaf, where you can upload `cv.tex` on its own.

```sh
pdflatex cv.tex && pdflatex cv.tex   # run twice so page breaks settle
mv cv.pdf ../CV.pdf
```

Required packages: `geometry`, `titlesec`, `enumitem`, `tabularx`,
`fontawesome5`, `needspace`, `hyperref` — all in `texlive-latex-recommended`,
`texlive-latex-extra` and `texlive-fonts-extra`.

Layout notes:
- `\cvHeading{org}{location}{role}{dates}` sets a two-line position entry.
- `\cvDetail{title}{description}` and `\cvProject{title}{date}{description}`
  set the sub-bullets.
- `\needspace` before *Work Experience* keeps that section from splitting
  across the page break; adjust or drop it if the content changes.
