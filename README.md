# A Real-Time VR Rendering Survival Guide for Human Scientists

Quarto source for the guide website + PDF.

## Structure
- `index.qmd` — the entire guide (edit this file to update the guide)
- `media/` — all figures
- `_quarto.yml` — site + PDF configuration

## Local preview
Install Quarto (https://quarto.org/docs/get-started/), then:

    quarto preview        # live-reloading local preview
    quarto render         # builds _site/ with HTML + PDF

## Publishing
First time only:

    git init && git add . && git commit -m "initial"
    # create empty repo on GitHub, then:
    git remote add origin git@github.com:YOURUSERNAME/rendering-guide.git
    git push -u origin main
    quarto publish gh-pages

After that, every `git push` to main re-renders and republishes
automatically via `.github/workflows/publish.yml`.
The PDF download link appears automatically in the site sidebar
("Other Formats").
