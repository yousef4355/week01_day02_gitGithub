# Git Basics
---
## Objectives 
- Start use a git and initilize repository in order to track changes.
- Make a new branch to isolate your change.
- Replace new or chagned files into the staging area to prepare them for a commit.
- Edit and remove files from the staging area before a commit.
- Commit new and changed files to a git repository. 
- Know how to Fork, Clone and PR concept. 

---
## GIT != GITHUB
![](https://camo.githubusercontent.com/8eae8cdaf798730ba3aa9e1c2de283305a06443d28393a7cceb53b1d2253f972/687474703a2f2f312e62702e626c6f6773706f742e636f6d2f2d57593259704e72335736672f555936745a41632d4833492f4141414141414141424c592f784a3978337749593856382f733434302f476974687562322e706e67)

## Why Git
---
We're as developers needs to track our changes on code and files and collaborators with other developers. So we need to use Version Controll as GIT.
Git is the most commonly used version control system. Git tracks the changes you make to files, so you have a record of what has been done, and you can revert to specific versions should you ever need to. Git also makes collaboration easier, allowing changes by multiple people to all be merged into one source. 


## Git Repositories
A Git repository (or repo for short) contains all of the project files and the entire revision history. You’ll take an ordinary folder of files (such as a website’s root folder), and tell Git to make it a repository. This creates a .git subfolder, which contains all of the Git metadata for tracking changes.

On Unix-based operating systems such as macOS, files and folders that start with a period (.) are hidden, so you will not see the .git folder in the macOS Finder unless you show hidden files, but it’s there! You might be able to see it in some code editors.


## Setups
In your terminal enter the following two lines:
```
git config --global user.name "your_name"
git config --global user.email your_email
```

Then, generate an access token from Github using the following [guide](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)


## Basics steps used for git and github

1. Create a new repository on a local project and commit changes to Github:
Assume you have a project on a folder named **my_project** and you want to upload it on Github. First, create a repository on Github (assume its name is **new_github_repo**). Second, in your terminal, change the working directory to **my_project** folder and execute the following command: 

```
git init
git add .
git commit -m "commit message"
git remote add origin https://github.com/<your_user_name>/new_github_repo
git push origin master
```

`git init` will initalize a Git repository locally.

`git add .` will add the changes to prepare the content staged for the next commit. If you want to add the changes of a specific file only, use `git add "file_name"`

`git commit -m "commit message"` Create a new commit with a descriptive commit message that describes the changes 

`git remote add origin https://github.com/<your_user_name>/new_github_repo` Add a remote named **origin** for the repository at the specified URL. This way we can use the name **origin** whenever we want to refer to this URL.

`git push origin master` Update remote reference with name **origin** ( the Github repository in this case).


2. Clone an existing repository, edit it, and commit changes to Github:
Assume that there is a project on a Github repository named **github_repo** that is not available locally, and you want to modify it and commit the changes to Github again. 
First, if you do not have an access to update the repo, create your own copy to your github account using the **Fork** button on the top right of the Github repo. Then, change the working directory to the place you want the repo to be cloned on it and execute the following commands: 

```
git clone https://github.com/<your_user_name>/github_repo
git add .
git commit -m "commit message"
git push origin master
```

`git clone` will clone the content of the github repo into your local machine. You can then start editing it and add, commit, and push the changes. No need for `git remote` in this case as the remote repo is already added when cloned.


## Lab 1
- Fork this Github repo into your account
- clone the repo into your machine
- edit the name.txt file by erasing the content and adding your name
- push the changes to Github

## Lab 2
- Create a Folder in Desktop “buildings”.
- Go into the folder.
- Create the git repo.
- Create 4 folders named Building 1, Building 2, Building 3 and Building 4
- Git status
- Create a file called “index.html” inside of Building 1.
- Go one level up to the “buildings” folder.
- Git status
- Add changes to the repo.
- Do the initial commit.
- Git status.
- Do a git add and commit each time you create the index.html file on each building folder.
- Git Status.

## Resources
For more info, check [git documentation](https://git-scm.com/docs) and [git cheat sheet](https://education.github.com/git-cheat-sheet-education.pdf)