
# Michael's Steps to Git and GitHub #


deploy to gh-pages is below

----------


**git checkout -b *feature1***

-     then do some work...
	
**git add -A**

**git commit -m "message"**

**git push**

- 	which pushed to the feature1 branch

**git checkout master**

- 	moved me back onto master,
- 	getting ready to push to GitHub
	
**git pull**

**git merge *feature1***

- 	merging my featured branch back into master

**git status**

-	which tell you everything is ok and ready

**git push**

-	pushes master

**git tag 	-a v1.2.1 	-m "message"**

**git push --tags**


======================================

I have a bunch of different readme's of Git and GitHub, from beginners level to advanced. 

- Introduction to Version Control with GIT
- Introduction to GitHub
- Introduction to Git and Github
- IntermediateGit
- GitHub
- git_branching
- git_resources

They are just different ones I picked up on my journey as a beginning developer. I should clean them up and remove duplicate and deadwood, but I don't care about this point. Maybe later. 




http://alblue.bandlem.com/2011/04/git-tip-of-week-tags.html
git tag example

If we want to make it as an annotated tag, we need to supply -a, and a message with -m
git tag -a v1.0.1 -m "adding some Bootstrap styling"

sooo
git add -A
git commit -m "message"
git push
git tag 		-a v1.0.1 		-m "message"
git push --tags


If you'd like to fetch them all, you can do git fetch --tags to pull them all in, or git fetch tag to pull a single one.

======================================

also
the **deploy to gh-pages** thing is somewhere

- git checkout gh-pages
- git merge master
- git push origin gh-pages
- git checkout master


----------
