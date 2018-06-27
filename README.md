# Getting Started

The **Getting Started** project is an effort to clarify and streamline development workflow for (1) starting and (2) deploying new web applications.

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
git remote add origin <your-repository-url-here>
```

An example of <your-repository-url-here> is (the repository for this project):
https://github.com/geoffreyhale/getting-started.git

> If you want to ignore files on a local basis not on a project-basis - maybe you want to exclude the PhpStorm `.idea` files from your local workspace - you can use `.git/info/exclude`.

```
git add .
git commit -m "first commit"

git push -u origin master
```

## Step 3 - npm

Initialize npm with:

`npm init`

...and complete the terminal dialog.

This creates `package.json` which we will use later.

*@todo: explain `"main": "index.js"`*

## Step 4 (Optional) - ES6

If you want to be able to use ES6 setup the Babel transpiler:

`npm install --save babel-cli`

Create `.babelrc` and setup like so:

```
{ 
  "presets": ["es2015"]
}
```
`npm install --save babel-preset-es2015`

And create a custom start script for your project:

Add to `package.json`:

```
"scripts": {
    "start": "babel-node src/index.js",
    "build": "babel src/ -d build/",
    "production": "node build/index.js"
  }
```

**Test:**

Create `src/index.js` with:

```
console.log('hello world');
```

Run `npm run build` and `npm run production` in terminal.

As response we expect to see console log `hello world` in the terminal.

**Resources:**
- https://codeutopia.net/blog/2014/12/18/getting-started-with-using-es6-ecmascript-6/

