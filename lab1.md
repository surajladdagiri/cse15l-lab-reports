## Lab Report 1 
***
 ## cd
1. Share an example of using the command with no arguments.
    *  ```
        [user@sahara ~/lecture1]$ cd
        [user@sahara ~]$ 
        ``` 
    * The working directory was ```/home/lecture1```
    * When you use the `cd` command with no arguments, it changes your working directory back to the home directory
    * The example shown is not an erroneous output. In the example, it changed directory to  ```/home```

2. Share an example of using the command with a path to a directory as an argument.
    *  ```
        [user@sahara ~]$ cd lecture1
        [user@sahara ~/lecture1]$
        ``` 
    * The working directory was ```/home```
    * When you use the `cd` command with a path to a directory, it changed your working directory to the directory you specified a path to
        * If you specify an absolute path, your working directory is irrelavant
        * If you specify a relative path, it can only change directory into directories within your working directory
    * The example shown is not an erroneous output. In the example, it changed directory to  ```/home/lecture1```

3. Share an example of using the command with a path to a file as an argument.
    *  ```
        [user@sahara ~/lecture1]$ cd Hello.java
        bash: cd: Hello.java: Not a directory
        ``` 
    * The working directory was ```/home/lecture1```
    * When you use the `cd` command with a path to a file, it is unable to do anything since you can only change your directory to a directory and not to a file
    * The error is simply saying that the specified path is to a file and not a directory since you can only change directory into a directory

***
 ## ls
 
1. Share an example of using the command with no arguments.
    *  ```
        [user@sahara ~/lecture1]$ ls
        Hello.java  messages  README 
        [user@sahara ~/lecture1]$
        ``` 
    * The working directory was ```/home/lecture1```
    * When you use the `ls` command with no arguments, it simply shows the contents of your working directory
    * The example shown is not an erroneous output. It showed the contents of ```/home/lecture1``` which were ```Hello.java```, ```README```, and a folder named ```messages```

2. Share an example of using the command with a path to a directory as an argument.
    *  ```
        [user@sahara ~/lecture1]$ ls messages
        en-us.txt  es-mx.txt  zh-cn.txt
        [user@sahara ~/lecture1]$
        ``` 
    * The working directory was ```/home/lecture1```
    * When you use the `ls` command with a path to a directory, it shows the content of the directory you specified a path to
        * If you specify an absolute path, your working directory is irrelavant
        * If you specify a relative path, it can only shows contents of directories within your working directory
    * The example shown is not an erroneous output, in this case it shows the 3 files in ```/home/lecture1/messages```

3. Share an example of using the command with a path to a file as an argument.
    *  ```
        [user@sahara ~/lecture1]$ ls /home/lecture1/Hello.java
        /home/lecture1/Hello.java
        [user@sahara ~/lecture1]$
        ``` 
    * The working directory was ```/home/lecture1```
    * When you use the `ls` command with a path to a file, it just shows the path to the file because are no files within a file. 
    * There is no error, in this example, it restates the path to `Hello.java`
    
***
 ## cat
 
1. Share an example of using the command with no arguments.
    *  ```
        [user@sahara ~/lecture1]$ cat
        ^C
        [user@sahara ~/lecture1]$
        ``` 
    * The working directory was ```/home/lecture1```
    * When you use the `cat` command with no arguments, it attempts to show the contents of no file and simply freezes which is why I had to use control+C to exit
    * The example shown is an error and it is caused by the fact that the terminal is trying to read a file but it doesn't have any file to look at

2. Share an example of using the command with a path to a directory as an argument.
    *  ```
        [user@sahara ~/lecture1]$ cat messages
        cat: messages: Is a directory
        [user@sahara ~/lecture1]$
        ``` 
    * The working directory was ```/home/lecture1```
    * When you use the `cat` command with a path to a directory, it is unable to do anything since it cannot show the contents of a directory and can only show the contents of a file hence leading to an error

3. Share an example of using the command with a path to a file as an argument.
    *  ```
        [user@sahara ~/lecture1]$ cat messages/en-us.txt
        Hello World!
        [user@sahara ~/lecture1]$ 
        ``` 
    * The working directory was ```/home/lecture1```
    * When you use the `cat` command with a path to a file, it just shows contents of the file like it was intended to
    * There is no error, in this example, it shows the contents of to `en-us.txt`
