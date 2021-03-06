# git study

## init: Initialized the git
```
_command_:~/git-dir$ git init
Initialized empty Git repository in /home/joonbinlee/git-dir/.git/
```
```
_command_:~/git-dir$ ls -a
.  ..  .git
```

## config: update my user name and email
```
_command_:~/git-dir$ git config user.name joonblee
```
```
_command_:~/git-dir$ git config user.email joon.bin.lee@cern.ch
```
```
_command_:~/git-dir$ vi .git/config
```
user name and email are updated

## clone
```
_command_:~/git-dir$ git clone https://github.com/joonblee/cern-cms.git
Cloning into 'cern-cms'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
```
```
_command_:~/git-dir$ ls
cern-cms
```

## status: check the git status
```
_command_:~/git-dir$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        cern-cms/

nothing added to commit but untracked files present (use "git add" to track)
```
```
_command_:~/git-dir$ cd cern-cms/
```
```
_command_:~/git-dir/cern-cms$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
```

## remote: check git repository url
```
_command_:~/git-dir/cern-cms$ git remote -v
origin  https://github.com/joonblee/cern-cms.git (fetch)
origin  https://github.com/joonblee/cern-cms.git (push)
```

If you want to add or remove the repository, use below commands
```
git remote add <name> <http:// ... .git>
git remote remove <name> <http:// ... .git>
```

## Change my file
```
_command_:~/git-dir/cern-cms$ vi README.md
```
```
_command_:~/git-dir/cern-cms$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

## add: Ready to update modified file (add the modification)
```
_command_:~/git-dir/cern-cms$ git add .
```
```
_command_:~/git-dir/cern-cms$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   README.md
```

## remove: remove a file
```
_command_:~/git-dir/cern-cms$ git rm -r --cached ~/<repo_name>/<file_name>
```

## commit: confirm modifications to add in the online repository
```
_command_:~/git-dir/cern-cms$ git commit -m "modify README.md"
[master 4142741] modify README.md
 1 file changed, 2 insertions(+), 1 deletion(-)
```
```
_command_:~/git-dir/cern-cms$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

## push: update the online repository
```
_command_:~/git-dir/cern-cms$ git push origin master
Username for 'https://github.com': joonblee
Password for 'https://joonblee@github.com':
Counting objects: 3, done.
Writing objects: 100% (3/3), 274 bytes | 274.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/joonblee/cern-cms.git
   a4f2071..4142741  master -> master
```

### Now the changes are uploaded

## 403 error
```
git remote set-url origin https://<username>@github.com/<username>/<repo-name>.git
```
Try to push again


# Write new repository

### 1) Make new repository in github homepage

### 2) Merge your local file into the git
```
$ git init
$ git config user.name <user_name>
$ git config user.email <full_email_address>
$ git add .
$ git commit -m "First commit"
$ git remote add origin https://github.com/joonblee/<repository_name>.git
$ git push -u origin master
```


# Re-update (modified content, untracked content) files
Check if you have any untracked content.
```
(After git init & config)
$ git status
      modified:   <file_name> (modified content, untracked content)
```

Re-update this untracked content.
```
$ git rm -rf --cached <file_name>
$ git add <file_name>
$ git commit -m "reupdate <file_name>"
$ git push origin master
```
