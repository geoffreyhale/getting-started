# Getting Started

The **Getting Started** project is an effort to clarify and streamline development workflow for (1) starting and (2) deploying new web application projects.

## Step 1 - Create Project

```
cd ~
mkdir new-project
cd new-project/
```

```
touch README.md
```

## Step 2 - Git

GitHub and Bitbucket are popular options for git.  GitHub is more popular.  Bitbucket offers free private repositories.  This guide currently uses GitHub.

### GitHub

**Add An Existing Project To GitHub**
[https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/)

1. Create a new repository on GitHub *without README, license, or gitignore files*.
2. 
```
git init
git add .
git commit -m "first commit"
git remote add origin <your-repository-url-here>
git push -u origin master
```

An example of <your-repository-url-here> is (the repository for this project):
https://github.com/geoffreyhale/getting-started.git

> If you want to ignore files on a local basis not on a project-basis - maybe you want to exclude the PhpStorm `.idea` files from your local workspace - you can use `.git/info/exclude`.