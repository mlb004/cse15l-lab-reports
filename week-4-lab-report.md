# Week 4 Lab Report

For this week's lab report, I am going to walk you through lab 7's competition tasks.

Setup
---
If this is your first time attempting the tasks, you can skip this section.
However, as I have practiced them several times, I need to delete my existing fork of the github repository.

To delete existing fork: rm -r <pwd + repository name> (from the current directory)

Log into ieng6
---
See Week 1 lab report for steps on how to log into the remote server.

Clone fork
---
git clone "fork URL"
cd lab7

Run JUnit
---
Copy + paste JUnit commands from Week 3 with ListExamplesTests
Should print failures

Correct errors
---
nano ListExamples.java 
Edit merge method —> should be index2

Run JUnit (again)
---
Run JUnit again 
Should pass

Add, commit, push
---
git add ListExamples.java
git commit -m “commit message”
git push

(Exit to logout of ieng6)
