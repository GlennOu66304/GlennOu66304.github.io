---
layout: mypost
title: connect the git, github, and Visula studio together.
categories: [Git]
---

## connect the git, github, and Visula studio together.

### 1.How to connect the git, github, and Visula studio together.  
1.Creat a github project;  
2.Commad pale (from the Visualstudio setting or command + option + p shortcut );  
3.Git clone the github project into the local: Git clone and paste the github project url into the bar area;  
4.Then you need to select a place to install your project;  
5.Creat a [readme.md file] new file and put the code content into the code files and save it ;  
6.Go to the fork tab, add the commit message and click the select the tick logo to finish the tick;  
7.go to the refresh logo in the bottom and click that to push the change into the github.  
8.To allow the password issue, just type the mac computer password to authorise it happen.  

Reference link:  
instruction video: [Using Git with VS Code and Github](https://www.youtube.com/watch?v=9cMWR-EGFuY)  
password isue fix:[Updating credentials from the macOS Keychain](https://docs.github.com/en/github/using-git/updating-credentials-from-the-macos-keychain)  
### 2.How to fix that MBP could not use the git, github, visual studio connect together.
1.Shut down the internet connect with other device, only left the MBP connect with internet； 
2.Astrill VPN Launch the  “smart mode";  
3.[Configure Git to work over proxy](https://www.youtube.com/watch?v=ObWxMWNx_m8) 
### 3. Git config:
1.change your Git username and the email:  
```
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```
[1.6 Getting Started - First-Time Git Setup](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)  

2.check the git config changes:
```
$ git config --list
```
3.Command+Shift+Dot in the finder to show the hiden mac file, then according to the latest git.config file to change the git config.  
[See hidden files on Mac via Finder](https://setapp.com/how-to/show-hidden-files-on-mac#:~:text=See%20hidden%20files%20on%20Mac%20via%20Finder&text=In%20Finder%2C%20open%20up%20your,2%20to%20hide%20them%20again!) 
### 4.Adjust the Mac pro could not connect the"5G" wifi;  
1.You need to find out your MBP's 5G channel;  
[MacBook Pro not connecting to 5Ghz wifi signals at 36, 40, 44 and 48 Channels](https://discussions.apple.com/thread/250703297)  
2.Edit the channel in the router' internet seting online;  
You could find this adress on the router's back or front;  
For example:  
192.168.1.1 this address, I found it on the router's back , if I type it in the browser's search bar,it will become a router's website, then I will be able to locate the Wifi internet setting to change the 5G channel.You will find the detailed information on the router to fill the required informaton to login and change the information.  
http://192.168.1.1/  
[MacBook Pro not connecting to 5Ghz wifi signals at 36, 40, 44 and 48 Channels](https://discussions.apple.com/thread/250703297)   
[Mac doesn't detect 5 GHz Wifi network](https://www.youtube.com/watch?v=l40XQw4-TMw)  

### Learning resources:  
Udacity:[Github version contral](https://classroom.udacity.com/courses/ud123)  
Github:[Git in the datasciences](https://github.com/GlennOu66304/Data-Sciences-in-R/blob/R-Learning/3.github_Using/Folder%20and%20file.md)  
Youtube channel:[Data school](https://www.youtube.com/watch?v=ruieT3Nkg2M&ab_channel=DataSchool)  
Front endmaster:    
[Git and Github](https://frontendmasters.com/courses/web-development/git-and-github/)    
[Git In-depth](https://frontendmasters.com/courses/git-in-depth/)  
