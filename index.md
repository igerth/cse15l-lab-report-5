# Lab Report 5

In this lab report, I am going to be finishing / tweaking my grading script from Lab 6 and showing that it works on several files. 

![Image](https://github.com/igerth/cse15l-lab-report-5/blob/main/Screenshot%202023-03-13%20at%202.18.25%20PM.png?raw=true)

This is first what my grading script looks like now before I make any changes. It so far works, however, it only prints whether all the tests passed or if at least one failed, demarcated by `Pass` and `Fail`. Very primative in my opinion. 

![Image](https://github.com/igerth/cse15l-lab-report-5/blob/main/Screenshot%202023-03-13%20at%202.45.31%20PM.png?raw=true)

This is what I changed in my script to include which tests passed/failed. I used `grep -c "FAILURES!!!" out.txt` to search for the number of times `FAILURES!!!` appeared in the output of the `java` command (that is what the `-c` part does with `grep`). Then I used an `if` statement to see if it equalled 0. If this was the case, I printed `ALL TESTS PASSED`. If not, I used `grep "Tests run:" out.txt` to search and return the line in the output of the `java` command where it gave how many tests passed and how many tests failed. 

Here are screenshots of my grading script running on some files that were provided in the Week 6 lab. 

![Image](https://github.com/igerth/cse15l-lab-report-5/blob/main/Screenshot%202023-03-13%20at%202.55.04%20PM.png?raw=true)

This first screenshot is of my script running from a repository with a bug in the code. Here you can see that one test was run and that it failed. A nice example of what a fail would look like. 

![Image](https://github.com/igerth/cse15l-lab-report-5/blob/main/Screenshot%202023-03-13%20at%202.55.20%20PM.png?raw=true)

This second screenshot is of my script running from a repository with no bugs. Here you are able to see what my script prints when the code runs flawlessly. 

![Image](https://github.com/igerth/cse15l-lab-report-5/blob/main/Screenshot%202023-03-13%20at%202.55.41%20PM.png?raw=true)

This third screenshot is the script running from a repository with a file that does not compile successfully. In my script I wrote an exit point for when the file does not compile succesfully. It echoes `Compiled Unsuccessfully` and terminates. 

![Image](https://github.com/igerth/cse15l-lab-report-5/blob/main/Screenshot%202023-03-13%20at%202.56.06%20PM.png?raw=true)

This last screenshot is of my script running from a repository that the file incorrectly named. My script checks for the specific file name `ListExamples.java`, however, the file in this repository is named `ListMethods`. My grading script recognizes that using an `if` statement, and if the file under the specific file name is not found, it echoes `File not found` and terminates. 

## Summary
Writing this grading script, although challenging, was by far one of my favorite parts of the labs this quarter. I got to learn all about bash scripts and also got to implement some of my knowledge about LINUX commands as well. Also, in the Week 8 lab, it was interesting to see other peoples' grading scripts and analyze how others attacked the problem. I loved hearing feedback and taking notes on how I can get better in coding. 
