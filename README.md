# the-gym-git-exercise-solution
it is the repo which will be used for submiting solutions for the git curriculum exercises

# Bundle 1
## Exercise 1
```bash
jb-dev% pwd
/home/jb-dev/Documents/TheGym/Prep/Git-Exercise/brundle1/Exercise1

jb-dev% git init
jb-dev% git branch -M main
  refname refs/heads/master not found
  fatal: Branch rename failed
jb-dev% git status
  On branch master

  No commits yet

  Untracked files:
    (use "git add <file>..." to include in what will be committed)
          README.md
          src/

  nothing added to commit but untracked files present (use "git add" to track)
jb-dev% git add .
jb-dev% git commit -m "Git Setup"
  [master (root-commit) ee8c310] Git Setup
  3 files changed, 18 insertions(+)
  create mode 100644 README.md
  create mode 100644 src/index.html
  create mode 100644 src/style.css
jb-dev% git branch
  * master
jb-dev% git branch -m main
jb-dev% git status
  On branch main
  nothing to commit, working tree clean
jb-dev% git log
  commit ee8c310e2c8bd284a81d33a3caa6c9a0342bc3c2 (HEAD -> main)
  Author: Bateyjosue <josuebatey19@gmail.com>
  Date:   Sun May 14 11:28:26 2023 +0200

      Git Setup
jb-dev% git remote add origin https://github.com/Bateyjosue/bundle1-exercise1.git
jb-dev% git push -u origin main 
  Enumerating objects: 6, done.
  Counting objects: 100% (6/6), done.
  Delta compression using up to 4 threads
  Compressing objects: 100% (5/5), done.
  Writing objects: 100% (6/6), 609 bytes | 609.00 KiB/s, done.
  Total 6 (delta 0), reused 0 (delta 0)
  To https://github.com/Bateyjosue/bundle1-exercise1.git
  * [new branch]      main -> main
  Branch 'main' set up to track remote branch 'main' from 'origin'.
jb-dev% git checkout -b dev
  Switched to a new branch 'dev'
jb-dev% git push -u origin dev 
  Total 0 (delta 0), reused 0 (delta 0)
  remote: 
  remote: Create a pull request for 'dev' on GitHub by visiting:
  remote:      https://github.com/Bateyjosue/bundle1-exercise1/pull/new/dev
  remote: 
  To https://github.com/Bateyjosue/bundle1-exercise1.git
  * [new branch]      dev -> dev
  Branch 'dev' set up to track remote branch 'dev' from 'origin'.
jb-dev% git checkout -b test
  Switched to a new branch 'test'
jb-dev% git push origin test
  Total 0 (delta 0), reused 0 (delta 0)
  remote: 
  remote: Create a pull request for 'test' on GitHub by visiting:
  remote:      https://github.com/Bateyjosue/bundle1-exercise1/pull/new/test
  remote: 
  To https://github.com/Bateyjosue/bundle1-exercise1.git
  * [new branch]      test -> test
jb-dev% git switch dev 
  Switched to branch 'dev'
  Your branch is up to date with 'origin/dev'.
jb-dev% git branch  
  * dev
    main
    test
jb-dev% git push origin --delete test
  To https://github.com/Bateyjosue/bundle1-exercise1.git
  - [deleted]         test

    Switched to a new branch 'test'

jb-dev% git branch
  * dev
    main

```

## Exercise 2
```bash
  jb-dev% git add .
  jb-dev% git commit -m "Add file home"
  jb-dev% git stash
  jb-dev% git stash list
    stash@{0}: WIP on dev: 1e66b7c Update README.md to add description
  jb-dev% git add .
  jb-dev% git commit -m "Add file about"
  jb-dev% git stash
  jb-dev% git stash list
    stash@{0}: WIP on dev: 1e66b7c Update README.md to add description
    stash@{1}: WIP on dev: 1e66b7c Update README.md to add description
  jb-dev% git add .
  jb-dev% git commit -m "Add file team"
  jb-dev% git stash
  jb-dev% git stash list
    stash@{0}: WIP on dev: 1e66b7c Update README.md to add description
    stash@{1}: WIP on dev: 1e66b7c Update README.md to add description
    stash@{2}: WIP on dev: 1e66b7c Update README.md to add description
  jb-dev% git stash pop stash@{1}
    On branch dev
    Your branch is behind 'origin/dev' by 1 commit, and can be fast-forwarded.
      (use "git pull" to update your local branch)

    Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
            new file:   src/about.html
    Dropped stash@{1} (90f8a020c3be424b0396025f4f0b275c1e42d140)
  jb-dev% git stash pop --index 1
    On branch dev
    Your branch is behind 'origin/dev' by 1 commit, and can be fast-forwarded.
      (use "git pull" to update your local branch)

    Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
            new file:   src/home.html
    Untracked files:
      (use "git add <file>..." to include in what will be committed)
            src/about.html
    Dropped refs/stash@{1} (eaf81f59c7eaa399927aa96bf3b08f8ced3634a4)
  jb-dev% git add .
  jb-dev% git commit -m "Add file home and about"
  [dev 0b4f6c8] Add file home and about
  3 files changed, 25 insertions(+), 12 deletions(-)
  create mode 100644 src/about.html
  create mode 100644 src/home.html
  delete mode 100644 src/index.html
  jb-dev% git push
  Enumerating objects: 14, done.
    Counting objects: 100% (14/14), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (8/8), done.
    Writing objects: 100% (8/8), 982 bytes | 982.00 KiB/s, done.
    Total 8 (delta 2), reused 0 (delta 0)
    remote: Resolving deltas: 100% (2/2), completed with 1 local object.
    To https://github.com/Bateyjosue/bundle1-exercise1.git
      0b8f3ac..91b040c  dev -> dev
jb-dev% git stash list
  stash@{0}: WIP on dev: 1e66b7c Update README.md to add description
jb-dev% git stash pop --index 0
  On branch dev
  Your branch is up to date with 'origin/dev'.

  Changes to be committed:
    (use "git restore --staged <file>..." to unstage)
          new file:   src/team.html

  Dropped refs/stash@{0} (3961ce7bedc4a66b87257ec927d0de3ce13d3d69)
  jb-dev% git status
    On branch dev
    Your branch is up to date with 'origin/dev'.

    Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
            new file:   src/team.html

  jb-dev% git reset --hard
    HEAD is now at 0b4f6c8  Add file home and about
```