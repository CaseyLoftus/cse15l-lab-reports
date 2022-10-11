# Week 1 Lab Report
Casey Loftus
A16860039

## Installing VS Code
![](https://user-images.githubusercontent.com/114450184/193356225-17d167df-7d37-4e27-ae45-f05895f5c729.png)
* Follow this link and download VS Code [VS Code](https://code.visualstudio.com/)
* I already had VS Code installed on my computer from a previous course.
* Follow the directions found in the linked website, and install the corresponding version suitable for your machine.

## Remotely Connecting
![](https://user-images.githubusercontent.com/114450184/193356739-688d6e39-cc07-4ec4-b2c7-5af2cc11aff5.png)
* I had to use the TA account becuase my account still does not work.
* To connect to your account use: ssh cs15lfa22**@ieng6.ucsd.edu
* Replace the asterisks with your specific account id, found with the [Accont Lookup Tool](https://sdacs.ucsd.edu/~icc/index.php)
* Type in the password to your accound when promted.
* When connected, you should see a confirmation similar to in the screenshot. Sometimes you will see a summary of log in attempts as well. 

## Some Helpful Commands
![](https://user-images.githubusercontent.com/114450184/193357735-e6987d2d-6b09-4764-a2ce-0e82f94ede3f.png)
* These are some examples of commands I frequently used throughout this lab. I changed the working directory, listed the folder and files in the directory, added a folder, and printed the working directory. 
* "pwd" prints the working directory
* "cd" changes the working directory to the path of whatever folder or file is referenced after in the command
* "ls" prints the folders and files in the working directory
* "mkdir" creates a folder

## Moving Files
![](https://user-images.githubusercontent.com/114450184/193360096-8d4283e1-7f6c-493b-ba09-dc49d62fc2fb.png)
* These are the commands needed to move a file from your local computer to a remote connection. 
* Use the "scp" command followed by the desired file and desired file destination.
* Make sure to use your specific account as previously mentioned.
* I additionally connected to the computer and ran the file: note the difference in output. 
* In order to run it, I had to change to working directory to the one specified in my "scp" command.

## Setting an SSH Key
![](https://user-images.githubusercontent.com/114450184/193360619-caeebf44-9612-4641-a9c8-8faa905ed76a.png)
* To create an ssh key, follow the command order outlined in the screenshot.
* It will automatically create the /.ssh/id_rsa path so do not do that manually. 
* You should see a "key" generate as in the screenshot.
* After this, create a new folder in the remote server called ".ssh" and copy the .pub file into it.
* Everything seems to work without error, however, when I attempted to use the key to move a file over with scp, I was still prompted with a password.
* I think this has something to do with multiple people using the TA account, given that so many people couldn't log in on their own. 
* The TA approved of the commands I was using, so you can refer to these.

## Optimizing Remote Running
![](https://user-images.githubusercontent.com/114450184/193363701-640a5dde-bbe0-4ce3-a27f-378bdf754f50.png)
* Since the key never worked, I wasn't really able to optimize.
* However, I can imagine it would be pretty easy to copy paste the lengthy scp command, and combine login and running commands and copy paste those as well, saving a lot of time.
