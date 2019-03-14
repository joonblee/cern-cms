# cern-cms

## git study
'''
_command_:~/git-dir$ git init
Initialized empty Git repository in /home/joonbinlee/git-dir/.git/
_command_:~/git-dir$ ls -a
.  ..  .git
'''

## update my user name and email
'''
_command_:~/git-dir$ git config user.name joonblee
_command_:~/git-dir$ git config user.email joon.bin.lee@cern.ch
_command_:~/git-dir$ vi .git/config
'''
user name and email are updated

## clone
'''
_command_:~/git-dir$ git clone https://github.com/joonblee/cern-cms.git
Cloning into 'cern-cms'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
'''
'''
_command_:~/git-dir$ ls
cern-cms
'''

## check the git status
'''
_command_:~/git-dir$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        cern-cms/

nothing added to commit but untracked files present (use "git add" to track)
'''
'''
_command_:~/git-dir$ cd cern-cms/
_command_:~/git-dir/cern-cms$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
'''

## check git repository url
'''
_command_:~/git-dir/cern-cms$ git remote -v
origin  https://github.com/joonblee/cern-cms.git (fetch)
origin  https://github.com/joonblee/cern-cms.git (push)
'''

If you want to add or remove the repository, use below commands
'''
git remote add < name > <http:// ... .git>
git remote remove < name > <http:// ... .git>
'''

## Change my file
'''
_command_:~/git-dir/cern-cms$ vi README.md
'''
'''
_command_:~/git-dir/cern-cms$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
'''

## Ready to update modified file / add: I'll add the modification
'''
_command_:~/git-dir/cern-cms$ git add .
'''
'''
_command_:~/git-dir/cern-cms$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   README.md
'''

## commit: confirm modifications to add in the online repository
'''
_command_:~/git-dir/cern-cms$ git commit -m "modify README.md"
[master 4142741] modify README.md
 1 file changed, 2 insertions(+), 1 deletion(-)
'''
'''
_command_:~/git-dir/cern-cms$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
'''

## update the online repository
'''
_command_:~/git-dir/cern-cms$ git push origin master
Username for 'https://github.com': joonblee
Password for 'https://joonblee@github.com':
Counting objects: 3, done.
Writing objects: 100% (3/3), 274 bytes | 274.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/joonblee/cern-cms.git
   a4f2071..4142741  master -> master
'''

### Now it's uploaded
