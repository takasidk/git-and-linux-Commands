
# Git Concepts
with examples and references I used during projects\
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




 **Note:** *<> mentioned symbols will not be present in the code*\
 *markdown/md tutorial* refer-[here](https://commonmark.org/help/tutorial/index.html)
    
