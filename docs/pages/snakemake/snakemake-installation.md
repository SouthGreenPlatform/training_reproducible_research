{% raw %}
# Setup Snakemake tutorial

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
mkdir -p  {{training_path}}/snakemake
cd {{training_path}}/snakemake
cp -r {{training_path}}/{{config.repo_name}}/tutorials/snakemake/* . 
```

We will use Conda environments for the set up of this tutorial. So, now we will install all the tools via conda:

```bash
conda env create -f environment.yml -n snakemake-env
conda activate snakemake-env
```



{% endraw %}