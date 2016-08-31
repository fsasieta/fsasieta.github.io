---
layout: post
title: "How to make a simple webpage using Jekyll"
date: 2016-08-30 11:25:00 -0400
comments: true
category: computer science
---

After finishing setting up my portoflio website and blog, and being a little confused along
the way (by the hosting, not Jekyll, I'll explain what I mean later), 
I decided I would do my own writeup as to how to setup the page. In case anyone 
wants to do the same. I will go step by step on how to create a simple static website based
on github pages. A `static` website simply means that it will not have flashy elements that move
or interact with you. You will still be able to put comments using add-ons, etc. but this
eliminates the need to setup a server or a database, only focusing on the website code. 
We will be usingg [Jekyll][Jekyll], a static site generator made by github itself. Its pretty
to use and help you get started relatively quickly, while giving you the freedom to
customize your site and being completely free (yay!). 

The first thing to do is setup and environment to do this. Go to [github][github] and create
 an account,if you haven't already. After you finish setting up and account,
 [create][create-repo] the repository in github pages where the website will be.
 As the tutorial says, the name of the repository will be the name of the website, ie.
`your-username.github.io`. This is pretty simple, and after you set it up and go to your website
you should see only a `Hello World!` sticking out in the upper left corner of your website.

Now comes the more exciting part. we have a place where our website lives, but we do not have
he way to modify it or really do anything to do it. Now I am assuming at some point in your life
you have used the command line and you have a Mac or Linux operating system, since the next
part of the development will not work on Windows. I use the command line for almost any 
kind development, and it not difficult to do [basic things][basic-things] in it.
We wil also need a text editor to open our files. I use `vim`, but that may be a little hard 
to start with. [Nano][nano] is great for beginners. Many people I know use [Sublime][sublime],
 which is also a good choice. It says you have to pay, but you could just extend the use of your
 free trial. 
Alternatively you could just open a file in notepad and start editing it, but that may not be the
 best choice. Also, if you're using linux, make sure you have `ruby` installed (`ruby --version` 
on the terminal).

After deciding how you'll edit your code, open up your terminal and navigate to wherever you
want to put your website. Note: if you're working with a Mac and you've never used your terminal,
you will get a prompt telling you to install the developer tools for that as well. The process
is very simple, just say yes to the prompt. This will take a while though, so you may want to 
allot some time free for that. After that, head over to the location on your computer where 
you'd like your website code to live and be edited (but not hosted, github does that for us).

Here you will have to `clone` your repository. There is a great [page][clone-repo] 
to learn how to do that in github. after you are done you should have a new folder named
something like `username.github.io` visible in the terminal. Change directories so you are in it.
Here you'll want to run the commands:

{%highlight linenos%}
gem install jekyll bundler
jekyll new .
{% endhighlight linenos%}

If there is no issues, there should be a bunch of new stuff in your folder, just `ls` to view it.
Open a new tab in the terminal and run `jekyll serve` then fire up your browser and put
`localhost:4000` in the url address box. You should see a basic site with a bunch template
stuff that comes with it. Go to the terminal wher you ran the `jekyll serve` command and 
press `control-c` to end the process. We'll return to that in a second.

For now we have to make sure everything we have is saved on github.
In the same place where all you files are, run the commands:

{% highlight linenos    %}
git add --all
git commit -m "Initial commit."
git push origin master
{% endhighlight linenos %}

This will probably ask for your username and password, so type it in when required.
If you're new to git, a bit of an explanation is required. Whenever your on you own repository
and you make changes, it is wise to continuosly keep track of them. The way to keep track of all
of the changes you make to a file is to add any complete changes to a file to a `commit` and
then submit the commit (commit the commit?). The command `git add <name-of-file>` does that,
but you can also do `git add --all` if want to list every file at once.

The command `git commit -m "Initial commit"` is used to submit the current changes as a "saved
block" of changes. With any commit it is required to give a short description about it, which
is the reason for the `-m` and the subsequent message. a helpful commit message gives an
example of what you're trying to accomplish, but the first one is just to start the project, so 
`"Initial commit"` is fine.

Finally, you have `git push origin master` which uses the network to submit the changes to
github's servers to be published on the web. This particular commit makes the changes on the 
"master" branch of your repository, which is the one we are using here.
Which means that at this point you could start your browser and put `your-username.github.io` 
on the url address and be taken to your actual webpage.

And so you have now published your very own webpage. Be sure to change it from the base webpage
given at the installation! If you're confused, look at the directories `_posts`, `_about` and
file `_config.yml`. Exploring is the best way to learn!

In another post I'll show how to setup you page so that is has a custom domain, like
`your-name-here.com`, since at first that part was a little confusing. Thanks for reading!

If anything in this post seems confusing, please drop me an email and i'll make sure to
clarify it.


[github]: https://github.com
[create-repo]: https://pages.github.com 
[Jekyll]: http://jekyllrb.com
[basic-things]: http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything
[nano]: https://www.nano-editor.org
[sublime]: https://www.sublimetext.com
[clone-repo]: https://help.github.com/articles/cloning-a-repository/

