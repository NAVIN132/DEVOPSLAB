# DEVOPSLAB
Create the New Repository for Lab Assignment
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
