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
mkdir -p  {{training_path}}/quarto
cd {{training_path}}/quarto
cp -r {{training_path}}/{{config.repo_name}}/tutorials/quarto/* . 
```

??? quote "Follow the instructions below only if you start the course at this stage! Otherwise skip this step!"
        ```bash
        conda env create -f {{training_path}}/{{config.repo_name}}/tutorials/rmarkdown/environment.yml -n rmarkdown-env
        ```

Now activate the environment containing RStudio:
```
conda activate rmarkdown-env
```

{% endraw %}