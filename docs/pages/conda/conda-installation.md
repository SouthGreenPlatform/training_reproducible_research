{% raw %}
# Setup Conda tutorial

## Setup course material 

??? quote "Follow the instructions below only if you start the course at this stage! Otherwise skip this step!"
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
mkdir -p  {{training_path}}/conda_tutorial
cd {{training_path}}/conda_tutorial
cp -r {{training_path}}/{{config.repo_name}}/tutorials/conda/* . 
```

## Installing Conda

Conda is installed by downloading and executing an installer from the Conda
website, but which version you need depends on your operating system. Choose the 
appropriate installer from the list you can found here: 
[https://docs.conda.io/en/latest/miniconda.html](https://docs.conda.io/en/latest/miniconda.html). 
Then copy the link and download the installer on your computer, see example below: 

```bash
# Install Miniconda3 for 64-bit Linux
curl -L https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O
```

!!! warning

    If you already have installed Conda but want to update, you should be able
    to simply run `conda update conda` and subsequently `conda init`, and skip
    the installation instructions below.

Now you can execute the installer:

```bash
bash Miniconda3-latest-Linux-x86_64.sh
```

The installer will ask you questions during the installation:

- Do you accept the license terms? 
    * Yes
- Do you accept the installation path or do you want to choose a different one?
    * Yes
- Do you want to run `conda init` to setup Conda on your system?
    * Yes

Restart your shell so that the settings in `~/.bashrc` or `~/.bash_profile` can take
effect. You can verify that the installation worked by running:

```bash
conda --version
```

You can now get rid of the installer, you don't need it anymore

```bash
rm Miniconda3-latest-Linux-x86_64.sh
```

By default conda will be activated to every new terminal you will open (in the `base` environment). If you 
whish to deactivate this behaviour run:

```bash
conda config --set auto_activate_base false
```


!!! info "Different Condas"
    There are three Conda-related things you may have encountered: the first is
    *Conda*, the package and environment manager we've been talking about so far.
    Second is *Miniconda*, which is the installer for Conda. The third is
    *Anaconda*, which is a distribution of not only Conda, but also over 150
    scientific Python packages. It's generally better to stick with only Conda,
    *i.e.* installing with Miniconda, rather than installing 3 GB worth of
    packages you may not even use.

Lastly, we will setup the default channels (from where packages will be searched
for and downloaded if no channel is specified).

```
conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels conda-forge
conda config --set channel_priority strict
```

{% endraw %}