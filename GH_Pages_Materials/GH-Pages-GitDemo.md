---
layout: default
title: 2. GitHub Desktop and Command Demo
parent: GitHub and GitHub Pages
has_children: false
nav_order: 2
---


# A general workflow for using Git and GitHub

### Overview  
This guide roughly follows along with the in-class demonstration. First, we will walk through GitHub, then cloning a repository using GitHub Desktop and making changes. 

**The main point here is to demonstrate the general clone-push-pull GitHub workflow.** 

## Working on GitHub.com  

### Create a new repository and make changes on GitHub

Step 1
{: .label .label-step}  
From your dashboard on GitHub.com, click the New button.  
![Click New](../content/img/git1.png)

Step 2
{: .label .label-step}  
1. Give the repo a name  
2. Check the Add ReadMe box  
3. Click Create Repository  
![Add meta](../content/img/git2.png)

Congrats! You've initialized a repository!  

### Edit README.md file  

Step 1
{: .label .label-step}  
Click the edit README button.  
![Edit button](../content/img/git3.png)


Step 2
{: .label .label-step}  
Add a new line to your README, then click Commit.
![edit readme](../content/img/git4.png)

Step 3
{: .label .label-step}  
Add a commit message, and click Commit to save the changes:
![Commit](../content/img/git5.png)  

Congrats. You've made an edit then committed it.  
![Updated page](../content/img/git6.png)


## GitHub Desktop Client

### First, we'll clone our repository to the local machine.  

Step 1
{: .label .label-step}
In GitHub Desktop, click the Clone button:  
![Settings](../content/img/git7.png)  

Step 2
{: .label .label-step}  
Select the example repository just created on GitHub.com, then click the Clone button:  
![Pages](../content/img/git8.png)  

Step 3
{: .label .label-step}  
In the Clone dialog box, choose URL, then select a destination folder. Be smart about where you save it... Click Clone:  
![branch](../content/img/git9.png)

Now you've downloaded the remote repository to your local machine.  
![branch](../content/img/git10.png)  

### Committing changes.  

Step 1
{: .label .label-step}
1. Use the File Explorer or Finder app to navigate to the directory holding your repository.  
2. Then create a new file: `newFile.txt`.  
3. Open the file, add a line with some text, and click save.   

Back in GitHub Desktop, note that changes to the files are tracked: 
![tracking changes](../content/img/git11.png)  

![tracking changes](../content/img/git12.png)  


Step 2
{: .label .label-step}  
1. Select the files you want to add commit changes to.  
2. Add a commit message  
3. Click commit  
![Commit](../content/img/git13.png)  


### Push changes to the remote repo on GitHub  
Step 1
{: .label .label-step}  
Just click Push Origin!  
![Push](../content/img/git14.png)  

Now, back on GitHub, the new files have been backed up and tracked.  
![Commits](../content/img/git15.png)  

### Pulling remote changes to the local repo:  

Often, changes are made to the remote, either by you on GitHub.com, or by a collaborator.  

Step 1  
{: .label .label-step}  
As we did before, navigate to the remote repo on GitHub.com and commit a change to one of the files.  

Step 2  
{: .label .label-step}  
Back on GitHub desktop, click Fetch Origin:  
![Fetch](../content/img/git16.png)  

Step 3  
{: .label .label-step}  
Now, simply press the Pull Origin button:  
![Fetch](../content/img/git17.png)  

Congrats! You've pulled remote changes down to your local repo!  

## Command line workflow:  

All of the above can be accomplished with the command line as long as you have Git installed. This is actually the more common workflow. If you're on Windows, the GitBash terminal/command interface comes with Git. On Mac, you can use the terminal app. Here is a basic example:  


### Cloning the repo:  

Step 1  
{: .label .label-step}
On your repository page on GitHub, click the Code button:  
![Cloning](../content/img/git18.png)  
You'll need this URL.  

Step 2  
{: .label .label-step}  
1. Now open your preferred terminal/command line interface, such as GitBash.  
2. Enter the command: ```git clone https://github.com/username/repo_name.git```.  
3. Of course, replace the ```username``` and ```repo_name``` with the actual ones.  
![Cloning](../content/img/git19.png)  
Upon completion, the remote repo will now be downloaded to your local machine.  

### Committing and pushing from the command line:  

Step 1  
{: .label .label-step}  
1. Next, modify any file in the repo as we did previously.  
2. Enter the ```git status``` command to see all modified or new files yet to be committed to the repo.  
![git status](../content/img/git20.png)  
In this example, you can see newFile.txt has been modified, but is not being tracked.  

Step 2  
{: .label .label-step}  
1. Use git add to add newFile.txt: ```git add newFile.txt```  
2. This "stages" the change, but does not yet commit. Think of this as clicking the check box as you do using the desktop app.  
![git add](../content/img/git21.png)  
3. Now use ```git status``` again to see files ready to commit:  
![git status](../content/img/git22.png)  
Note the file is now green. It is ready to commit.  
4. Now we will commit. You MUST add a commit message, like this:  
```git commit -m 'added a line to newFile.txt'```   
The ```-m``` is the "message flag"  

Your changes are now committed.  

Step 3
{: .label .label-step}  
Finally, we will push the changes to the remote repository on GitHub using: ```git push origin main```  
![git push](../content/img/git24.png)

Done! Go take a look at your remote repo and you'll see the changes have been pushed.  
