# Mental health and neurodivergence in veterinary students

Data analysis of a survey of veterinary students who study (or studied) in Hungary, about neurodivergence, mental health and wellbeing.

- `cleanup.ipynb`: cleans the survey answers
- `eba.ipynb`: exploratory data analysis
- `cda.ipynb`: work in progress

The `datasets` folder is not committed.

## Slides

The EDA notebook is published as a slideshow on GitHub Pages: <https://carlaonate.github.io/data-analysis-mental-health-veterinary-medicine-thesis/>

The slides are `docs/index.html`, exported from `eba.ipynb` with the code hidden. After changing the notebook, run it, save it, then re-export:

```bash
jupyter nbconvert eba.ipynb --to slides --no-input --no-prompt --TemplateExporter.extra_template_basedirs=templates --template slides --SlidesExporter.reveal_number='c/t' --output-dir docs --output index && mv docs/index.slides.html docs/index.html
```

Commit and push `docs/index.html` to update the site.

- Each markdown cell is a slide and the chart or table below it is a sub-slide (press ↓). Code cells without output are skipped. This is set per cell in the notebook's slideshow metadata.
- `templates/slides` extends nbconvert's reveal template so long slides scroll to the end instead of being cut off.
