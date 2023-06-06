{% raw %}
# Setup Jupyter tutorial

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
mkdir -p  {{training_path}}/jupyter
cd {{training_path}}/jupyter
cp -r {{training_path}}/{{config.repo_name}}/tutorials/jupyter/* . 
```

Let's continue using Conda for installing software, since it's so convenient to do so! Create a Conda environment from the environment.yml file and test the installation of Jupyter, like so:

```bash
conda env create -f environment.yml -n jupyter-env
conda activate jupyter-env
```

{% endraw %}