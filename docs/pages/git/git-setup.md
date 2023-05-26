## Configure git

If it is the first time you use git on your computer, you may want to configure
it so that it is aware of your username and email. These should match those that
you have registered on GitHub. This will make it easier when you want to sync
local changes with your remote GitHub repository.

```
git config --global user.name "Mona Lisa"
git config --global user.email "mona_lisa@gmail.com"
```

!!! tip

    If you have several accounts (*e.g.* both a GitHub and Bitbucket account),
    and thereby several different usernames, you can configure git on
    a per-repository level. Change directory into the relevant local git
    repository and run `git config user.name "Mona Lisa"`. This will set the
    default username for that repository only.

You will also need to configure the default branch name to be `main` instead of
`master`:

```bash
git config --global init.defaultBranch "main"
```

The short version of why you need to do this is that GitHub uses `main` as the
default branch while Git itself is still using `master`; please read the box
below for more information.

!!! note

    The default branch name for Git and many of the online resources for hosting
    Git repositories has traditionally been `master`, which historically comes
    from the "master/slave" repositories of
    [BitKeeper](https://mail.gnome.org/archives/desktop-devel-list/2019-May/msg00066.html).
    This has been heavily discussed and in 2020 the decision was made by  many
    ([including GitHub](https://sfconservancy.org/news/2020/jun/23/gitbranchname/))
    to start using `main` instead. Any repository created with GitHub uses this
    new naming scheme since October of 2020, and Git itself is currently
    discussing implementing a similar change. Git did, however, introduce the
    ability to set the default branch name when using `git init` in
    [version 2.28](https://github.blog/2020-07-27-highlights-from-git-2-28/#introducing-init-defaultbranch),
    instead of using a hard-coded `master`. We have chosen to use `main` for this course.
