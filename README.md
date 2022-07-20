# The lowdown on Git

$ git clone url_of_your_remote_repository   # Clone a repository from a remote repository
$ git add file1 file2    # will add those two files to the index if they were modified
$ git commit -m "Meaningful commit message"   # will commit those two files (locally)
$ git add .   # will add all of the modified files to the index at once
$ git commit -m "Other meaningful commit message"   # will commit all of those files together
$ git push origin master   # send all commit to the remote server

#On a branch

$ git branch my_feature   # Creating the branch
$ git checkout my_feature   # Changing the codebase so that we're on that branch now
$ git checkout -b my_feature   # This does the two previous operations in one ;)
$ git add file1 file2
$ git commit -m "Meaningful commit message"   # We didn't just commit this on the master branch like last time, but on the my_feature one
$ git add .
$ git commit -m "Other meaningful commit message"
$ git push origin my_feature   # Notice: we're not pushing master anymore, you just create a new remote branch

#Next time you want to work on that branch, you should probably do this first:

$ git checkout my_feature   # Just making sure you're currently on the right branch!
$ git pull origin my_feature   # Pulling what your coworkers have done so far.

#And when you’re done with the whole feature and want to merge it to master:

$ git checkout master
$ git merge my_feature

#One other pretty neat thing: if you have a non-Git directory in your computer, and you want to turn it into a Git repository, it’s that easy:

$ git init   # You're done!
$ git remote add origin url_of_your_git_server   # So that you can push your code somewhere.

#When you’re in a Git repository, and want to know which files are modified but not in the index, and those that are modified and are in the index, you can run:

$ git status

Git provides many more abilities, such as rewriting pieces of the history of the project if you feel the commits were not meaningful enough, displaying the history in visually meaningful ways, …



#For instance, you should run this right now, and see how a complex history can be viewed really nicely:

$ git clone [https://github.com/loverajoel/jstips.git](https://github.com/loverajoel/jstips.git)   # You will need a GitHub account for this to work
$ cd jstips   # changing your directory into the one you just downloaded
$ git log --graph --pretty=tformat:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%an %cr)%Creset' --abbrev-commit --date=relative


#Interesting links about Git

[https://try.github.io]: an interactive tutorial for beginners.
[https://help.github.com/articles/good-resources-for-learning-git-and-github/]: a list of resources about Git, curated by GitHub.
[http://nvie.com/posts/a-successful-git-branching-model/]: once you master the technical tool, you have many ways to organize your branches according to your project. This very notorious article from 2010 introduces git-flow , a detailed proposal for organizing collective work with Git that is still the most common today. You should talk about that each time you start a collaborative project using Git.
[http://semver.org]: now that you can give version numbers to your code iterations, how should you number them? Semantic versioning is the most used versioning scheme.
[https://alx-intranet.hbtn.io/rltoken/AGmLa9Evzc9MI8dP9SFOcQ]:
[https://alx-intranet.hbtn.io/rltoken/OAvUt-4nF_R3xb_cC20fqw]:




