{% raw %}
# Setup R-markdown tutorial

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
mkdir -p  {{training_path}}/rmarkdown
cd {{training_path}}/rmarkdown
cp -r {{training_path}}/{{config.repo_name}}/tutorials/rmarkdown/* . 
```

We will use Conda environments for the set up of this tutorial. So, now we will install all the tools via conda:

```bash
conda env create -f {{training_path}}/{{config.repo_name}}/tutorials/rmarkdown/environment.yml -n rmarkdown-env
conda activate rmarkdown-env
```

You can then activate the environment followed by running RStudio in the background from the command line:

conda activate rmarkdown-env
rstudio &

!!! tip "The sluggishness of Conda"
        Some environments are inherently quite complicated in that they have many and varied dependencies, meaning that the search space for the entire dependency hierarchy becomes huge - leading to slow and sluggish installations. This is often the case for R environments. This can be improved by using Mamba, a faster wrapper around Conda. Simply run conda install -n base mamba to install Mamba in your base environment, and replace any conda command with mamba - except activating and deactivating environments, which still needs to be done using Conda.

!!! tip "RStudio and Conda"
        In some cases RStudio doesn't play well with Conda due to differing libpaths. The first and simplest thing to try is to always start RStudio from the command line (rstudio &). If you're still having issues, check the available library path by .libPaths() to make sure that it points to a path within your Conda environment. It might be that .libPaths() shows multiple library paths, in which case R packages will be searched for by R in all these locations. This means that your R session will not be completely isolated in your Conda environment and that something that works for you might not work for someone else using the same Conda environment, simply because you had additional packages installed in the second library location. One way to force R to just use the conda library path is to add a .Renviron file to the directory where you start R with these lines:
        ```
        R_LIBS_USER=""
        R_LIBS=""
        ```
        ... and restart RStudio. The rmarkdown/ directory in the course materials already contains this file, so you shouldn't have to add this yourself, but we mention it here for your future projects.

{% endraw %}