# Git and GitHub

## Git

1. What is Git?
    - Git is a version control software
    - It keep track of code changes
    - It helps to collaboration in project
    - It is installed and maintained locally
    - It provides Command Line Interface(CLI)

2. What is GitHub?
    - GitHub is a hosting server where we can keep our git repository
    - It is maintained on cloud or web
    - It provides Graphical User Interface(GUI)


## Hot to set git environment and configuration

- Download and install git on your pc from  [Git](https://git-scm.com/downloads)
- Check git version:open cmd then use the command `git -v`.If git installed it will return a version number of git.

### Git Configuration

    1. Check all configuration options: git config
    2. set global user name and user email:
- set global user name: `git config --global user.name "username"`
- set global user email: `git config --global user.email "email"`
  3. list all git configuration:
  - list all the configuration: `git config --list`
  - list user name: `git config user.name`
  - list user email: `git config user.email`
  4. Change global username and email
  - Change global user name: `git config --global user.name "set new username"`
  - change global user email:`git config --global user.email "set new user_email`

## create git repository and adding new files
1. creating a git folder
- ls -a:list all files inside of a directory

```
    mkdir folder_name
    cd folder_name
    git init
```
- Example
```
    mkdir test
    cd test
    git init
    ls -a
```

2. adding new files in git folder
- git status: displays the state of the working directory and staging area

```
    ls -a
    echo > filename.extension
    git status
```
- Example
```
    echo > index.html
    echo write something inside the file > index.html
```

## How to add files in staging and remove files

1. adding files to staging area:
- `git add fileName` add a file from working directory to staging area
- `git add .` add all files of working directory to staging area
- `git rm --cached fileName` unstage a file from staging area
- `git diff` checking the difference of a staged file
- `git restore fileName` restore the file

## commit and uncommit
- `git commit -m "message"` move the file to local repository from staging area
- `git log` check the commit history
- `git`

## git HEAD and undo theory
- `git log --oneline`
- `git show`
- `git show HEAD^`
- ` git show commit-id`
- `git checkout commit-id`
- `git checkout master`

## Git Ignore
- create a `.gitignore` file and add the things we do not want to add in the stagging area
- Inside `.gitignore` we can keep secret files, hidden files, temporary files, log files
- `secret.txt` secret.txt wil be ignored
- `*.txt` ignore all files with `.txt` extension
- `!main.txt` ignore all files with `.txt` extension without `main.txt`
- `test?.txt` ignore all files like `test1.txt, test2.txt`
- `temp/` all the file in temp folder will be ignored


## How to create github repository and commits

- sign in to our github account
- create a git repository

## README.md
- Everything you need to know about `README.md` is discussed in the video.
- 6 heading levels. number of hashes define heading levels. check the following example
    - `# heading 1`
    - `## heading 2`
    - `## heading 3`
- bold syntax: `**Hello World**`
- italic syntax: `_Hello World_`
- Strikethrouh syntax: `~~hello world~~`
- Single line code syntax: `place code inside backticks`
- Multiple line code syntax:```place code inside three open and closing backticks```
- Ordered list syntax:
    - ```
            1. HTML5
            2. CSS3
                1. Fundamental
                2. CSS Architecture - BEM
                3. CSS Preprocessor - SASS
            3.JavaScript
    ```

- Unordered List syntax:

```
    - HTML5
    - CSS3
        - Fundamental
        - CSS Architecture - BEM
        -  CSS Preprocessor - SASS
    - JavaScript

```

- Task List:

```
    - [x] Task One
    - [x] Task Two
    - [X] Task Three
```

- Adding Link

```
    <!-- automatic link -->
    https://github.com/mstsurnalyakter

    <!-- markdown link syntax -->
     [title](link)
     [mstsurnalyakter](https://github.com/mstsurnalyakter)

```

- Adding table

```
       table syntax
   | heading1 | heading2 |
   | ----- | ----- |
   | data1 | data2 |
   | data3 | data4 |
   | data5 | data6 |
```

## Connecting local repository to remote repository

- check remote connection `git remote` or `git remote -v`
- `git remote and name remote_url`
    - example:`git remote add origin http://..`
    - to clone a remote repository:`git clone remote_url`

## Push and Pull
- push a branch `git push -u origin branch_name`
- push all branches `git push --all`
- pull from repository: `git pull` which is equivalent to git fetch + git merge

## branching and merging
- Branch is new and separate branch `master/main` repository
- Create a branch `git branch branch_name`
- List branches `git branch`
- List all remote branches `git branch -r`
- List all local and remote branches `git branch -a`
- move to a branch `git checkout branch_name`
- create and move to branch `git checkout -b branch_name`
- delete a branch: `git branch -d branch_name`
- merge branches:
```
    git checkout branchName
    git merge branchName
```
- `git log --oneline --all --graph`