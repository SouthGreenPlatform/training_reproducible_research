# Tools for Reproducible Research

**Important: This repo is an example and does not have the data to make it work.**

## How can a bioinformatics project be made more reproducible?

The aim of this repo is to show how : 

1. Create a repo on GitHub
2. Create a README and set a license
3. Add a conda file and our Jupyter notebook file
4. Update the README to explain how to edit it and use quarto to generate the page in HTML
5. Publish this page on GitHub and put it online
6. Make a release with Zenodo to have a DOI of your code
7. Set up a contributors file
8. See how to archive the repository on Software heritage

## For collaborators and developers

This part is for collaborators and developers.

### Create a conda env

```bash
conda env create -f environment.yml -n quarto-env
conda activate quarto-env
```

### Render the notebook

```bash
quarto render supplementary_material.Rmd --to html
``` 

### Example of results 

- [Rmd to HTML](./supplementary_material.html)

##  Acknowledgement

 * All contributors

## License

This work is licensed under a [Creative Commons Attribution 4.0 International License][cc-by].

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg



