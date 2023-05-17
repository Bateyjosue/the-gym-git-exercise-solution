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

# Bundle 2
## Exercise 1

```bash
  jb-dev% git checkout -b ft/bundle-2
  jb-dev% touch services.html && code services.html
  jb-dev% git status
    On branch ft/bundle-2
    Your branch is up to date with 'origin/ft/bundle-2'.

    Untracked files:
      (use "git add <file>..." to include in what will be committed)
            services.html

    nothing added to commit but untracked files present (use "git add" to track)
  jb-dev% git add .
  jb-dev% git commit -m "Add services.html page"
    [ft/bundle-2 015af51] Add services.html page
    1 file changed, 12 insertions(+)
    create mode 100644 services.html
  jb-dev% git push
    Enumerating objects: 4, done.
    Counting objects: 100% (4/4), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 520 bytes | 520.00 KiB/s, done.
    Total 3 (delta 0), reused 0 (delta 0)
    remote: This repository moved. Please use the new location:
    remote:   https://github.com/Bateyjosue/Git-Exercise.git
    To https://github.com/Bateyjosue/bundle1-exercise1.git
      91b040c..015af51  ft/bundle-2 -> ft/bundle-2
  jb-dev% 
```

## Exercise 2

```bash
  jb-dev% git switch main 
    Switched to branch 'main'
    Your branch is behind 'origin/main' by 4 commits, and can be fast-forwarded.
      (use "git pull" to update your local branch)
  jb-dev% git pull
    Updating 1e66b7c..a671154
    Fast-forward
    services.html                  | 12 ++++++++++++
    src/{index.html => about.html} |  4 ++--
    src/home.html                  | 13 +++++++++++++
    src/style.css                  |  4 ++++
    4 files changed, 31 insertions(+), 2 deletions(-)
    create mode 100644 services.html
    rename src/{index.html => about.html} (74%)
    create mode 100644 src/home.html
  
  jb-dev% git checkout -b ft/service-redesign
    Switched to a new branch 'ft/service-redesign'
  jb-dev% git add services.html 
  jb-dev% git commit -m "Add descriptive paragraph"          
    [ft/service-redesign f353589] Add descriptive paragraph
    1 file changed, 4 insertions(+), 1 deletion(-)
  jb-dev% git push -u origin ft/service-redesign 
    Enumerating objects: 5, done.
    Counting objects: 100% (5/5), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 908 bytes | 908.00 KiB/s, done.
    Total 3 (delta 0), reused 0 (delta 0)
    remote: This repository moved. Please use the new location:
    remote:   https://github.com/Bateyjosue/Git-Exercise.git
    remote: 
    remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
    remote:      https://github.com/Bateyjosue/Git-Exercise/pull/new/ft/service-redesign
    remote: 
    To https://github.com/Bateyjosue/bundle1-exercise1.git
    * [new branch]      ft/service-redesign -> ft/service-redesign
    Branch 'ft/service-redesign' set up to track remote branch 'ft/service-redesign' from 'origin'.
    jb-dev% git status
    On branch ft/service-redesign
    Your branch is up to date with 'origin/ft/service-redesign'.

    nothing to commit, working tree clean
  jb-dev% git switch main
    Switched to branch 'main'
    Your branch is up to date with 'origin/main'.
  jb-dev% git add services.html 
  jb-dev% git commit -m "Add headline and paragraph"
    [main 6de9e7e] Add headline and paragraph
    1 file changed, 7 insertions(+), 1 deletion(-)
    jb-dev% git push
    Enumerating objects: 5, done.
    Counting objects: 100% (5/5), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 653 bytes | 653.00 KiB/s, done.
    Total 3 (delta 0), reused 0 (delta 0)
    remote: This repository moved. Please use the new location:
    remote:   https://github.com/Bateyjosue/Git-Exercise.git
    To https://github.com/Bateyjosue/bundle1-exercise1.git
      a671154..6de9e7e  main -> main
  jb-dev% git switch ft/service-redesign 
    Switched to branch 'ft/service-redesign'
    Your branch is up to date with 'origin/ft/service-redesign'.

  jb-dev% git diff ft/service-redesign..main
    diff --git a/services.html b/services.html
    index 060621b..0aa4c1e 100644
    --- a/services.html
    +++ b/services.html
    @@ -7,9 +7,12 @@
      <title>Git Exercise | Services</title>
    </head>
    <body>
    -  <h1>
    +  <h2>
        Services Page Git Exercise
    -  </h1>
    -  <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ducimus nam fuga provident impedit similique! Labore doloribus officia odio fuga, debitis autem natus amet corrupti, deserunt beatae ullam reiciendis illo iure quam magni, modi veniam dolorum ipsam veritatis. Ab minus exercitationem harum? At quia voluptas pariatur obcaecati maxime delectus facilis, id ducimus. Consequatur ad expedita, eos rerum placeat doloribus officia rem soluta libero porro, consectetur, est itaque? Fugit dignissimos quia ducimus aut id alias corporis beatae, ipsa sapiente ullam maiores eaque, ab dicta labore temporibus ipsam fuga hic cumque fugiat laborum, consequatur dolorem iure provident et! Modi doloribus incidunt voluptas minima!</p>
    +  </h2>
    +  <p>
    +    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Inventore quasi aspernatur dignissimos in harum quisquam, veniam laudantium possimus tempore. Provident.
    +    <a href="#">Read more</a>
    +  </p>
    </body>
    </html>
    \ No newline at end of file
  
  jb-dev% git merge main
    Auto-merging services.html
    CONFLICT (content): Merge conflict in services.html
    Automatic merge failed; fix conflicts and then commit the result.
    jb-dev% git add .
    jb-dev% git commit -m "Fix Merge"
    [ft/service-redesign 05f47be] Fix Merge
    jb-dev% git status
    On branch ft/service-redesign
    Your branch is ahead of 'origin/ft/service-redesign' by 2 commits.
      (use "git push" to publish your local commits)

    nothing to commit, working tree clean
  jb-dev% git push
    Enumerating objects: 7, done.
    Counting objects: 100% (7/7), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 551 bytes | 551.00 KiB/s, done.
    Total 3 (delta 1), reused 0 (delta 0)
    remote: Resolving deltas: 100% (1/1), completed with 1 local object.
    remote: This repository moved. Please use the new location:
    remote:   https://github.com/Bateyjosue/Git-Exercise.git
    To https://github.com/Bateyjosue/bundle1-exercise1.git
      f353589..05f47be  ft/service-redesign -> ft/service-redesign
```

# Bundle 3
## Exercise 1

```bash
  jb-dev% git checkout -b ft/team-page
    Switched to a new branch 'ft/team-page'
  jb-dev% touch team.html
  jb-dev% code team.html 
  jb-dev% git add .
  jb-dev% git commit -m "Add Team page"
    [ft/team-page 7649b1d] Add Team page
    1 file changed, 14 insertions(+)
    create mode 100644 team.html
  jb-dev% git push -u origin ft/team-page 
    Enumerating objects: 4, done.
    Counting objects: 100% (4/4), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 475 bytes | 475.00 KiB/s, done.
    Total 3 (delta 1), reused 0 (delta 0)
    remote: Resolving deltas: 100% (1/1), completed with 1 local object.
    remote: This repository moved. Please use the new location:
    remote:   https://github.com/Bateyjosue/Git-Exercise.git
    remote: 
    remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
    remote:      https://github.com/Bateyjosue/Git-Exercise/pull/new/ft/team-page
    remote: 
    To https://github.com/Bateyjosue/bundle1-exercise1.git
    * [new branch]      ft/team-page -> ft/team-page
    Branch 'ft/team-page' set up to track remote branch 'ft/team-page' from 'origin'.
  jb-dev% git switch main 
    Switched to branch 'main'
    Your branch is up to date with 'origin/main'.
  jb-dev% git checkout -b ft/contact-page
    Switched to a new branch 'ft/contact-page'
  jb-dev% git checkout ft/team-page 
    Switched to branch 'ft/team-page'
    Your branch is up to date with 'origin/ft/team-page'.
  jb-dev% git log --oneline
    7649b1d (HEAD -> ft/team-page, origin/ft/team-page) Add Team page
    da37eb3 (origin/main, main, ft/contact-page) Merge pull request #3 from Bateyjosue/ft/service-redesign
    05f47be (origin/ft/service-redesign, ft/service-redesign) Fix Merge
    6de9e7e Add headline and paragraph
    f353589 Add descriptive paragraph
    a671154 Merge pull request #2 from Bateyjosue/ft/bundle-2
    015af51 (origin/ft/bundle-2, ft/bundle-2) Add services.html page
    5b9efbe Merge pull request #1 from Bateyjosue/dev
    91b040c (origin/dev, dev) Fix Merge
    0b4f6c8 Add file home and about
    0b8f3ac Add file home and about
    1e66b7c (test) Update README.md to add description
    ee8c310 Git Setup
  jb-dev% git checkout ft/contact-page 
    Switched to branch 'ft/contact-page'

  jb-dev% git cherry-pick 7649b1d
    [ft/contact-page 7497724] Add Team page
    Date: Wed May 17 12:36:42 2023 +0200
    1 file changed, 14 insertions(+)
    create mode 100644 team.html
  jb-dev% git status
    On branch ft/contact-page
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
            modified:   team.html

    no changes added to commit (use "git add" and/or "git commit -a")
  jb-dev% git add team.html 
  jb-dev% git commit -m "Add the descriptive paragraphin team.html page"
    [ft/contact-page 2634d00] Add the descriptive paragraphin team.html page
    1 file changed, 1 insertion(+)
    jb-dev% git push -u origin ft/contact-page 
    Enumerating objects: 7, done.
    Counting objects: 100% (7/7), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (6/6), done.
    Writing objects: 100% (6/6), 964 bytes | 964.00 KiB/s, done.
    Total 6 (delta 3), reused 0 (delta 0)
    remote: Resolving deltas: 100% (3/3), completed with 1 local object.
    remote: This repository moved. Please use the new location:
    remote:   https://github.com/Bateyjosue/Git-Exercise.git
    remote: 
    remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
    remote:      https://github.com/Bateyjosue/Git-Exercise/pull/new/ft/contact-page
    remote: 
    To https://github.com/Bateyjosue/bundle1-exercise1.git
    * [new branch]      ft/contact-page -> ft/contact-page
    Branch 'ft/contact-page' set up to track remote branch 'ft/contact-page' from 'origin'.

  jb-dev% git checkout -b ft/faq-page
    Switched to a new branch 'ft/faq-page'
  jb-dev% touch faq.html
  jb-dev% code faq.html 
  jb-dev% git add faq.html 
  jb-dev% git commit -m "Add faq page"
    [ft/faq-page ca81e5e] Add faq page
    1 file changed, 14 insertions(+)
    create mode 100644 faq.html
  jb-dev% git push -u origin ft/faq-page 
    Enumerating objects: 4, done.
    Counting objects: 100% (4/4), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 474 bytes | 474.00 KiB/s, done.
    Total 3 (delta 1), reused 0 (delta 0)
    remote: Resolving deltas: 100% (1/1), completed with 1 local object.
    remote: This repository moved. Please use the new location:
    remote:   https://github.com/Bateyjosue/Git-Exercise.git
    remote: 
    remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
    remote:      https://github.com/Bateyjosue/Git-Exercise/pull/new/ft/faq-page
    remote: 
    To https://github.com/Bateyjosue/bundle1-exercise1.git
    * [new branch]      ft/faq-page -> ft/faq-page
    Branch 'ft/faq-page' set up to track remote branch 'ft/faq-page' from 'origin'.

  jb-dev% git revert  7649b1d      
    Removing team.html
    [ft/team-page e09b471] Revert "Add Team page"
    1 file changed, 14 deletions(-)
    delete mode 100644 team.html
```
