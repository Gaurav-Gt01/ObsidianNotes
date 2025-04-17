
- Download Git from the website 

- For verifying the installation 

git 

you should be getting a liost of commands . This means git is sucssfully installated in ur sysytem .

- Cloning a repository 
	git clone < link of the github you want to clone >

- Initializing a Git Repository 

git init 

This initailazes the folder to a git version control and any changes made in this are then recorded by the .git hidden folder .

- To see hidden folders we use the command 

ls -a 

- To check the status of the changes made we use the command 

git status 

The untracked files are the files who are not been added to the staging area and they are represenated in  red .
The files who are added to the staging area are in green . 

- To add the untracked files to the staging area we use the command :

git add < name of the file > 
This adds the specific file to the staging area 
or
git add . 
This adds all the files that are untracked to the staging area 

- To remove files from the staging area :

git restore --staging  < name of file > 

- To commit the changes you have made to the repository :
This means that all the changes will be now saved in the hostory of the repository and the command used is :

git commit -m" add a message "

-m represents that we add a message to the commit .

- To see all the hostory of commits made we can use the command 

git log 

- If we commit somthing and we want to go back to some previous version of the commit then :

git reset < hash id of the commit you want to go to > 

hash id is the big 20 digit alpha numeric thing that is written in front of the commit when we prompt git log .

The files that were commited after that are then again transferred to the staging area 

- Stashing the changes made :

If i have made changes to a file and it is currently tracked  and now i want to work with a clean slate but i have this file in which i have made changes to then to work with a clean slate we use the command :

git stash 
This command basically puts the changes to the backstage area 

To bring these changes to the staging area we use the command :

git stash pop 

To clear the backstage files we use the command 

git stash clear

- TO connect your local repository on your device to a remote github repository we use the command :

git remote add origin  < url of the github repo you want to connect your local older to >

Here , 
remote - means connecting to a remote thing like a github repo 
add - means adding 
origin - it is the name of your own account (sometimes we use upstream in case of origin when we fork someones other repository )

To verify that remote was added we use the command 

git remote -v
This should show url of the github(push) and url of github(fetch)

- To push something on github using git we use the command :

git push origin main 
main is the name of the brach we are pushing our commit to 

- Branches in github :
In github we have various braches and the default branch is called as the main / master branch . 
Whenever we are making any changes in a big coebase we should always create a seperate branch on which we commit our changes . 
This is done because if there are any errors in the commit made then the main brach is not affected .
To create a brach we use the command :

git brach < name of the new brach >

Head is the pointer to the brach your commits would be made on .  
To switch to a different brach we can use the command :

git checkout < name of the brach you want to swicth your head to >

- When you have forked someone others github repository and have it cloned and you want to add from where it is forked it is called as the upstream url . 
So similar to adding / connecting your local repository to the remote repository you can do this by using the command :

git remote add upstream < url of the github from where you have forked the repo >

- Pull requests :
whenever we fork a repository and make changes to a brach that we have created other than the main branch and then when we want it to merge to the main brach we need to raise / create a pull request on the github . The github automatically prompts to create a pull request for a brach .
furthur if a single brach has raised a PR and then we do some other commit and push to the same brach then that commit is automatically added in the pull request as ONE BRACH CAN hAVE ONLY ONE PULL REQUEST OPEN and so for adding some other feature we should always create another brach .

- If i want to remove a commit after pushing  i need to copy the 20 digit alpha numeric number of the commit i want to be in then after that i need to do 

git reset < hash id >
By doing this i remove the commit from my local repository and now when i need to push it to github i cannot do it normally as it has the commit so i need to force push it .

git push origin < branch name > -f 

- To keep your repository  up to date with the changes made in the upstream branch we use the command :

git pull upstream < name of the branch you want to merge with > 

This command executes two commands that are :

git fetch upstream main 
This gets the latest changes from the main brach of the upstream repository 

git merge upstream/< branch >
This merges those fetched changes to the < branch > of your repository .


- To merge selected commits in a single commit we use the command :

git rebase -i < hash code of the commit above which you want to merge the selected commits >

-i represents interactive environemnt 

This opens up a interactive environment where all the commits above the hash code commits are there and it is written either pick or squash represented by s .
What pick is that it is a dfferent commit and squash is that all the commits below a pick who are squash are squashed in the pick above them and is created in a single commit .

To exit the interacive environment we use the command :x and then we can type a message for the new merged commit .