# CV source

`cv.html` is the source for the top-level `CV.pdf`. Edit it, then regenerate:

```sh
chromium --headless --no-pdf-header-footer \
  --print-to-pdf=../CV.pdf --virtual-time-budget=8000 \
  "file://$PWD/cv.html"
```

Any Chromium/Chrome build works (`--headless=new` on newer versions). Page
size, margins and print styling are set in the `@page` / `@media print`
rules inside `cv.html`.
