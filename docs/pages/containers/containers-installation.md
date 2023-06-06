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
mkdir -p  {{training_path}}/containers
cd {{training_path}}/containers
cp -r {{training_path}}/{{config.repo_name}}/tutorials/containers/* . 
```

This tutorial depends on Docker and Singularity. Take a look at the
[setup](../course-information/pre-course-setup.md) for instructions on how to install them if you
haven't done so already.

{% endraw %}