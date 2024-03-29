
# Git Concepts and Linux Commands 
With examples and references I used during projects\
##### Starting of repo:
`sudo apt-get install git`\
`git init`     intialises git functionality for ur local folder\
`git add .`    adds ur files to the for staging\
`git commit -m "comments" `   commit changes\
`git remote add origin <http link of ur repo on github>`  adding ur ref repo\
`git push`     finally push to ur repo\
`git help`\
`git status `   displays status of ur files of unchanged/changed files stagged files\

##### Merging:
merging refer- [here](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)\
merge error :unrelated history--\
fixing it up example: merging Implementation_Data_Structures-branch with our master here\
`git checkout Implementation_Data_Structures`\
`git commit -a -m "fixing error"`\
`git checkout master`\
~~`git merge Implementation_Data_Structures`~~  error\
~~`git pull origin master --allow-unrelated-histories`~~  error\
~~`git merge Implementation_Data_Structures`~~//error\
`git merge --allow-unrelated-histories master \Implementation_Data_Structures` **correct way**
##### Branching:
shows our branches= `git branch` \
checksout to the branch specified= `git checkout <your branch name>`\
create new branch and checkout= `git checkout -b <branch name>`\
shows branch origined data= `git branch -vv`\
deleting your branch= `git branch -d <branch name>` first checkout to your master\
force deleting branch=`git branch -D <branch name>` checkout to master first\
 
##### Updating apts(linux):
`sudo apt update`    Fetches the list of available updates\
`sudo apt upgrade`   Installs some updates; does not remove packages\
`sudo apt full-upgrade`     Installs updates; may also remove some packages, if needed\
`sudo apt autoremove`       Removes any old packages that are no longer needed\
When updating u can get errors:\
*Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3893*something like this\
`ps aux | grep -i apt` command to check if any program using apt. to update which is auto in all systems\
If you see that apt is being used by a program like apt.systemd.daily update,
This is a daemon that runs in the background and check for system updates automatically when you start your system.

##### Deleting complete application(linux)
`dpkg -l | grep mysql`      Lists all packages installed with name mysql\
`sudo apt-get purge mysql-client-core-8.0 mysql-server-8.0 mysql-server-core-8.0 python3-pymysql `       Will uninstall all those packages mentioned in command\
`sudo apt-get autoremove`   removes/deletes all files which are of no use and uninstalled\
`apt-get autoclean`  u can use this to clean any unwanted files

##### Deleting sensitive info from github
https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository \
https://stackoverflow.com/questions/872565/remove-sensitive-files-and-their-commits-from-git-history

`git filter-branch --force --index-filter "git rm --cached --ignore-unmatch PATH-TO-YOUR-FILE-WITH-SENSITIVE-DATA" --prune-empty --tag-name-filter cat -- --all`
`git push --force --verbose --dry-run`
`git push --force`

 **Note:** *<> mentioned symbols will not be present in the code*\
 *markdown/md tutorial* refer-[here](https://commonmark.org/help/tutorial/index.html)
        
          
                
                 
      
       
   
 
