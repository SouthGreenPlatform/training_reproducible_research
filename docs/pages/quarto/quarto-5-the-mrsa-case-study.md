All the work of writing notebooks has already been done in the 
previous sequences: [Rmardown](../../rmarkdown/r-markdown-7-the-mrsa-case-study.md) and [Jupyter](../../jupyter/jupyter-8-the-mrsa-case-study.md)

Here, we're going to see how to use quarto to convert them. 

## Rmarkdown

```bash
quarto render code/supplementary_material.Rmd --to html
quarto render code/supplementary_material.Rmd --to docx
```

!!! warning
    As indicated in the setup section, the package versions available on conda cause conflicts with Posit. It is possible to run these commands in the conda environment but we had to mount the versions of certain packages in relation to the rmardown TP because of conflicts. 

## Jupyter

```bash
quarto render code/supplementary_material.ipynb --to html
quarto render code/supplementary_material.ipynb --to docx
```

You're looking at quarto's greatest strength! It can convert Rmd and jupyter notebooks in exactly the same way!

!!! Success "Quick recap"
    In this section you learned how to render R Markdown documents and Jupyter document using quarto.