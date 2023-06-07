One of the main points of version control is that you can go back in time to recover.
Let's have look at safe commands that do not modify the commit history.

## Undoing uncommitted changes 

### Unstaged file

* Let's edit `config.yml` and remove the line 
`sample_ids: ["SRR935090","SRR935091","SRR935092"]`. Run `git status`, it will tell you 
that there are modifications in one file (`config.yml`) compared to the previous commit.

For unstaged file it is possible to have details about the modifications made.
```bash
git diff config.yml
```

You now realize that this modification was wrong. Use `git restore` to remove all 
modifications made since last commit.
```bash
git restore config.yml
git status
```
As you can see, Git tells us that this file has not been modified since last commit.

### Staged file

* Let's edit `config.yml`, remove the line 
`sample_ids: ["SRR935090","SRR935091","SRR935092"]`, stage the file and run `git status`. 

Stage and commit the first file 
```bash
git add config.yml
git status
```

Git tells us that there is a staged file. You now realize that this modification was 
wrong. You have to first unstage the file before to clean the modifications:

```bash
git restore --stage config.yml
git status
git restore config.yml
git status
```

!!! tip
    In case you want to throws away everything that is not in last commit (HEAD) you can
    use `git reset --hard HEAD`. It is apply on all files, staged and unstaged. 

## Undoing committed changes 

* Let's edit `config.yml`, remove the line 
`sample_ids: ["SRR935090","SRR935091","SRR935092"]`, stage the file, commit, and run 
`git status`. 
```bash
git add config.yml
git commit -m "remove sample_ids line"
git status
```

The `git status` is not really helpfull here as we already commited our modifications 
```bash
git log
```

The `git log` command show us the message we entered in previous commits.

To see modification made in the previous commit you can use:
```bash
git diff HEAD^
```

!!! tip
    Too see the modifications between the last commit and a particular commit you can use 
    `git diff <commit_id>`. It is also possible to compare the differences between two commits:
    `git diff <commit_id1> <commit_id2>`.

You now realize that the latest commit was a mistake and you wish to undo it:
```bash
git log --online
git revert <commit>
```

This creates a new commit that does the opposite of the reverted commit. The old commit remains in the history.

!!! note 
    You can revert any commit, no matter how old it is. It doesn’t affect other commits you have done since then - but if they touch the same code, you may get a conflict (which we’ll learn about later).

!!! Success "Quick recap"
    We added four important Git commands to our repertoire:
    
    * `git diff <file>` list all modifications made on a file since last commit
    * `git restore <file>` cancels the modifications of an unstaged file
    * `git restore --staged <file>` unstage a staged file
    * `git revert <commit>` does the opposite of the reverted commit


