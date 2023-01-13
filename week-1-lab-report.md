# Week 1 Lab Report
This is a blog post detailing how to install VS Code, remotely connect to the CSE basement server, and start using commands.

Installing VS Code
---
1. Go to the VS Code website: [VS Code](https://code.visualstudio.com/)
2. Follow the instructions for your operating system.
3. Open the VS Code window:
![Coding Window](https://user-images.githubusercontent.com/122575873/212215215-fbde234a-7b5c-47e4-b9ae-7df8b2b3f3b1.png)

Remotely Connecting to the Server
---
1. Open a new terminal in VS Code by selecting Terminal --> New Terminal.
2. Enter `ssh cs15lwi23____@ieng6.ucsd.edu`, where the blank is the letters in your CSE 15L account.
*look up your account [here](https://sdacs.ucsd.edu/~icc/index.php)*
3. If you're connecting to the server for the first time, you will usually see a message like
`The authenticity of host`...`can't be established.`
`RSA key fingerprint is`...
`Are you sure you want to continue connecting (yes/no/[fingerprint])?`
You will want to say yes to this message.
**If you connect to the server on a regular basis, you might be at a security risk if you keep seeing this message.**
4. Enter your password when prompted. **Even if you don't see the cursor move or letters appear while you're typing, the password is still registering.**
5. Now your terminal should be connected to a computer in the CSE building! 

This is a visual after login:
![Image](https://user-images.githubusercontent.com/122575873/212230037-87c0752b-81a2-4533-872b-db1f4ff024eb.png)


*If at any point you want to leave the remote server, just run `exit`.*

Using Commands
---
1. You can now start to experiment with commands like `cd`, `ls`, `pwd`, `mkdir`, and `cp`. Some might produce error messages at this point if the directory isn't defined.
2. You can also try `cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/` and `cat /home/linux/ieng6/cs15lwi23/public/hello.txt`. 

## Examples
![Image](https://user-images.githubusercontent.com/122575873/212230083-a9a16d86-0bd7-406a-a010-5d17291e48fb.png)
