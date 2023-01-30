# Installing VScode 
I visited [code.visualstudio.com](https://code.visualstudio.com/)

![Image](https://user-images.githubusercontent.com/57383573/212238996-beeec690-831f-4965-a254-632039eb4e35.png)

Next, I clicked this Download button in the top right corner of the window.

Last, I downloaded the Mac version for my Mac.

# Remotely Connecting on Mac
I opened a terminal in VSCode (Ctrl/Command + `)
I entered this command but with the zz replaced by the letters in your course specific account. 
```
ssh cs15lwi23zz@ieng6.ucsd.edu
```
I then got a message like this because this was my first time connecting.
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
![Image](https://user-images.githubusercontent.com/57383573/212238987-8ffa2ab3-799b-4d1a-9122-34fea666d9df.png)

All done! I connected my terminal to a computer in the CSE basement, and all of my commands would run on that computer. The *client* was my computer and the *server* was the computer in the basement.


# Trying Some Commands
First, I opened up the terminal using this command: ```CTRL + ` ```
To run the following command, I typed ```cd ~```. This was the output:

![Image](https://user-images.githubusercontent.com/57383573/212240806-7e7c73b6-026f-4834-97d8-8fb40576a60a.png)

I ran several other commands such as
```cd```,
```ls -lat```,
```ls -a```,
```ls /home/linux/ieng6/cs15lwi23/cs15lwi23aus``` ,
```cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/```, and
```cat /home/linux/ieng6/cs15lwi23/public/hello.txt```.
Permission was denied for the command, ```ls /home/linux/ieng6/cs15lwi23/cs15lwi23aus```, because the directory belonged to another group member, not me. ```ls -lat``` had an interesting output which listed out the contents of my profile's working directory. It was also interesting to see how ```cd``` and ```cd ~``` produced empty outputs. This is because change directory was not called to change the directory.
