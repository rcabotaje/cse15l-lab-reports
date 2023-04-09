# How to Log Into a Course-Specific Account on "**ieng6**."

**Step 1. Download and open VScode**


To do this, go to [this link](https://code.visualstudio.com/), download VScode for whichever operating system you're using, and follow their directions for installation (for this example we'll be using macOS). Once installed it open it and it should look like this:

![Image](vscode.png)


**Step 2. Open Terminal within VScode**

In VScode bring your cursor all the way up so that the drop down menus show. Click "Terminal" then "New Terminal",  and your VScode should look like this witht the Terminal at the bottom of the screen:

![Image](terminal.png)

**Step 3. Get your course-specific username and set your password for it.**

To get your username log into [here](https://sdacs.ucsd.edu/~icc/index.php) with your regular tritonlink username and PID. It should look like this:

![Image](sdcas.png)

Under "Additional Accounts" you'll see your course-specific username(s). Click the course you're looking for (in this case cse15l).
![Image](1.png)

Once clicked you'll see your username and "Global Password Change" Tool. Click it.
![Image](2.png)

Then click "Proceed to the Password Change Tool"
![Image](3.png)

Enter your course-specific username (in this case the cse15l*****):
![Image](4.png)


Click I want to change my course-specific password:
![Image](5.png)

Change your password:
![Image](6.png)

**Step 5: Log Into Your "ieng6" Account**

Go to back to VScode with the terminal open. Type inside the terminal `ssh course-specific-usename@ieng.ucsd.edu` and it'll prompt you to enter the your password you just set.

