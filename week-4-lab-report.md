# Week 4 Lab Report

For this week's lab report, I will go through the steps for lab 7's competition tasks.

1,2,3. Setup
---

If this is your first time attempting the tasks, you can skip this section.
I still need to delete my existing fork of the github repository from my last practice session.


![setup](https://user-images.githubusercontent.com/122575873/221065713-2e7c0737-caf1-439c-a2de-abda5c007a0d.png)


Commands: `pwd`, `rm -r /home/linux/ieng6/cs15lwi23/cs15lwi23ahx/lab7`
Keys Pressed: Nothing special


I am logged into my account on ieng6 in the home directory. I will `pwd` from the command line to get the path and then add `/lab7` since it is the name of the repository I want to delete.
The -r option recursively goes through all the files in the given directory and deletes them. I press `y` several times to ensure everything is deleted. 


4. Log into ieng6
---

Please see [Week 1 Lab Report](https://mlb004.github.io/cse15l-lab-reports/week-1-lab-report) for instructions on how to log into the remote server. 


5. Clone fork
---

I made a fork of the desired repository and cloned it on the command line. Then, I `cd`'d into lab7. 


![clone fork](https://user-images.githubusercontent.com/122575873/221068520-4b8465e7-e711-4e35-b3b4-36556e832d95.png)


Commands: `git clone https://github.com/mlb004/lab7`, `cd lab7`
Keys Pressed: Nothing special


6. Run JUnit and show that tests fail
---

I copied and pasted the commands to compile and run the JUnit tests from [lab 3's page](https://ucsd-cse15l-w23.github.io/week/week3/) on the course website. As expected, there are failures. 


![junit1](https://user-images.githubusercontent.com/122575873/221069108-d723ace9-8409-47c2-8359-60c28e699761.png)


Commands: See above
Keys Pressed: ^C/^V for copy-pasting on Mac


7. Edit the code file to correct errors
---

From the command line, I used `nano` to open the text editor. Based on the JUnit failure message in the last step, I know that the error is within the merge method of `ListExamples.java`. I eventually find that instead of `index1` in the last while loop, it should be `index2`. 


![correction](https://user-images.githubusercontent.com/122575873/221069685-ff357a60-1c67-4185-a3dd-40676569e3c1.png)
![nano](https://user-images.githubusercontent.com/122575873/221070033-f9ab4e53-5c0e-4b3d-b0dd-11799c34ad64.png)


Commands: `nano ListExamples.java`, ^X to quit the text editor
Keys Pressed: *up down left right* arrow keys to navigate to where the error was

  
8. Run JUnit and show that tests pass 
---

I used the exact same compile and run commands as in Step #6 so I won't go over them again here. The important thing is that now the JUnit tests show as passed.
  
  
![junit2](https://user-images.githubusercontent.com/122575873/221070540-64c94e72-57ed-4977-8945-b1d9885383ed.png)

  
Commands: See above
Keys Pressed: Nothing special

 
9. Add, commit, push
---

Nothing much to describe here. I just used the commands add, commit (with commit message denoted by `-m`), and push on ListExamples.java the to save the edits I made to it.
I also used the command git status to show me the current state of my branch.


![add and commit](https://user-images.githubusercontent.com/122575873/221072696-544c533a-d5ba-4a2d-9dbb-7a3d02eeb869.png)
![push](https://user-images.githubusercontent.com/122575873/221072729-39083e10-2c43-4346-ab4f-d8953b69a0a5.png)


Here is the edited file on github.com:

![github](https://user-images.githubusercontent.com/122575873/221072914-5ca24f0a-baa5-4de9-b72d-9407e0468f86.png)


Commands: `git add ListExamples.java`, `git commit -m "update"`, `git status`, `git push -u origin main`
Keys Pressed: Nothing special
