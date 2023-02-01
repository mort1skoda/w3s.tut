## w3s.tut.git.txt.md
### an easy tutorial.

<pre>
git reflog
git reset --merge 56fadc2
git merge ctrl-alt
git rm --cached test.txt 
git checkout master 
git push -u origin master

</pre>


check version:
==============
<pre>
git --version
</pre>


configure git:
==============
let Git know who you are.
this is important for version control systems,
as each Git commit uses this information:

<pre>
git config --global user.name  "mort1skoda"
git config --global user.email "mort1skoda@gmail.com"
</pre>

Note: Use global to set the username and e-mail for every repository on your computer.
If you want to set the username/e-mail for just the current repo, you can remove global



### Note: Short status flags are:
###
    ?? - Untracked files
    A - Files added to stage
    M - Modified files
    D - Deleted files



create folder:
==========
let's create a new folder for our project:
<pre>
mkdir myproject
cd myproject
</pre>

Initialize Git:
=
<pre>
git init
</pre>

add files:
=
For this example, I am going to use a simple HTML file like this:
<pre>
<!DOCTYPE html>
<html>
<head>
<title>Hello World!</title>
</head>
<body>

<h1>Hello world!</h1>
<p>This is the first file in my new Git Repo.</p>

</body>
</html>
</pre>

And save it to our new folder as index.html.

<pre>
git status
</pre>

git status
On branch master

No commits yet

Untracked files:
  (use "git add ..." to include in what will be committed)
    index.html

nothing added to commit but untracked files present (use "git add" to track)

<pre>
git add index.html
</pre>


---

A README.md file that describes the repository (recommended for all repositories):
Example:
<pre>
# hello-world
Hello World repository for Git tutorial
This is an example repository for the Git tutoial on https://www.w3schools.com

This repository is built step by step in the tutorial.
</pre>

---

A basic external style sheet (bluestyle.css):
Example:
<pre>
body {
background-color: lightblue;
}

h1 {
color: navy;
margin-left: 20px;
}
</pre>


And update index.html to include the stylesheet:
Example:
<pre>
<!DOCTYPE html>
<html>
<head>
<title>Hello World!</title>
<link rel="stylesheet" href="bluestyle.css">
</head>
<body>

<h1>Hello world!</h1>
<p>This is the first file in my new Git Repo.</p>

</body>
</html>
</pre>

---

<pre>
git add -A
git status
git commit -m "First release of Hello World!"
</pre>

---

Let's add a small update to index.html:
Example:
<pre>
<!DOCTYPE html>
<html>
<head>
<title>Hello World!</title>
<link rel="stylesheet" href="bluestyle.css">
</head>
<body>

<h1>Hello world!</h1>
<p>This is the first file in my new Git Repo.</p>
<p>A new line in our file!</p>

</body>
</html>
</pre>

---

<pre>
git status --short
</pre>
   M index.html

I can use: git status -s  or
gs -s
  check my aliases: .bash_aliases
ag git

---

### Note: Short status flags are:
###
    ?? - Untracked files
    A - Files added to stage
    M - Modified files
    D - Deleted files

---

### add(staging environment) and commit in one go.
<pre>
git commit -a -m "Updated index.html with a new line"
</pre>

## Warning: Skipping the Staging Environment is not generally recommended.

## Skipping the stage step can sometimes make you include unwanted changes.

---

### Git Commit Log
To view the history of commits for a repository, you can use the log command:
Example:
<pre>
git log
</pre>

---

### Git Branch
Working with git branches
New Git Branch
Let add some new features to our index.html page.
We are working in our local repository, and we do not want to disturb or possibly wreck the main project.
So we create a new branch:
Example:
<pre>
git branch hello-world-images
</pre>

Let's confirm that we have created a new branch:
Example:
<pre>
git branch
</pre>



checkout is the command used to check out a branch. Moving us from the current branch, to the one specified at the end of the command:
Example
<pre>
git checkout hello-world-images
</pre>


### For this example, we added an image (img_hello_world.jpg) to the working folder and a line of code in the index.html file:
Example:
<pre>
<!DOCTYPE html>
<html>
<head>
<title>Hello World!</title>
<link rel="stylesheet" href="bluestyle.css">
</head>
<body>

<h1>Hello world!</h1>
<div><img src="img_hello_world.jpg" alt="Hello World from Space"
style="width:100%;max-width:960px"></div>
<p>This is the first file in my new Git Repo.</p>
<p>A new line in our file!</p>

</body>
</html>
</pre>


### So let's go through what happens here:

    There are changes to our index.html, but the file is not staged for commit
    img_hello_world.jpg is not tracked

So we need to add both files to the Staging Environment for this branch:
Example
<pre>
git add -A
</pre>



<pre>
git status
</pre>



### We are happy with our changes. So we will commit them to the branch:
Example:
<pre>
git commit -m "Added image to Hello World"
</pre>




### Note:

    Using the -b option on checkout will create a new branch, and move to it, if it does not exist

---


<pre>
ls
</pre>

We can see the new file img_hello_world.jpg, and if we open the html file, we can see the code has been altered. All is as it should be.
Now, let's see what happens when we change branch to master
Example:
<pre>
git checkout master
</pre>



### The new image is not a part of this branch. List the files in the current directory again:

    Example:

<pre>
ls
</pre>

README.md  bluestyle.css  index.html
img_hello_world.jpg is no longer there! And if we open the html file, we can see the code reverted to what it was before the alteration.
See how easy it is to work with branches? And how this allows you to work on different things?




