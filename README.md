# git-commands :computer:	


> git log -2 --oneline

Gives you the latest two commits in oneline format. You can specity the log number of your choice. 

Example
```
65de67a fixed minor css issue
bab4e1e updated js code
```

```
git log -2 
```
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

```
git reset HEAD~1
```
Deletes the commit history and unstages the files from the previous commit. 

## For macOS
If you want to close the commit message window on the terminal, hit Escape key once you enter your commit message. 
Then, type `:wq!` and hit *Enter*
It will save your commit with the message entered. 
`:` enters the commandline mode when you press it after you hit the Escape key
`w` is write which means Save
`q` is quit