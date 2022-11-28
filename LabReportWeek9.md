# Lab Report 5
Casey Loftus
A16860039

## Your grade.sh in a code block

```
# Create your grading script here
set -e 
CPATH=".:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar"
rm -rf student-submission
git clone $1 student-submission 2> cloneout.txt
cd student-submission
if [[ ! -e ListExamples.java ]]
then 
    echo "ListExamples.java missing"
    exit 1
fi
cd ..
cp TestListExamples.java ./student-submission
cd ./student-submission
set +e
javac -cp $CPATH *.java 2> output.txt
if [[ $? -ne 0 ]]
then
    if grep -iq "TestListExamples.java" output.txt 
    then
        echo "Method header argument error!"
        exit 1
    fi
    echo "ListExamples.java did not compile!"
    exit 1
fi
java -cp $CPATH org.junit.runner.JUnitCore TestListExamples > TestOutput.txt
if [[ $? -eq 0 ]]
then
    echo "All tests pass. Full Score!"
fi
if grep -iq "merge" TestOutput.txt
then
    echo "Merge method incorrect!"
fi
```

## Three example screenshots
![](https://user-images.githubusercontent.com/114450184/204182220-94e782b1-0088-4099-a3fa-19881e14fd45.png)
![](https://user-images.githubusercontent.com/114450184/204182235-59bcc469-62b0-41fe-b1b1-998b602d5b4e.png)
![](https://user-images.githubusercontent.com/114450184/204182251-25cb3fba-bc0d-40ab-b218-641f30e7b3d1.png)

## Script trace for list-methods-compile-error
* Line 2-4: No stdout or stderr. Return code 0.
* Line 5: No stdout. Default stderr describing cloning process. Return code 0.
* Line 6: No stdout or stderr. Return code 0
* Line 7: No stdout orstderr. Return code non-zero
* Line 8-11: Skip due to false if conditional
* Line 12-15: No stderr or stdout. Return code 0.
* Line 16: No stdout. Return code non-zero. stderr:
```
ListExamples.java:15: error: ';' expected
        result.add(0, s)
                        ^
1 error
```
* Line 17: No stdout or stderr. Return code 0.
* Line 19: No stdout or stderr. Return code non-zero.
* Line 20-23: Skip due to false conditional
* Line 24: stdout: "ListExamples.java did not compile!" no stderr. Return code 0.
* Line 25: No stdout or stderr. Return code 0.
* Line 26-35: Skip due to script termination.