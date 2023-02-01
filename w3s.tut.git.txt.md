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

