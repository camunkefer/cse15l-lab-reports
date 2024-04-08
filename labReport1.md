# `cd`
## no arguments
* ![Image](https://github.com/camunkefer/cse15l-lab-reports/blob/main/Screenshot%202024-04-07%20182058.png) <br>
* `/c/Users/camer/lecture1` <br>
* There is no output because it produces no output when it works. I am already in the directory `lecture1` but since there is no arguments it moved me to my home directory. <br>
* The output is not an error. <br>

## path to a directory
* ![Image](https://github.com/camunkefer/cse15l-lab-reports/blob/main/Screenshot%202024-04-07%20182105.png) <br>
* /c/Users/camer <br>
* There is no output because it produces no output when it works. I am in the home directory and then I go into `lecture1` which is a directory so it works. <br>
* The output is not an error. <br>

## path to a file
* ![Image](https://github.com/camunkefer/cse15l-lab-reports/blob/main/Screenshot%202024-04-07%20182121.png) <br>
* /c/Users/camer/lecture1 <br>
* My argument was `messages/en-us.txt` which is a file but `cd` is used to switch to another directory. Since that is a file and not a folder, it produced an error. <br>
* The output is an error because `messages/en-us.txt` is not a directory, it is a file. <br>

# `ls`
## no arguments
* ![Image](https://github.com/camunkefer/cse15l-lab-reports/blob/main/Screenshot%202024-04-07%20183702.png) <br>
* `/c/Users/camer/lecture1` <br>
* I got an output of a list of the file and folder names within `lecture1` because `ls` lists out the files and folders within the given path. With no given path, it will produce a list of the current directory i'm in which is `lecture1`. <br>
* The output is not an error. <br>
## path to a directory
* ![Image](https://github.com/camunkefer/cse15l-lab-reports/blob/main/Screenshot%202024-04-07%20184332.png) <br>
* `/c/Users/camer/lecture1` <br>
*  I got an output of a list of the file and folder names within `lecture1` because `ls` lists out the files and folders within the given path which is `lecture1`. <br>
* The output is not an error. <br>
## path to a file
* ![Image](https://github.com/camunkefer/cse15l-lab-reports/blob/main/Screenshot%202024-04-07%20185718.png) <br>
* `/c/Users/camer/lecture1` <br>
* It produced just `Hello.java` because it is a file and there are no files or folders within it. <br>
* The output is not an error. <br>
# `cat`
## no arguments
* ![Image](https://github.com/camunkefer/cse15l-lab-reports/blob/main/Screenshot%202024-04-07%20190220.png) <br>
* `/c/Users/camer/lecture1` <br>
* `cat` prints out the contents of a file but with no arguments, it waits for an input but since I left it blank, it didn't print anything. <br>
* The output is not an error. <br>
## path to a directory
*  ![Image](https://github.com/camunkefer/cse15l-lab-reports/blob/main/Screenshot%202024-04-07%20190747.png) <br>
* `/c/Users/camer/lecture1` <br>
* `cat` prints out the contents of a file and we gave it a path to a directory so it gave us an error that the path is to a directory. <br>
* The output is an error because the argument is not a file, it is a folder. <br>
## path to a file
* ![Image](https://github.com/camunkefer/cse15l-lab-reports/blob/main/Screenshot%202024-04-07%20190714.png) <br>
* `/c/Users/camer/lecture1` <br>
* The output is the contents of `Hello.java` because we gave it the path to `Hello.java` and since it is a file it printed out its contents. <br>
* The output is not an error. <br>
