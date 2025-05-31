# Who is Mariam?

I am Mariam Yusuff, a creative writer diving into technical writing. Here are a few things I'd love to learn about next:
* SEO
* Software documentation (in-depth)
* CI/CD
* Other useful aspects of technical writing that can help me standout. 

I've written a few technical (and non-technical) articles. You can check out my baby steps here:  
1. [Hashnode](https://mwithheart.hashnode.dev/machine-learning-a-beginners-guide)
2. [LinkedIn](https://linkedin.com/in/yusuff-mariam)  

## What Mariam learnt during the week
This is going to be a lot because I've learnt a lot this week. To make it brief, here's a bit of my jottings.  

Below, you'll read about:
* Some terminologies in Git & GitHub
* repositories
* cloning, deleting repositories and so much more.

### Some terminologies in Git & GitHub
Here are some terminologies that I had to look up to understand the class.  

**Directory**: A directory, in the context of computing and web technology, refers to a hierarchical structure that organizes files and other resources on a computer or network. It serves as a roadmap to help users locate specific data, applications, or services within a system

Alternate definition: A directory is a folder.  

Git has 3 main states tht your file can be in:
* Modified: You have changed the file but haven’t committed it to your database yet.
* Staged: You have marked a modified file in it current version version to go into your next commit snapshot.
* Committed: Committed means that the data is safely stored in your local database

**Staging area:**
The staging area is a file, generally contained in your Git directory, that stores information about what will go into your next commit. It's technical name in Git parlance is the “index”, but the phrase “staging area” works just as well

The basic Git workflow goes something like this:  

* You modify files in your working tree.  

* You selectively stage just those changes you want to be part of your next commit, which adds only those changes to the staging area.  

* You do a commit, which takes the files as they are in the staging area and stores that snapshot permanently to your Git directory.

* If a particular version of a file is in the Git directory, it’s considered committed. If it has been modified and was added to the staging area, it is staged. And if it was changed since it was checked out but has not been staged, it is modified.  

**Repository vs Directory**  
The repository is essentially the . git hidden folder inside the working directory (workspace). The working directory (workspace) is essentially your project folder.  

**Another Online Explanation**
**Working Directory:** Where you work on your files locally.  
**Staging Area (Index):** A temporary holding area where you choose changes to include in the next commit.  
**Repository:** Where all committed changes and project history are stored


## What we did in week 3 
### **Git & VS Code**
1. Installed git - I had it installed. SO I checked git version: ```git --version```
2. Created a directory in my GitHub Folder (under document) with mkdir “TechBootcamp”
TechBootcamp is the name of the new directory I made, the one I want to use to house my repos.
3. Back to VS Code. I opened the new TechBootcamp folder in my VS Code
4. I created index.html and style.css styles to mirror what the tutor did.
5. Then I did git init to create a hidden .git folder that will house my staged files. Notice that html and css files have a U (called flag U) in front of them meaning Untracked
6. Then use git add to add unsaved files to the temporary stage (staging area).
7. So if I want to add one after the other, I’ll type git add index.html, otherwise use git add . to add everything to staging area. 
8. Notice that the symbol in front of the index file changes to A (meaning it is in the staging area).
9. Then make git commit, it’ll commit it to your local repository.  

When you edit a document and Ctrl + S, it gets the M flag meaning modified. Then you can commit it. Then check status with git status.  
> ```gitlog```: Used to show commit history — so write detailed commit messages.

### Created a Remote origin (remote repo- GitHub)
1. Create new repo locally
2. Create repo in GitHub without Readme file or gitignore file with same name as local repo
3. Cloned GitHub repo with ```git clone https://github.com/MwithHeart/my-writing-project.git.``` (if no readme file or gitignore file was added) 
Or ```git remote add origin https://github.com/MwithHeart/my-writing-project.git```
5. Then in VS Code, ```git branch -M main```
6. Then checked branch in VS Code with git branch.
8. Then ```git push -u (pronounced flag U) origin main```. But after this time, you’ll only need to use git push.

#### To initialize a git repository 
1. Run git in it, use git add and git commit
2. Your GitHub repo is your remote repo
> Your repo on VS Code is your local repo. Remote Repo is the one on GitHub

### Branching & Merging
> Before resuming work on VS Code, do git pull first to avoid merge conflicts.

```*.gitignore*``` is useful when you do not want files to show online. Could be files that are susceptible to attack. .env files are those that contain sensitive information like private API keys. 

Create new files in your VS code and name them ```.gitignore``` and ```.env```
In the ```.gitignore``` file, type ```.env```. Immediately you save that, you realize that the env file that was flagged untracked will no longer be flagged.

### To Create Branch
Branching allows you to create separate versions of your project so you can work on different tasks or features inependently without affecting the main feature.  

#### Common Branching Strategies
main- stable production code
feature/new-button – new features
bugfix/hot-scroll – fix specific issues
release/ request payemnt – prepare for production
hotfix/login – urgent fixes for live systems.

Now, let’s Create Branch
1. Create a new branch with ```git checkout -b "feature/new-menu"```(You may or may not put the quotation marks). The b flag (-b) is very important.
2. Then type ```git branch``` and you’ll see that you have two branches.
3. After this, you can’t push the new branch to your remote repo on GitHub like that. 
4. So go to GitHub and create new branch over there, then push from VS Code with ```git push --set-upstream origin feature/new-menu```
5. Create pull request and there you go
6. When you’re done with the branch, you can delete the branch.  
But when you delete on GitHub, a git branch on VS Code will still show that branch.  
So first switch to another branch or main branch with git checkout main. Then ```git pull```.


> **Best Practice:** 
Commit small changes for each pull request. Changes should address something tangible but should be easy to review.
Always pull before working on your local repo. Merge conflicts are not always easy to resolve.

### Git Merge
**To merge locally (on VS Code):**   
You be in the branch you want to update (eg main), which you want to merge another branch with.
* ```git checkout main```
* ```git merge feature/new-menu```

### Delete Branch
Deleting branch on GitHub is easy.
* To delete on VS code: Use ```git branch -d delete feature/new-menu```
* To delete two branches, just put space in between both branch names

#### Delete local Repo
Use ```rm -rf bootcamp_repo``` 

### Cloning Repo  
Go to cmd and paste the link to the repo which you copied from GitHub.
Then cd into it
