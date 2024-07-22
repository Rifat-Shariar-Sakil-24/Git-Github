![screenshot](images/1.png)


## Check Git Version
```sh
git --version
```
you'll see something like `git version 2.39.1.windows.1` <br>
or if the command is unrecognized then for windows, you've to install git from
<a> https://git-scm.com/download/win </a>
<hr>


## Git Configuration 
### For Global Setup
```aidl
git config --global user.name 'your_username'
```
```aidl
git config --global user.email 'your_email'
```



<br>
For Local Folder Setup 

```aidl
git config --local user.name 'your_username'
```
```aidl
git config --local user.email 'your_email'
```
<br>
<br>
Now, to check global git configuration, run:

```aidl
git config --global --list
```
you'll see something like below:
<br>
`filter.lfs.smudge=git-lfs smudge -- %f`<br>
`filter.lfs.process=git-lfs filter-process` <br>
`filter.lfs.required=true` <br>
`filter.lfs.clean=git-lfs clean -- %f`  <br>
`user.name=Rifat Shariar Sakil`   // `my username`<br>
`user.email=shariarsakil101@gmail.com` // `my email`<br> 
`core.editor=code --wait` // `default code editor VS Code was set` <br>
`init.defaultbranch=main`  // `default starting branch` `$main` `is chosen`<br>
<br>
or, for local git configuation run: 

```aidl
git config --local --list
```
<hr>









## Initialize Git

`navigate to your directory` 
<br> <br>
make sure no git is already initialized:
```aidl
git status
```
output: `fatal: not a git repository (or any of the parent directories): .git` <br>

Now, Initialize Git:
```aidl
git init
```
<hr>


<br>

## Dive Into Git


Basically:
`modify file` => `stage changes` => `commit changes`<br>

![screenshot](images/3.png)
![screenshot](images/4.png)
![screenshot](images/5.png)
![screenshot](images/6.png)

<br>
<br>

# Git Commit
`modify file` => `stage changes` => `commit changes`<br>
<br>
check for modifications to be staged:
```aidl
git status
```
<br>

now,
single file stage:
```aidl
git add filename.txt
```
<br>

multiple file Stage:
```aidl
git add filename1.txt filename2.txt
```

<br>

stage all changes at once:
```aidl
git add --all
```
<br>

now, again check status of all files:
```aidl
git status
```
<br>
commit staged changes:

```aidl
git commit -m 'commit message' 
```
<br>

git stage and commit in one-line:
```aidl
git commit -a -m 'commit message'
```
<br>

check git commit log:
```aidl
git log
```
or git log in oneline:
```aidl
git log --oneline
```

<hr>

<br>
<br>


$ git init


// start with git
$ touch index.txt

modify index file

// check status
$ git status


//start staging
$ git add index.txt
or (add all files to staging area)
$ git add --all


// start commit
$ git commit -m "commitMessage"



// add and commit in oneline
$ git commit -am "commitMessage"



// check git log
$ git log
or (for oneline git log history)
// git log --oneline

you can't commit without staging files

// for unstage
$ git rm --cached index.txt


modify => stage => commit  |=> sleep


//update last commit for forgotten file

$ git commit -m "someCommit"
$ git add forgotttenFile.txt
$ git commit --amend
now the editor will open up, and I'll update the commit message if needed and close the file




// Branch Merging
$ git branch
$ git branch experiment

$ git switch experiment
or
$ git checkout experiment


$ git switch -c experiment

$ git branch -v

// suppose you updated an existing file. without committing, you can't switch to another branch.
but you can switch to another branch if you add a non conflicting file. But the nonconflicting file
will follow you to the switched branch. 
   