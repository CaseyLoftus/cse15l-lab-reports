# Week 5 Lab Report
Casey Loftus
A16860039


## Find Options

**-min/max depth**
* Sets a floor or ceiling for the depth of directory path for the file names printed.
* Helpful for maintaining a constant working directory, so printing files from different directory depths can be done without changing the working directory. 
```
find ./technical -mindepth 4
./technical/government/About_LSC/fo/fjs
```
* As shown in the path of this file, the depth from the /technical folder is 4, and since it is the only file with this depth it is the only file name printed.

```
find ./technical -mindepth 3 -maxdepth 5 
./technical/government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt
./technical/government/About_LSC/Progress_report.txt
./technical/government/About_LSC/Strategic_report.txt
./technical/government/About_LSC/fo/fjs
```
* In this example, there is both a floor and ceiling, and paths with different depths between these are printed.

```
find ./technical -maxdepth 1
./technical
./technical/government
./technical/plos
./technical/biomed
./technical/where
./technical/911report
```
* This example demonstrates that maxdepth limits the output to files and folders with a certain depth, so only these files and folders are printed.


**-empty**
```
find ./technical -empty
./technical/government/About_LSC/fo/fjs
./technical/biomed/what.txt
```
* Searches for empty folders and files. 
* Created two empty files in different paths to demonstrate.

```
find ./technical -empty
```
* When there are no empty files, there is no output. There is also no error thrown.

```
find ./technical -empty -mindepth 3
./technical/government/About_LSC/fo/fjs
```

* Used with mindepth to find empty files after a certain path depth.
* This command is useful for finding obsolete files.

**-size**

```
find ./technical -size 0k
./technical/government/About_LSC/fo/fjs
```
* This can be used to the same effect as -empty to find empty files of no size. 

```
find ./technical -size -2k 
./technical
./technical/government
./technical/government/About_LSC
./technical/government/About_LSC/fo
./technical/government/About_LSC/fo/fjs
./technical/government/Env_Prot_Agen
./technical/government/Alcohol_Problems
./technical/government/Post_Rate_Comm
./technical/government/Media/Helping_Hands.txt
./technical/government/Media/Campaign_Pays.txt
./technical/government/Media/Fire_Victims_Sue.txt
./technical/government/Media/Court_Keeps_Judge_From.txt
./technical/government/Media/It_Pays_to_Know.txt
./technical/government/Media/Self-Help_Website.txt
./technical/government/Media/Justice_requests.txt
./technical/government/Media/Wilmington_lawyer.txt
./technical/government/Media/Lawyer_Web_Survey.txt
./technical/plos/pmed.0020048.txt
./technical/plos/pmed.0020028.txt
./technical/plos/pmed.0020191.txt
./technical/plos/pmed.0020226.txt
./technical/plos/pmed.0020192.txt
./technical/plos/pmed.0020157.txt
./technical/plos/pmed.0020082.txt
./technical/plos/pmed.0020120.txt
./technical/911report
```
* This command can also be used to find files with size under a certain amount. 

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
* In this example, I searched for non empty files with size under 1 kilobyte. As shown, you can use this format to search for files within a certain file size range.
* In general, this is useful for finding outlier files: files with unusual size. 



