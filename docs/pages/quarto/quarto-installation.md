{% raw %}
# Setup Quarto tutorial

## Setup course material 

??? info "Follow this instructions only if you start the course at this stage! Otherwise skip this step!"
        This tutorial depends on files from the course GitHub repo. Please follow these instructions 
        on how to set it up if you haven't done so already.  
        Let's create a directory and clone the course GitHub repo.
        
        ```bash
        mkdir -p  {{training_path}}
        cd {{training_path}}
        git clone {{config.repo_url}}
        ```

## Setup environment 

First let's create a dedicated folder for this tutorial:

```bash
mkdir -p  ~/training-reproducible-research-area/quarto
cd ~/training-reproducible-research-area/quarto
cp -r ~/training-reproducible-research-area/training_reproducible_research/tutorials/quarto/* . 
```

We will use Conda environments for the set up of this tutorial. So, now we will install all the tools via conda:

```bash
conda env create -f ~/training-reproducible-research-area/training_reproducible_research/tutorials/quarto/environment.yml -n quarto-env
```

You can then activate the environment followed by running RStudio in the background from the command lines:

```bash
conda activate quarto-env
```

## Rstudio with quarto 

!!! warning 
        Quarto is still in its infancy on conda and has some conflicts with certain R packages on conda. What's more, the Rstudio package on conda is not the latest version (does not integrate quarto natively). If you wish to use the graphical interface to generate Quarto files, we recommend the following installations

### Docker installation (Reproductible)

The documentation is available [here](https://rocker-project.org/images/versioned/rstudio.html) from the Rocker project.

```bash 
docker run --rm -ti -p 8787:8787 rocker/rstudio
```

### Classic installation

1. Install Rstudio : [https://posit.co/download/rstudio-desktop/](https://posit.co/download/rstudio-desktop/)
2. Install quarto : [https://quarto.org/docs/get-started/](https://quarto.org/docs/get-started/)


Et voilà !

{% endraw %}

conda env update -f environment.yml -n quartp-env