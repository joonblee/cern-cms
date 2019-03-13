# cern-cms

### git study ###
joonbinlee@joonbinlee-H97-D3H:~/git-dir$ git init
Initialized empty Git repository in /home/joonbinlee/git-dir/.git/
joonbinlee@joonbinlee-H97-D3H:~/git-dir$ ls -a
.  ..  .git

### update my user name and email
joonbinlee@joonbinlee-H97-D3H:~/git-dir$ git config user.name joonblee
joonbinlee@joonbinlee-H97-D3H:~/git-dir$ git config user.email joon.bin.lee@cern.ch
joonbinlee@joonbinlee-H97-D3H:~/git-dir$ vi .git/config
# user name and email are updated

### clone
joonbinlee@joonbinlee-H97-D3H:~/git-dir$ git clone https://github.com/joonblee/cern-cms.git
Cloning into 'cern-cms'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
joonbinlee@joonbinlee-H97-D3H:~/git-dir$ ls
cern-cms

### check the git status
joonbinlee@joonbinlee-H97-D3H:~/git-dir$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        cern-cms/

nothing added to commit but untracked files present (use "git add" to track)

joonbinlee@joonbinlee-H97-D3H:~/git-dir$ cd cern-cms/
joonbinlee@joonbinlee-H97-D3H:~/git-dir/cern-cms$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

### check git repository url
joonbinlee@joonbinlee-H97-D3H:~/git-dir/cern-cms$ git remote -v
origin  https://github.com/joonblee/cern-cms.git (fetch)
origin  https://github.com/joonblee/cern-cms.git (push)
# If you want to add or remove the repository, use below commands
git remote add <name> <http:// ... .git>
git remote remove <name> <http:// ... .git>

### Change my file
joonbinlee@joonbinlee-H97-D3H:~/git-dir/cern-cms$ vi README.md
joonbinlee@joonbinlee-H97-D3H:~/git-dir/cern-cms$ git status
On branch master
Your branch is up to date with 'origin/master'.

#Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

### Ready to update modified file / add: I'll add the modification
joonbinlee@joonbinlee-H97-D3H:~/git-dir/cern-cms$ git add .

joonbinlee@joonbinlee-H97-D3H:~/git-dir/cern-cms$ git status
On branch master
Your branch is up to date with 'origin/master'.

#Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   README.md

### commit: confirm modifications to add in the online repository
joonbinlee@joonbinlee-H97-D3H:~/git-dir/cern-cms$ git commit -m "modify README.md"
[master 4142741] modify README.md
 1 file changed, 2 insertions(+), 1 deletion(-)

joonbinlee@joonbinlee-H97-D3H:~/git-dir/cern-cms$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

### update the online repository
joonbinlee@joonbinlee-H97-D3H:~/git-dir/cern-cms$ git push origin master
Username for 'https://github.com': joonblee
Password for 'https://joonblee@github.com':
Counting objects: 3, done.
Writing objects: 100% (3/3), 274 bytes | 274.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/joonblee/cern-cms.git
   a4f2071..4142741  master -> master
# Now it's uploaded
