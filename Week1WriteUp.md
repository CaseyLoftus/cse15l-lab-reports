# Week 1 Lab Report
Casey Loftus
A16860039

## Installing VS Code
![](https://user-images.githubusercontent.com/114450184/193356225-17d167df-7d37-4e27-ae45-f05895f5c729.png)
* I already had VS Code installed on my computer from a previous course.
* This step is relatively self explanatory.

## Remotely Connecting
![](https://user-images.githubusercontent.com/114450184/193356739-688d6e39-cc07-4ec4-b2c7-5af2cc11aff5.png)
* I had to use the TA account becuase my account still does not work.
* To connect to your account use: ssh cs15lfa22id@ieng6.ucsd.edu

## Some Helpful Commands
![](https://user-images.githubusercontent.com/114450184/193357735-e6987d2d-6b09-4764-a2ce-0e82f94ede3f.png)
* These are some examples of commands I frequently used throughout this lab. I changed the working directory, listed the folder and files in the directory, added a folder, and printed the working directory. 

## Moving Files
![](https://user-images.githubusercontent.com/114450184/193360096-8d4283e1-7f6c-493b-ba09-dc49d62fc2fb.png)
* These are the commands needed to move a file from your local computer to a remote connection. 
* I additionally connected to the computer and ran the file: note the difference in output. 

## Setting an SSH Key
![](https://user-images.githubusercontent.com/114450184/193360619-caeebf44-9612-4641-a9c8-8faa905ed76a.png)
* In this screenshot, I follow the steps outlined in the lab description to set the SSH Key.
* Everything seems to work without error, however, when I attempted to use the key to move a file over with scp, I was still prompted with a password.
* I think this has something to do with multiple people using the TA account, given that so many people couldn't log in on their own. 
* The TA approved of the commands I was using, so you can refer to these.

## Optimizing Remote Running
![](https://user-images.githubusercontent.com/114450184/193363701-640a5dde-bbe0-4ce3-a27f-378bdf754f50.png)
* Since the key never worked, I wasn't really able to optimize.
* However, I can imagine it would be pretty easy to copy paste the lengthy scp command, and combine login and running commands and copy paste those as well, saving a lot of time.
