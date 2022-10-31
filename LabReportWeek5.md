# Week 5 Lab Report
Casey Loftus
A16860039

## Less Options

**-N**
* This option creates line numbers for the less output. 
* This is helpful for locating where in the file useful information is. 
![](https://user-images.githubusercontent.com/114450184/199063766-76ff22b1-f834-4f73-b9e8-93183726c336.png)
![](https://user-images.githubusercontent.com/114450184/199063862-98000ad2-3e94-4926-8b93-5df4cbd821c8.png)

**-S**
* This option extends long file lines past the command line width limit, and allows the user to scroll horizontally to view the entire line. 
* This provides more flexibility for viewing options, rather than wrapping every long line.
![](https://user-images.githubusercontent.com/114450184/199064616-341e369b-d245-4fc0-a995-593f1e470005.png)
![](https://user-images.githubusercontent.com/114450184/199064676-88b296d7-eb7c-4cd2-b433-f609b45c1eb5.png)
![](https://user-images.githubusercontent.com/114450184/199064703-579c19a9-4bcb-42f9-9b30-12d017cd36fd.png)

**-E**
* The command option terminates the less interface upon scrolling to the end of the file, eliminating the need to press q if the entire contents has been viewed. 
```
less -E ./technical/911report/preface.txt
```

## Find Options

**-mindepth**
* Sets a floor for the depth of directory path for the file names printed.
* Helpful for maintaining a constant working directory, so printing files from different directory depths can be done without changing the working directory. 
```
find ./technical -mindepth 4
./technical/government/About_LSC/fo/fjs
```
* Created a folder and file with depth 4 to demonstrate the command only outputting files with the specified minimum depth.

**-empty**
```
find ./technical -empty
./technical/government/About_LSC/fo/fjs
./technical/biomed/what.txt
```
* Searches for empty folders and files. 
* Created two empty files in different paths to demonstrate. 

**-size**
```
find ./technical -size +0k -size -1k  
./technical
./technical/government
./technical/government/About_LSC
./technical/government/About_LSC/fo
./technical/government/Env_Prot_Agen
./technical/government/Alcohol_Problems
./technical/government/Post_Rate_Comm
./technical/plos/pmed.0020191.txt
./technical/plos/pmed.0020226.txt
./technical/911report
```
* This command allows you to specify a range of file sizes to search for in a directory. 
* In this example, I searched for files with size under 1 kilobyte.

## Grep Options

**-c**
```
grep -c  "security" ./technical/911report/chapter-1.txt
18
```
* This option outputs the number of lines in a file that contain the search query. 
* This is helpful for quickly monitoring specific changes to a file that contains output for something.

**-v**
```
grep -v "the" ./technical/911report/test6.txt 
where
g
```

* This option outputs the lines that do not contain the search query. 
* This is helpful for parsing files containing output that is very similar.

**-i**
```
grep -i "the" ./technical/911report/test6.txt
the 
The
```
* This option removes the default case sensitivity of grep.
* This could be helpful for searching files for specific information regardless of case.