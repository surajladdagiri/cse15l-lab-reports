# Lab Report 4
___


Throughout this, I occasionally typed in the command `clear` whenever the terminal was cluttered. This command simply cleared the terminal window, but kept all the history. I will not be mentioning whenever I typed it since I tend to use it after almost every command so that the screenshots come out clean and easy to understand. I initially started off at the default terminal of my system:

![Picture of the starting terminal]()

___

The next step was logging into the `ieng6` server.

![Picture of me logged in]()

The command I typed to get to this point was `ssh sladdagiri@ieng6.ucsd.edu`. This command is relatively simple. The `ssh` command simply allows you to remotely connect to another computer or server through the internet. The remote server has the URL `ieng6.ucsd.edu`. the `sladdagiri@` part before that simply specifies that I want to login to the username called `sladdagiri` that is housed at the server located at `ieng6.ucsd.edu`. Overall, the command simply says that I want to remotely log in to the server `ieng6.ucsd.edu` under the username `sladdagiri`. Typically, I would need to input a password for the username, but I set up a trusted key on the server so that my laptop is recognized by the server and it doesn't prompt for a password whenever my laptop is logging in.

___

The next step is to clone the repository of interest

![Picture of the repo cloned]()

The command I typed was `git clone git@github.com:surajladdagiri/lab7.git`. I copied the `git@github.com:surajladdagiri/lab7.git` from the GitHub website under the Code option, followed by selecting the ssh option. I pasted it in the terminal by first typing in `git clone `(with a space at the end) and then pressed <command> and v to paste it then I pressed <enter>. This command just cloned all the contents of the repository and it set it up so that your local changes can be pushed to the online version of the repository on GitHub. I set up a private key on GitHub similar to how I set up a private key on the server. This made it so that when the server I am sshed into attempts to connect to github, it doesn't prompt for a password since it is a trusted client. This is analagous to how it was done between my laptop and the `ieng6` server.

___

The next step is to run the test program.

![screen after cd and ls]()

The first thing I did was `cd lab7` which changed my working directory to the newly cloned GitHub repository's directory. After this, I used `ls` to list the files and noted a folder called `lib` within it. I then used `ls lib` to list the files within the `lib` directory. 


![Test results]()

Since we need to run a JUnit test, I checked the names of the two `.jar` files in the `lib` that have all the dependencies and classes necessary for JUnit to function. Once I had this, I could craft the compile and run commands. The first command was `javac -cp lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar *.java`. The `javac` command is the command to compile java code. the `-cp` argument stands for "class path" which specifies where the compiler can find any classes necessary for compilation. I provided the relative paths for the two `.jar` files required for the code to compile split by a colon. I finally listed `*.java` as the file that needs to be compiled. The `*.java` specifies every file with the extension `.java` in the working directory. After I compiled the code, I ran the tests using the `java` command which was `java -cp lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore ListExamplesTests`. The tests then ran and the results are above.
