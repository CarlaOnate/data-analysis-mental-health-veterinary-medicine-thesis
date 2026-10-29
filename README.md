# Mental health and neurodivergence in veterinary students

Data analysis of a survey of veterinary students who study (or studied) in Hungary, about neurodivergence, mental health and wellbeing.

- `cleanup.ipynb`: cleans the survey answers
- `eba.ipynb`: exploratory data analysis
- `cda.ipynb`: confirmatory data analysis (ND vs not ND comparisons and potential protective factors)

The `datasets` folder is not committed.

## Slides

Both analysis notebooks are published as slideshows on GitHub Pages:

- EDA: <https://carlaonate.github.io/data-analysis-mental-health-veterinary-medicine-thesis/>
- CDA: <https://carlaonate.github.io/data-analysis-mental-health-veterinary-medicine-thesis/cda.html>

The slides are `docs/index.html` (from `eba.ipynb`) and `docs/cda.html` (from `cda.ipynb`), exported with the code hidden. After changing a notebook, run it, save it, then re-export it:

```bash
jupyter nbconvert eba.ipynb --to slides --no-input --no-prompt --TemplateExporter.extra_template_basedirs=templates --template slides --SlidesExporter.reveal_number='c/t' --output-dir docs --output index && mv docs/index.slides.html docs/index.html
```

```bash
jupyter nbconvert cda.ipynb --to slides --no-input --no-prompt --TemplateExporter.extra_template_basedirs=templates --template slides --SlidesExporter.reveal_number='c/t' --output-dir docs --output cda && mv docs/cda.slides.html docs/cda.html
```

Commit and push the updated file in `docs` to update the site.

- Each markdown cell is a slide and the chart or table below it is a sub-slide (press ↓). Code cells without output are skipped. This is set per cell in the notebook's slideshow metadata.
- `templates/slides` extends nbconvert's reveal template so long slides scroll to the end instead of being cut off.
