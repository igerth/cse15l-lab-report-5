# Lab Report 5

In this lab report, I am going to be finishing / tweaking my grading script from Lab 6 and showing that it works on several files. 

![Image](https://github.com/igerth/cse15l-lab-report-5/blob/main/Screenshot%202023-03-13%20at%202.18.25%20PM.png?raw=true)

This is first what my grading script looks like now before I make any changes. It so far works, however, it only prints whether all the tests passed or if at least one failed, demarcated by `Pass` and `Fail`. Very primative in my opinion. 

![Image](https://github.com/igerth/cse15l-lab-report-5/blob/main/Screenshot%202023-03-13%20at%202.45.31%20PM.png?raw=true)

This is what I changed in my script to include which tests passed/failed. I used `grep -c "FAILURES!!!" out.txt` to search for the number of times `FAILURES!!!` appeared in the output of the `java` command (that is what the `-c` part does with `grep`). Then I used an `if` statement to see if it equalled 0. If this was the case, I printed `ALL TESTS PASSED`. If not, I used `grep "Tests run:" out.txt` to search and return the line in the output of the `java` command where it gave how many tests passed and how many tests failed. 

Here are screenshots of my grading script running on some files that were provided in the Week 6 lab. 

![Image](https://github.com/igerth/cse15l-lab-report-5/blob/main/Screenshot%202023-03-13%20at%202.55.04%20PM.png?raw=true)
First
![Image](https://github.com/igerth/cse15l-lab-report-5/blob/main/Screenshot%202023-03-13%20at%202.55.20%20PM.png?raw=true)
Second
![Image](https://github.com/igerth/cse15l-lab-report-5/blob/main/Screenshot%202023-03-13%20at%202.55.41%20PM.png?raw=true)
Third
![Image](https://github.com/igerth/cse15l-lab-report-5/blob/main/Screenshot%202023-03-13%20at%202.56.06%20PM.png?raw=true)
Fourth
