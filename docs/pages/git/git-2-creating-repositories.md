{% raw %}
!!! Warning
    To properly start this training session, you must be within a folder
    where it makes sense to work during the course:  
    ```
    mkdir {{training_path}}
    cd {{training_path}}
    ```

Let's start by running this command:

```bash
git --version
```

You should get something like `git version 2.37.1 (Apple Git-137.1)`. That means
git is well installed on your computer and you can go ahead.
Then try the following command and see what happens: 

```bash
git status
```
!!! tip
    If you try to run `git status` in a non-Git directory, it will say
    that it is *not a git repository*. The way this works is that Git
    adds a hidden directory `.git/` in the root of a Git tracked
    directory (run `ls -a` to see it). This hidden directory contains
    all information and settings Git needs in order to run and version
    track your files. This also means that your Git-tracked directory
    is self-contained, *i.e.* you can simply delete it and everything that
    has to do with Git in connection to that directory will be gone

Let start by retrieving the Reproducible Research course git repository somewhere on internet:

```bash
git clone {{config.repo_url}}
```

The `git clone` command copies a remote git repository locally. No worries, we will review this concept later.
You now have a local directory called  `{{config.repo_name}} `, run `ls -l` to see it

Move in it and run the `git status` command again, what do you see?

```bash
cd {{config.repo_name}}
git status
```

The directory you are looking is a version-tracked directory. Indeed the 
`git status` command should return something like this:

```no-highlight
On branch main

Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

!!! note
    git repository == version-tracked directory

Let's now create our own git repository. First get out of the `{{config.repo_name}}` 
directory and go back to the `git_tutorial` one:

```bash
cd ..
```

!!! warning
    From here you must be back to the `{{training_path}}` directory  

In order to create a new Git repository, we first need a directory to track.
Let's create one and move inside:

```bash
mkdir git_tutorial
cd git_tutorial
```

This directory is not yet a version-tracked directory, you can check it using
again the `git status` command. Now we can *initialise*
Git with the following command:

```bash
git init
```

The directory is now a version-tracked directory. How can you know? Run the
command `git status`, which will probably return something like this:

```no-highlight
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```

The text `nothing to commit (create/copy files and use "git add" to track)`
tells us that while we are inside a directory that Git is currently tracking,
there are currently no files being tracked; let's add some!

Copy the following files from the `{{config.repo_name}}` directory we get at 
the beginning of the excercice into your `git_tutorial` directory:

```bash
cp ../training_reproducible_research/tutorials/git/Dockerfile .
cp ../training_reproducible_research/tutorials/git/Snakefile .
cp ../training_reproducible_research/tutorials/git/config.yml .
cp ../training_reproducible_research/tutorials/git/environment.yml .
```

Once you have done that, run `git status` again. It will tell you that there
are files in the directory that are not version tracked by Git.

!!! note
    For the purpose of this tutorial, the exact contents of the files you just
    copied are not important, but we provide a brief overview here:

    - The `environment.yml` file contains the Conda environment with all the
      software used for a defined analysis.
    - The `Snakefile` and `config.yml` are both used to define a Snakemake
      workflow.
    - The `Dockerfile` contains the recipe for making a Docker container for
      a defined analysis.

!!! Success "Quick recap"
    We have used two `git` commands this far:

    - `git init` tells Git to track the current directory.
    - `git status` is a command you should use *a lot*. It will tell you,
      amongst other things, the status of the current directory (version-tracked  or not),
      the status of files contained in your reposiory (Tracked or not), of a Git clone 
      in relation to the online remote repository, etc.

{% endraw %}