# Part 1
EdStem Post:


<img width="747" alt="Screenshot 2023-06-04 at 7 34 14 PM" src="https://github.com/rcabotaje/cse15l-lab-reports/assets/130100627/66b43514-5f2e-41d4-bbfb-23e24a1220e3">

**What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?**

* The type of computer I am using is a MacBook running on MacOS. Also I'm using VScode and the Terminal inside of VScode to run the bash
script that is also compiling and running the java program.

**Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.**

* What im getting is that "directory is not found" and I'm also getting an IllegalArgumentException which I think is also causing the java test
program to fail, which is not what I want. What I want is the test to Pass, not have an error get thrown out, and the directoy to get found
becuase I know it exists since I can see it in the files/directories in VScode.

**Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.**

* The error happens when I run the bash script of "bash grade.sh". I think I think the errors happens, and tests fail, after I find if the
"TestJavaFile.java" is in the the list-grading-area directory because, its output of "file found" is the last running command that I
expected to happen because I want that to happen. So line 30 and after is where everything starts failing.

My bash script:
<img width="960" alt="Screenshot 2023-06-04 at 8 38 07 PM" src="https://github.com/rcabotaje/cse15l-lab-reports/assets/130100627/5396bdd8-741d-4fda-943a-6d20dce37a79">

---

**1. Tutor Response:** 

I can see that the 'grading-area' directory exists, but your script commands are outputting that it's not an existing one. So I would recommend that you try and print the working directory to before where you get the error and see where your script leads you to, and from there try using the terminal commands try to go the directory you can cd into 'grading-area' directory.

**2.Trying out the the given info/bug description:**

<img width="664" alt="Screenshot 2023-06-04 at 8 53 49 PM" src="https://github.com/rcabotaje/cse15l-lab-reports/assets/130100627/7439475f-6e1f-4e6c-ba28-bc472b2efea6">

When I printed the working directory (on line 29) before where I thought the the lines that were causing the error(line 30), I saw that I was ending up in the "list-examples-grader" directory which is the directory I don't to end up in to run "ListTestExamples.java" Since I want to be in the one of the repository I cloned. Then after in line 30 I cd up into the previous directory before "List-Examples-Grader" directory and then I try to cd into "grading-area" directory which doesn't exist in that directory, which causes all the other errors as line 32 (of image above) does the same thing, and when I run the tests it fails because it runs the tests in the wrong directory.

**3. Info Setup:**

The directory structure needed is `/Users/rommelcabotaje/Documents/GitHub/list-examples-grader/grading-area` and the file needed to run is the "TestListExamples.java" file so you can compile it and run the Tests inside of it.

Contents before the change:
<img width="960" alt="Screenshot 2023-06-04 at 8 38 07 PM" src="https://github.com/rcabotaje/cse15l-lab-reports/assets/130100627/5396bdd8-741d-4fda-943a-6d20dce37a79">
Command trigger bug: `bash grade.sh`

Description to fix the bug: 
On line 30 remove the "../" before the "grading-area" this will set you into the right directory to compile and run the tests correctly.

<img width="745" alt="Screenshot 2023-06-04 at 10 01 49 PM" src="https://github.com/rcabotaje/cse15l-lab-reports/assets/130100627/ddcc9f6f-7d4d-4aec-afe2-22c0a859cc0a">

# Part 2

Something I learned from our lab expirence was how to use VIM to edit files. I learned about the various keyboard commands that let us 
edit files in VIM. For example the usage of 'i' which was the "insert command" which allowed us to insert characters inside of a file 
like editing code in java files which caused tests to fail. Another example would be when we learned how to quit VIM using the command ":q" and 
how to save and quit using the command :wq. We also learned how to scroll through files using the keyboard keys h,j,k, and l. I found it
useful to learn VIM because it showed us how to we could edit java files without the usage of editors like VScode.
