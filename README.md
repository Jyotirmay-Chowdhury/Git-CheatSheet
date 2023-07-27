# Git Contents 

# Git Get Started
1. Git New Files
2. Git Staging Environment
3. Git Commit
4. Git Help
5. Git Branch
6. Git Branch Merge

# Git and GitHub
1. GitHub Get Started
2. GitHub Edit Code
3. Pull from GitHub
4. Push to GitHub
5. GitHub Branch
6. Pull Branch from GitHub
7. Push Branch to GitHub
8. GitHub Flow
9. GitHub Pages

# Git Contribute
1. GitHub Fork
2. Git Clone from GitHub
3. GitHub Send Pull Request

# Git Advanced
1. Git .gitignore
2. Git Security SSH
3. GitHub Add SSH

# Git Undo
1. Git Revert
2. Git Reset
3. Git Amend
	





# Git Get Started:
1) Get Started:-->


To check the Version of the Git use this command in cmd or Terminal.


---> git --version
Output---> git version 2.30.2.windows.1


To Configure Git
Now let Git know who you are. 
This is important for version control systems, as each Git commit uses this information:


local user:  git config --global user.name "Git-test"
local user:  git config --global user.email "test@git.com"


# Creating Git Folder:


local user: mkdir myproject   —> Make a directory of folder name is myproject
local user: cd myproject      


#Initialize Git


Once you have navigated to the correct folder, you can initialize Git on that folder:
--> git init
 
(Initialize empty Git repository in /Users/user/myproject/.git)
	

For Eg:- Create an Html file that contains the heading Hello World and with Paragraph.
<!DOCTYPE html>
<html>
<head>
<title>Hello World!</title>
</head>
<body>
<h1>Hello world!</h1>
<p>This is the first file in my new Git Repo.</p>
</body>
</html>
	And Save it as index.html
Let's go back to the terminal and list the files in our current working directory:


ls - List


Steps:- 
a) git init —> This is the step of initializing the file
b) git ls   —> Showing the list of the files or folder
c) git status  —> Status of the process
	



---------------------------------------------------------------------------------------------------------------------


2) Git Staging Environment:--->
As you are working, you may be adding, editing and removing files. But whenever you hit a milestone or finish a part of the work, you should add the files to a Staging Environment.
Staged files are files that are ready to be committed to the repository you are working on. You will learn more about Commit shortly.
For now, we are done working with index.html. So we can add it to the Staging Environment:


Steps:- 
a) git add index.html
b) git status
c) git add - -all   or   git add -A
	



























3) Git Commit:---> 


Since we have finished our work, we are ready to move from stage to commit for our repo.
Adding commits keeps track of our progress and changes as we work. Git considers each commit change point or "save point". It is a point in the project you can go back to if you find a bug, or want to make a change.


When we commit, we should always include a message.
a) git commit -m “First release of Hello world”
Git status - - short
b) Git Commit without Stage:- It is possible to commit changes directly, skipping the staging environment.
The -a option will automatically stage every changed, already tracked file.
- -> git commit -a -m “Update index.html with a new line”
git log (To view the history of commits for a repository)
	

















4) Git Help:--->


If you are having trouble remembering commands or options for commands, you can use Git help.


git command -help -  See all the available options for the specific command
git help --all -  See all possible commands
	

5) Git Branch:--->


In Git, a branch is a new/separate version of the main repository.


New Git Branch:- Now we created a new branch called "hello-world-images".  Let's confirm that we have created a new branch:
Eg:- a) git branch hello-world-images
b) git branch


c) git checkout hello-world-images


d) The edit in and IDE or VSCode and edit the file (index.html) or add a new file(image.jpg).
 
e) git checkout hello-world-images Switched to branch ‘hello-world-images’ —>  Checkout is the command used to check out a branch.
f) git status
g) git add - -all
h) git status
	

i) git commit -m “Added image to Hello World”
Switching Between Branches:- 


Steps:- 


a) ls
b) git checkout master
c) ls
	

Emergency Branch:- If you don’t want to mess with master directly and I do not want to mess with hello-world-images, then use this command:- 


Steps:- 


a) git checkout -b emergency-fix
b) git status (To Check The status)
c) git add index.html
	

6) Git Branch Merge:-->  


After emergency fix ready and then merge the master and emergency-fix branches.


Steps:- 
1. git checkout master   - Checkout the master branch


2. git merge emergency-fix    - Then merge with emergency branch
3. git branch -d emergency-fix   (-d for delete operations)   
- As master and emergency-fix are essentially the same now, we can delete emergency-fix, as it is no longer needed:




4. Merge Conflict:-
 It is a process in which github shows the duplicate file's data in the repository/branches and  that have to be resoled by using this process are:- 


1) git checkout hello-world-images        —-----(It will shift to this branch)
2) git add - - all          


3) git commit -m “added new image”
4) git checkout master        —--- (Swift to the master branch)
5) git merge hello-world-images
6) git status
7) Then after fixing the index.html file:
git add index.html
git status
git  commit -m “merged with hello-world-images after fixing conflicts”


8) Then delete the hello-world-images branch:-


git branch -d hello-world-images  
	





























---------------------------------------------------------------------------------------------------------------------
# Git and GitHub


1) GitHub Get Started:---> 
Steps:-


1) Create a new repository and use the HTTP Link of the repository.
2) git remote add origin https://github.com/xyz.git (Or - Link)
3) git push - -set-upsteam origin master


	

2) GitHub Edit Code:---> 


 It is an easy step in GitHub you can do it in the repository section. 
a) Readme.md file
b) and Commit Changes.


3) Pull from GitHub:--->  


Pull is the combination of 2 Different commands:-


1) fetch
2) merge


Steps:-


1) git fetch origin                                     —- It will fetch the origin data 
2) git log origin/master                            —-- It will obtain the history of branch
3) git diff origin/master                            —-- Differentiate between them.
4) git merge origin/master                      —-- It will merge the origin and master
5) git pull origin                                      —-- Git will pull in the origin
	





4) Push to GitHub:---> 


Let's try making some changes to our local git file (index.html) and pushing them to GitHub.
1) git commit -a -m “Updated index.html Resized image”
2) git push origin
3) git status
	

5) GitHub Branch:---> 


Create a new Branch on Github using master
On GitHub, access your repository and click the "master" branch button.
There you can create a new Branch. Type in a descriptive name, and click Create branch:
  



The branch should now be created and active. You can confirm which branch you are working on by looking at the branch button. See that it now says "html-skeleton" instead of "main"?
  





  



  





If you are happy with the change, add a comment that explains what you did, and click Commit changes.
You now have a new branch on GitHub, updated with some changes!






6) Pull Branch from GitHub:---> 
Pulling a branch from GitHub:- 
Now continue working on our new branch in our local Git.
Lets pull from our GitHub repository again so that our code is up-to-date:
1) git pull


2) git status


3) git branch 


4) git branch -a  — > So, we do not have the new branch on our local Git. But we know it is available on GitHub. So we can use the -a option to see all local and remote branches: (Note: branch -r is for remote branches only.)


We see that the branch html-skeleton is available remotely, but not on our local git. Let's check it out:
5) git checkout html-skeleton —> switch the branch


6) git pull                    —> And check if it is all up to date:


7) git branch                —- > Which branches do we have now, and where are we working from?
	

























7) Push Branch to GitHub:---> 


Let's try to create a new local branch, and push that to GitHub.


Start by creating a branch, like we did earlier:


1) git checkout -b update-readme       —-> creating a new branch 


2) git status         —--> checking the status


3) git add README.md    —> is modified but not added to the Staging Environment.


4) git status   —- > to check the status of the branch 


5) git commit -m “updated readme for GitHub Branches”  —> 


Then saves our changes


6) git push origin update-readme   —> 


Now push the branch from our local Git repository, to GitHub, where everyone can see the changes.
	











Go to GitHub, and confirm that the repository has a new branch:
In GitHub, we can now see the changes and merge them into the master branch if we approve it.
If you click the "Compare & pull request", you can go through the changes made and new files added:




  









In GitHub, we can now see the changes and merge them into the master branch if we approve it.
If you click the "Compare & pull request", you can go through the changes made and new files added:
  



Note: This comparison shows both the changes from update-readme and html-skeleton because we created the new branch FROM html-skeleton.


If the changes look good, you can go forward, creating a pull request:
  















A pull request is how you propose changes. You can ask some to review your changes or pull your contribution and merge it into their branch.
Since this is your own repository, you can  merge your pull request yourself:
  











The pull request will record the changes, which means you can go through them later to figure out the changes made.
The result should be something like this:
  

To keep the repo from getting overly complicated, you can delete the now unused branch by clicking "Delete branch".






  



8)GitHub Flow:---> 


The GitHub flow is a workflow designed to work well with Git and GitHub.
It focuses on branching and makes it possible for teams to experiment freely, and make deployments regularly.
The GitHub flow works like this:
1. Create a new Branch
2. Make changes and add Commits
3. Open a Pull Request
4. Review
5. Deploy
6. Merge






Create a New Branch
Branching is the key concept in Git. And it works around the rule that the master branch is ALWAYS deployable.
That means, if you want to try something new or experiment, you create a new branch! Branching gives you an environment where you can make changes without affecting the main branch.
When your new branch is ready, it can be reviewed, discussed, and merged with the main branch when ready.
When you make a new branch, you will (almost always) want to make it from the master branch.
Note: Keep in mind that you are working with others. Using descriptive names for new branches, so everyone can understand what is happening.
	

Make Changes and Add Commits
After the new branch is created, it is time to get to work. Make changes by adding, editing and deleting files. Whenever you reach a small milestone, add the changes to your branch by commit.
Adding commits keeps track of your work. Each commit should have a message explaining what has changed and why. Each commit becomes a part of the history of the branch, and a point you can revert back to if you need to.
Note: commit messages are very important! Let everyone know what has changed and why. Messages and comments make it so much easier for yourself and other people to keep track of changes.
	











Open a Pull Request
Pull requests are a key part of GitHub. A Pull Request notifies people you have changes ready for them to consider or review.
 You can ask others to review your changes or pull your contribution and merge it into their branch.
________________


Review
When a Pull Request is made, it can be reviewed by whoever has the proper access to the branch. This is where good discussions and review of the changes happen.
Pull Requests are designed to allow people to work together easily and produce better results together!
If you receive feedback and continue to improve your changes, you can push your changes with new commits, making further reviews possible.
Note: GitHub shows new commit and feedback in the "unified Pull Request view".
	

Deploy
When the pull request has been reviewed and everything looks good, it is time for the final testing. GitHub allows you to deploy from a branch for final testing in production before merging with the master branch.
If any issues arise, you can undo the changes by deploying the master branch into production again!
Note: Teams often have dedicated testing environments used for deploying branches.
	

Merge
After exhaustive testing, you can merge the code into the master branch!
Pull Requests keep records of changes to your code, and if you commented and named changes well, you can go back and understand why changes and decisions were made.
Note: You can add keywords to your pull request for easier searching!
	

9)GitHub Pages:---> 


Host Your Page on GitHub
With GitHub pages, GitHub allows you to host a webpage from your repository. Let's try to use GitHub Pages to host our repository.
Create a New Repository
Start by signing in to GitHub. GitHub pages need a special name and setup to work, so we start by creating a new repository:
  





  

Push Local Repository to GitHub Pages
We add this new repository as a remote for our local repository, we are calling it gh-page (for GitHub Pages).
Copy the URL from here:
  







And add it as a new remote:
git remote add gh-page https://github.com/w3schools-test/w3schools-test.github.io.git


	

Make sure you are on the master branch, then push the master branch to the new remote:


User —> git push gh-page master
	

Note: If this is the first time you are connecting to GitHub, you will get some kind of notification to authenticate this connection.
	

Check that the new repository has received all the files:
  











Check Out Your Own GitHub Page
That looks good, now click the Settings menu and navigate to the Pages tab:


  





















---------------------------------------------------------------------------------------------------------------------


# Git Contribute


1)GitHub Fork:---> 


Add to Someone Else's Repository
At the heart of Git is collaboration. However, Git does not allow you to add code to someone else's repository without access rights.
In these next 3 chapters we will show you how to copy a repository, make changes to it, and suggest those changes be implemented to the original repository.
At the end of these chapters, you will have the opportunity to add a message to our public GitHub page: https://w3schools-test.github.io/
Fork a Repository
A fork is a copy of a repository. This is useful when you want to contribute to someone else's project or start your own project based on theirs.
fork is not a command in Git, but something offered in GitHub and other repository hosts. Let's start by logging in to GitHub, and fork our repository:
https://github.com/w3schools-test/w3schools-test.github.io
  



Now we have our own copy of w3schools-test.github.io:
  

2)Git Clone from GitHub:---> 
Clone a Fork from GitHub
Now we have our own fork, but only on GitHub. We also want a clone on our local Git to keep working on it.
A clone is a full copy of a repository, including all logging and versions of files.
Move back to the original repository, and click the green "Code" button to get the URL to clone:
  

Open your Git bash and clone the repository:
Git —> git clone https://github.com/w3schools-test/w3schools-test.github.io
	

Take a look in your file system, and you will see a new directory named after the cloned project:


Git—> ls


Navigate to the new directory, and check the status:


Git—-> a) cd w3school-test-github.io
b)  git status
c) git log
	Configuring Remotes
Basically, we have a full copy of a repository, whose origin we are not allowed to make changes to.
Let's see how the remotes of this Git is set up:
 git remote -V
	We see that origin is set up to the original "w3schools-test" repository, we also want to add our own fork.
First, we rename the original origin remote:
git remote rename origin upstream
git remote -v
	

Then fetch the URL of our own fork:
  



And add that as origin:


a) git remote add origin https://github/xyz/xyz.github.io.git
b) git remote -v
	Now we have 2 remotes:
* origin - our own fork, where we have read and write access
* upstream - the original, where we have read-only access
Now we are going to make some changes to the code. In the next chapter, we will cover how we suggest those changes to the original repository.


3)GitHub Send Pull Request:---> 


Push Changes to Our GitHub Fork
We have made a lot of changes to our local Git.
Now we push them to our GitHub fork:
commit the changes:
git push origin
	

Go to GitHub, and we see that the repository has a new commit. And we can send a Pull Request to the original repository:
  



Click that and create a pull request:
  



Remember to add an explanation for the administrators.
  



















Pull Request is sent:
  



Approving Pull Requests
Now any member with access can see the Pull Request when they see the original repository:
  











And they can see the proposed changes:
  

Comment on the changes and merge:
  

Confirm:
  

















And changes have been merged with master:
  

























---------------------------------------------------------------------------------------------------------------------


# Git Advanced


1)Git .gitignore:---> 


Git Ignore
When sharing your code with others, there are often files or parts of your project, you do not want to share.
Examples
* log files
* temporary files
* hidden files
* personal files
* etc.
Git can specify which files or parts of your project should be ignored by Git using a .gitignore file.
Git will not track files and folders specified in .gitignore. However, the .gitignore file itself IS tracked by Git.
Create .gitignore
To create a .gitignore file, go to the root of your local Git, and create it:
touch .gitignore
	Now open the file using a text editor.
We are just going to add two simple rules:
* Ignore any files with the .log extension
* Ignore everything in any directory named temp
Example:-
# ignore ALL .log files
*.log


# ignore ALL files in ANY directory named temp
temp/
	Now all .log files and anything in temp folders will be ignored by Git.
  

  

  

  

Local and Personal Git Ignore Rules
It is also possible to ignore files or folders but not show it in the distributed .gitignore file.
These kinds of ignores are specified in the .git/info/exclude file. It works the same way as .gitignore but are not shown to anyone else.








2)Git Security SSH:---> 


Git Security
Up to this point, we have used HTTPS to connect to our remote repository.
HTTPS will usually work just fine, but you should use SSH if you work with unsecured networks. And sometimes, a project will require that you use SSH.
________________


What is SSH
SSH is a secure shell network protocol that is used for network management, remote file transfer, and remote system access.
SSH uses a pair of SSH keys to establish an authenticated and encrypted secure network protocol. It allows for secure remote communication on unsecured open networks.
SSH keys are used to initiate a secure "handshake". When generating a set of keys, you will generate a "public" and "private" key.
The "public" key is the one you share with the remote party. Think of this more as the lock.
The "private" key is the one you keep for yourself in a secure place. Think of this as the key to the lock.
SSH keys are generated through a security algorithm. It is all very complicated, but it uses prime numbers, and large random numbers to make the public and private key.
It is created so that the public key can be derived from the private key, but not the other way around.
________________


Generating an SSH Key Pair
In the command line for Linux, Apple, and in the Git Bash for Windows, you can generate an SSH key.
Let's go through it, step by step.
Start by creating a new key, using your email as a label:
Eg:- 
ssh-keygen -t rsa -b 4096 -C "test@w3schools.com"
	

You will be prompted with the following through this creation:


Enter file in which to save the key (/c/Users/user/.ssh/id_rsa):
	

Select a file location, or press "Enter" to use the default file location.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again:
	Entering a secure passphrase will create an additional layer of security. Preventing anyone who gains access to the computer to use that key without the passphrase. However, it will require you to supply the passphrase anytime the SSH key is used.
Now we add this SSH key pair to the SSH-Agent (using the file location from above):
Eg:- 
ssh-add /Users/user/.ssh/id_rsa 
Enter passphrase for /Users/user/.ssh/id_rsa: 
Identity added: /Users/user/.ssh/id_rsa (test@w3schools.com)
	You will be prompted to supply the passphrase if you added one.
Now the SSH key pair is ready to use.
3)GitHub Add SSH:---> 


Copy the SSH Public Key
In the previous chapter, we created an SSH key pair.
Now we will use the clip < command to copy the public key to our clipboard:


Eg:- 
clip < /Users/user/.ssh/id_rsa.pub
	

Go to GitHub, navigate to the top left corner, click your profile, and select: Settings:


  

























Then select "SSH and GPG keys". and click the "New SSH key" button:
  



Select a title, and paste the public SSH key into the "Key" field, and click "Add SSH Key":
  









You will be prompted to supply your GitHub password.
You will see your new SSH key added:
  



Test SSH Connection to GitHub
Now we can test our connection via SSH to GitHub:
ssh -T git@github.com


Output:- The authenticity of host 'github.com (140.82.121.3)' can't be established. RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8. Are you sure you want to continue connecting (yes/no/[fingerprint])? yes Warning: Permanently added 'github.com,140.82.121.3' (RSA) to the list of known hosts. Hi w3schools-test! You've successfully authenticated, but GitHub does not provide shell access.
	

If the last line contains your username on GitHub, you are successfully authenticated!






Add New GitHub SSH Remote
Now we can add a new remote via SSH to our Git.


First, get the SSH address from our repository on GitHub:


  



Then use that address to add a new origin:
git remote add ssh-origin git@github.com:w3schools-test/hello-world.git
	



Note: You can change a remote origin from HTTPS to SSH with the command:
 git remote set-url remote-name git@github.com:username/repository.git


git remote set-url origin git@github.com:w3schools-test/hello-world.git
	















---------------------------------------------------------------------------------------------------------------------


# Git Undo


1) Git Revert:---> 


Git Revert
revert is the command we use when we want to take a previous commit and add it as a new commit, keeping the log intact.
Step 1: Find the previous commit:
  

	

Step 2: Use it to make a new commit:


  

	Let's make a new commit, where we have "accidentally" deleted a file:
Eg:- 
git commit -m "Just a regular update, definitely no accidents here..."
	

Now we have a part in our commit history we want to go back to. Let's try and do that with revert.
________________


Git Revert Find Commit in Log
First thing, we need to find the point we want to return to. To do that, we need to go through the log.
To avoid the very long log list, we are going to use the --oneline option, which gives just one line per commit showing:
* The first seven characters of the commit hash
* the commit message
So let's find the point we want to revert:
git log - - oneline
	

We want to revert to the previous commit: 52418f7 (HEAD -> master) Just a regular update, definitely no accidents here..., and we see that it is the latest commit.


Git Revert HEAD
We revert the latest commit using git revert HEAD (revert the latest change,  and then commit), adding the option --no-edit to skip the commit message editor (getting the default revert message):
a) git revert HEAD - - no-edit
b) git log - - oneline
	

We want to revert to the previous commit: 52418f7 (HEAD -> master) Just a regular update, definitely no accidents here..., and we see that it is the latest commit.


2) Git Reset:---> 


Git Reset
reset is the command we use when we want to move the repository back to a previous commit, discarding any changes made after that commit.
Step 1: Find the previous commit:
  

	

Step 2: Move the repository back to that step:


  

	

After the previous chapter, we have a part in our commit history we could go back to. Let's try and do that with reset.


Git Reset Find Commit in Log
First thing, we need to find the point we want to return to. To do that, we need to go through the log.
To avoid the very long log list, we are going to use the --oneline option, which gives just one line per commit showing:
* The first seven characters of the commit hash - this is what we need to refer to in our reset command.
* the commit message
So let's find the point we want to reset to:
a) git log - - online
	

We want to return to the commit: 9a9add8 (origin/master) Added .gitignore, the last one before we started to mess with things.


Git Reset
We reset our repository back to the specific commit using git reset commithash (commithash being the first 7 characters of the commit hash we found in the log):
git reset 9a9add8
	Now let's check the log again:
git log - - oneline
	









Warning: Messing with the commit history of a repository can be dangerous. It is usually ok to make these kinds of changes to your own local repository. However, you should avoid making changes that rewrite history to remote repositories, especially if others are working with them.
	

Git Undo Reset
Even though the commits are no longer showing up in the log, it is not removed from Git.
git reset e56ba1f
	Now let's check the log again:


git log - - oneline
	

























3) Git Amend:---> 
Git Reset
reset is the command we use when we want to move the repository back to a previous commit, discarding any changes made after that commit.
Step 1: Find the previous commit:
  

	



Step 2: Move the repository back to that step:
  

	

After the previous chapter, we have a part in our commit history we could go back to. Let's try and do that with reset.
Git Reset Find Commit in Log
First thing, we need to find the point we want to return to. To do that, we need to go through the log.
To avoid the very long log list, we are going to use the --oneline option, which gives just one line per commit showing:
* The first seven characters of the commit hash - this is what we need to refer to in our reset command.
* the commit message
So let's find the point we want to reset to:
Eg:- 
git log - - oneline
	We want to return to the commit: 9a9add8 (origin/master) Added .gitignore, the last one before we started to mess with things.
Git Reset
We reset our repository back to the specific commit using git reset commithash (commithash being the first 7 characters of the commit hash we found in the log):
Eg:- 
git reset 9a9add8
	Now let's check the log again:
git log - - oneline
	Git Undo Reset
Even though the commits are no longer showing up in the log, it is not removed from Git.
If you know the commit hash you can reset to it:
Git reset  e56ba1f
	Now let's check the log again:
git log – - oneline
	



---------------------------------------------------------------------------------------------------------------------


Git - Cheat Sheet Developed by Jyotirmay Chowdhury 🥰


Content Credit to w3Schools
