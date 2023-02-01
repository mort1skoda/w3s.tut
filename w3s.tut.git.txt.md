## w3s.tut.git.txt.md
### an easy tutorial.


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





