# Hello Y'all
### **This is a guide that I made for myself to understand git better; however, if you somehow found yourself on this page, welcome!**

Git Guide

### Getting Started

For me, git was never really taught too well even though I am studying at a high-ranked university, hence, I am making a document that summerizes the most important steps to setting up your git and GitHub

`git init` (initialize a branch) initializing a branch can be thought of like creating a folder. Git will track all your changes.

`git config --global init.defaultBranch <name> `(configure the initial branch name) here you can change the name of your branch, usually, it is set to 'master' or 'main' at first. 

Once you are inside a new folder, run `git init` that way git can track the changes you make inside this folder

`git log` (Shows all the commits you have made and their tag) You know when you mess something up or you added a little too much nonsense to your code, USE THIS. git log will show you all the different commits you have added. I hope you used good names to track your changes, because if not you might be screwed.

`git checkout <tag> `(You can use git checkout in combination with git log to move around your different commits) Now, when you do `git log`, you should see something that reads - commit 12345... - this is the commit number, if you want to go back and forth between different commits replace <tag> with that code ex. `git checkout 1234abc`

`git checkout main` (this command will take you to the latest commit within the main branch) this command can help you get back to the latest commit inside your main branch. Lets say you get a bit too lost in the sauce, just use this. If you arent in the main branch, use whatever branch name you are in, duhhh.

#### **How to add and modify your remote repo**
Now, first thing first repo stands for repository just like calc stands for calculator. Repo's are cool becuase thats how you show off all your cool projects, well assuming you make it public.

*First, make sure you create your repo in Github, do this by clicking the little plus sign in the upper right corner and selecting **New Repository**, giving it a name, and create*

`git add origin <gitURL>` Now, let us create your remote repo. Use the command shown with your corresponding git repo URL. This should be shown when you create the repo, or you can find it by clicking the green code dropdown and then copying it. If you somehow already have a remote repo under the name origin, you can either use a different name or remove it using `git remote rm origin`

`git status` git status will show you all the modified documents this way you can check what has been modified before adding it to the commit. You wouldn't want that ultra top secret sauce to accidentally get committed and pushed to your public repo now would you

There are many ways to add your modified files to your next commit:
`git add file.name` you add a single file by using git add and the file name ex. `git add main.c`

`git add ./` You can also add all the files you have modified in your directory using this command

`git add -A` Lastly, you can use git add -A to add all changes you have made, keep in mind this includes files outside of your current directory

`git commit -m 'message'` finally, you are commiting your work, congrats! This is the equivalant of saving your code under a new name called file_v1 except this way all you need to do it type a simple command.

`git push -u origin main` This command will push your commit to your remote repo. After entering this command you can go to your repo and see the changes you have made, pretty cool right?

### Branching

`git branch <branch_name>` This will create a new branch

`git checkout <branch_name>` Use this to move around your branches

If you want to create a branch and immediately enter it, use this:

`git checkout -b <feature-branch>`

Keep in mind that the new branch you create will contain the code of the place you are branching from. If I am on branch_v2 and I make another branch called branch_v3, it will contain the code from branch_v2 and nothing else, the code from my main branch will not transfer over unless you specify it through: `git branch <newBranch> <sourceBranch>`

When you return to your main branch, you will notice that the changes you have made in your feature branch have not been implemented in your main code yet. In order to implement your branch, you will have to create a pull request in github, and then in your main branch, you will have to call `git fetch` and then `git merge` only after fetching and then merging will your changes be made in main.


