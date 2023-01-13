# Installing VScode 
1. I visited [Link](https://code.visualstudio.com/)
2. I clicked this Download button in the top right corner of the window.
3. Last, I downloaded the Mac version for my Mac. 

# Remotely Connecting on Mac
1. I opened a terminal in VSCode (Ctrl/Command + `)
![Image](https://user-images.githubusercontent.com/57383573/212238996-beeec690-831f-4965-a254-632039eb4e35.png)
2. I entered this command but with the zz replaced by the letters in your course specific account. 
```
ssh cs15lwi23zz@ieng6.ucsd.edu
```
3. I then got a message like this because this was my first time connecting.
```
⤇ ssh cs15lwi23zz@ieng6.ucsd.edu
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
```
Type ```yes```, press enter, give your password. Here's what the interaction should look like.
```
# On your client
⤇ ssh cs15lwi23zz@ieng6.ucsd.edu
The authenticity of host 'ieng6-202.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
Password:
```
```
# Now on remote server
Last login: Sun Jan  2 14:03:05 2022 from 107-217-10-235.lightspeed.sndgca.sbcglobal.net
quota: No filesystem specified.
Hello cs15lwi23zz, you are currently logged into ieng6-203.ucsd.edu

You are using 0% CPU on this system
```
![Image](
All done! I connected my terminal to a computer in the CSE basement, and all of my commands would run on that computer. The *client* was my computer and the *server* was the computer in the basement.


# Trying Some Commands
1. First, I opened up the terminal using this command: CTRL + `
2. To run the following command, I typed ```cd ~``` This was the output:
3. I tried several more commands, finding that i could not access the directory of another group member
