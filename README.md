# Test1
This is a demo repo. I'll use it for a demo.

# Common Git Commands

git clone
git lol
git status
git add
git commit
git checkout
git branch
git branch -r
git checkout -b
git fetch
git pull
git push
git push -f
git push origin --delete
git help tag
git tag
git push --tag
git rebase master

# Merge Feature Branch
First, make sure master is up to date.

git fetch --prune
git checkout master
git rebase origin/master

Rebase from master.

git checkout feature/foo-bar
git rebase master

Merge into master.

git checkout master
git merge [--no-ff] feature/foo-bar
If the feature branch consists of only a single commit, leave out --no-ff.

Next, push the feature branch and merge commit. Pushing your feature branch may require -f. Use a git push -n first to see what you're about to push. Do not force push to master.

git push [-f] origin feature/foo-bar
git push origin master
Lastly, if you are not going to continue working on this branch, delete your local branch and the remote branch.

git push --delete origin feature/foo-bar
git branch -d feature/foo-bar

