# DEVOPSLAB

**Create the New Repository for Lab Assignment**

****Assignement 1 ****

**1. Go to the Physical Path and Set the Current Working Directory**
Navigate to C:\KCSWorks\DevOps:

cd C:\KCSWorks\DevOps

**2. Clone the Git Repository Using HTTP URL**

Clone the repository from GitHub:
 git clone https://github.com/NAVIN132/DEVOPSLAB.git
 
This will create a DEVOPSLAB directory, and inside it, there will be a .git folder that tracks the repository.

**3. Change the Working Directory and Verify the Status of the Main Branch**

Change the directory to the DEVOPSLAB folder and check the status of the main branch:

cd DEVOPSLAB
git status

**4. Check the Git Log to Ensure All Objects are Received**

To make sure all objects (commits, branches, etc.) are received from the repository:
git log

**5. Create a New Branch (feature1)**

Create a new branch called feature1:
git branch feature1

**6. Switch to the feature1 Branch**
   
Switch from the main branch to the feature1 branch:

git checkout feature1
Alternatively, you can create and switch to the new branch in one command:

git checkout -b feature1

**7. Create a New File (index.html) in the feature1 Branch**

Create the index.html file in the feature1 branch:

touch index.html
**8. Add the File to the Staging Area**

Add the index.html file to the staging area:

git add index.html
**9. Commit the index.html File**

Commit the changes with a descriptive message:

git commit -m "add the index.html file"

**10. Check the Git Log and Git Status**

Check the log to verify the commit and status to see if there are any changes that need to be staged:

git log
git status

**11. Pull the Latest Changes (If Any) from the Remote Repository**

To ensure that your feature1 branch is up to date, pull the latest changes from the remote repository:

git pull

**12. Push the feature1 Branch to GitHub**

Push your changes to the feature1 branch on GitHub:

git push -u origin feature1

**13. Check the Git Status Again**

Verify the status to ensure everything is committed and pushed:

git status


******Assignment 2 ******


**1. Stash Your Uncommitted Changes**
Before you revert the commit, you want to make sure your uncommitted changes are saved. This can be done using git stash. This temporarily stores your uncommitted changes so you can work on the bug fix without losing your progress.

git stash
This command will save your changes to a "stash" and revert your working directory to the state of the last commit.

**2. Checkout to the Development Branch**
Make sure you're on the correct branch (in this case, development) where the buggy commit was made.


git checkout development
**3. Revert the Buggy Commit**
If you know the commit that introduced the bug, you can revert it using the commit hash. You can find the commit hash by running git log or using a tool like gitk:

git log

Once you have the commit hash (let’s assume it’s abc1234), run the following command to revert the commit:

git revert abc1234
This command creates a new commit that undoes the changes from the problematic commit. If there are merge conflicts, you will need to resolve them manually.

**4. Fix the Issue (If Needed)**
Once you've reverted the commit, you might want to manually fix any remaining issues that were introduced by that commit. Make any necessary code changes in your working directory.

After making changes, you can add and commit these fixes:


git add .
git commit -m "Fixed issue caused by commit abc1234"


**5. Apply Your Stashed Changes (If Needed)**
If you stashed changes earlier and want to bring them back into your working directory, use:


git stash pop
This will apply the changes you had stashed before. If there are any conflicts, Git will notify you, and you'll need to resolve them.

**6. Tag the Repository to Mark the Release**
Once everything is fixed and you're happy with the state of the repository, you can create a new tag to mark the release of a new version. Tags are typically used to mark significant points in history, like releases.

To create a lightweight tag (not attached to a specific commit message):


git tag v1.0.0
Or, if you'd like to add a message to the tag:


git tag -a v1.0.0 -m "Release version 1.0.0"
This will create a tag with the version number v1.0.0 to mark the current commit.

**7. Push the Reverted Commit and the Tag to Remote Repository**
Now, you need to push the changes (revert and fixes) along with the tag to the remote repository.

To push the changes to the development branch:


git push origin development
To push the new tag to the remote repository:

git push origin v1.0.0
If you stashed changes earlier and want to bring them back into your working directory, use:


git stash pop
This will apply the changes you had stashed before. If there are any conflicts, Git will notify you, and you'll need to resolve them.

******Assignment 3******

**1. Source already Pushed on after commit of First Assignemnt on git Hub.**

       git push -u origin feature1
       
**2. Go to GitHub and Create a Pull Request**
   
Once the feature branch is pushed to GitHub, follow these steps to create the pull request (PR):

Open the GitHub repository in your browser where the repository is hosted.

Navigate to the "Pull requests" tab at the top of the repository page.

Click the "New pull request" button.

Select the base and compare branches:

For the base branch, choose main (this is the branch you're merging into).
For the compare branch, select feature1 (or the name of your feature branch).
Review the changes:

GitHub will show you the changes between the main and feature1 branches. Make sure everything looks correct.
You can also add a description of the changes you've made in the PR text box (for example, explaining the feature you worked on or any other context the reviewer might need).
Create the pull request:

After reviewing, click the Create pull request button.
You can add a title and description for your PR. It's a good practice to add a meaningful description about what the PR is doing (e.g., "Add new feature to handle user authentication").
**3. Merge the Pull Request**
Once your PR is created, you may need someone to review the changes (depending on the repository's settings). After the review, you'll either:

Merge it yourself (if you have the necessary permissions), or
Wait for a project maintainer to review and merge the PR.
To merge the PR:

Click the "Merge pull request" button on GitHub.
Confirm the merge (you may be prompted to confirm the merge, depending on settings).
If necessary, delete the feature branch after merging (GitHub will typically give you an option to delete the branch).

**4. Pull the Latest Changes into Your Local Repository (Optional)**
After merging the pull request on GitHub, you can update your local main branch to reflect the changes from the remote repository.

Switch to your main branch:

git checkout main
Pull the latest changes from GitHub:

git pull origin main


