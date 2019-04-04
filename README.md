# git-commands :computer:	


> git log -2 --oneline

Gives you the latest two commits in oneline format. You can specity the log number of your choice. 

Example
```
65de67a fixed minor css issue
bab4e1e updated js code
```

> git log -2 

Gives you latest two commits in the below format.

Example
```
commit 65de67acc0d57dc8fx69b5396450c47d26c54bb2
Author: John, Snow <john.snow@gmail.com>
Date:   Wed Jan 30 11:38:52 2019 -0600

    fixed minor css issue

commit bab4e1e9f44f7ba53fsb37859c2d8f1fd1de0924
Author: Ramsay, Gordon <ramsay.gordon@gmail.com>
Date:   Tue Jan 29 16:13:34 2019 -0600

    updated js code
```


> git reset HEAD~1

Deletes the commit history and unstages the files from the previous commit. In other words, it uncommits. 

## For macOS
If you want to close the commit message window on the terminal, hit Escape key once you enter your commit message. Then, type `:wq!` and hit *Enter*. It will save your commit with the message entered. 
- `:` enters the commandline mode when you press it after you hit the Escape key
- `w` is write which means Save
- `q` is quit

## Uploading your Local Repository Code to Remote Repository
1. Initialize your local repository with the `init` command
```
git init
```
2. Add your files to staging with the `add` command
```
git add . 
```
3. Commit your changes 
```
git commit -m "version 1.0"
```
4. Add your remote repository url. The below command will set your remote url 
```
git remote add origin REMOTE REPOSITORY URL ( HTTPS format )  
```
5. Verify the new remote url 
```
git remote -v
```
6. Push the code to your remote remository
```
git push -u origin master
```
<hr>

If you see this issue while pushing the code  

```
$ git push -u origin master
To https://bitbucket.org/xx/xxx.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://teckbyt@bitbucket.org/xx/xxx.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
```

<hr>

use git `pull` command with `--allow-unrelated-history` and push the code. 
```
git pull origin master --allow-unrelated-histories
```

## How to add remote URL to your local repository
Someday, you might come across a situtation where your project in one source code hosting platform will be migrated to other platform. In my case, the source code of our project has been migrated to GitLab from OneStash. So, you will need to change the remote URL of your local project.

First, check the remote URLs
```
git remote -v
```
Secondly, remove the previous remote URL
```
git remote remove origin 
```
Finally, add the current remote URL
```
git remote add origin <.git url of source code>
```
