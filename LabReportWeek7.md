# Week 7 Lab Report
Casey Loftus
A16860039

# Part 1

## In DocSearchServer.java, change the name of the start parameter of getFiles, and all of its uses, to instead be called base.

* The complete list of commands used:
* /start\<enter\>cebase\<esc\>n.n.

/start\<enter\>
![](https://user-images.githubusercontent.com/114450184/201717315-a1f90142-fe5f-4e51-b9b2-93e8a7f49385.png)
* Moves the cursor to the first instance of start

ce
![](https://user-images.githubusercontent.com/114450184/201717359-aff2f590-88ad-45e9-aa97-737e885ec92c.png)
* Deletes the word under the cursor and enters insert mode

base
![](https://user-images.githubusercontent.com/114450184/201717397-b7194cfe-087d-4b57-bf73-3291af68a46a.png)
* Inserts base into the cursor location

\<esc\>n
![](https://user-images.githubusercontent.com/114450184/201717459-832297e6-4fdf-4562-86ce-cda4154a7e16.png)
* Exits insert mode into normal mode and moves the cursor to the next instance of start

.
![](https://user-images.githubusercontent.com/114450184/201717488-0c204f4b-fe96-41ac-abcc-9c557397b409.png)
* Completes the last commands executed, in this case cebase, which deletes start and enters base on the cursor

n.
![](https://user-images.githubusercontent.com/114450184/201717519-e5a125b0-68ed-4f91-bc7d-08c8b424fdee.png)
* Finds the final instance of start and replaces it with base.

# Part 2
* It took me 20 seconds to edit locally and scp the file over to the remote server.
* It took me 35 seconds to connect to the remote server and edit using vim.
* The majority of the time I spent for the first option was writing the commands, passwords, and running the script, as the actual edits took only a few seconds.
* On the second option I spent more time on the actual edits but there was less terminal use, as I was constantly connected to the remote server.
* I think I would generally prefer to use the first style, as I am much more familiar with editing code on visual studio code than in vim. Copying the file over will take the same amount of time no matter the edit, and I can always edit faster in vs code.
* More or less complicated code edits would certainly change this decision, as an easy edit like in this lab is easier to do in vim. However, complicated code edits would be faster in vs code.
