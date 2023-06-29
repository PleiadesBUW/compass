## Getting Started: Linux Interface
### Linux

The computers in the compass lab all use Linux, Linux is an open source operating system (OS). The user interface is often different compared to the Windows and Mac OS interfaces many of you might be used to. 

There are many reasons why Linux os prefered in academic and work settings:

* There are many Linux distributions (or flavors)  available in the market such as Ubuntu, Fedora etc. Many of them have been developed for specific purposes and have their own unique advantage and use cases.

* As you will see, Linux contains low-level tools like sed, grep, awk piping etc. Programmers working on complex applications often prefer it for Linux's versatility, power, security, and speed

* Linux is quite light weight. As an emphasis is on performance you will notice that most programs will run faster on Linux compared to other OSs as the memory footprint and disk space are lower.

## How to use the Command line

#### 1. What is a Command line

A command line, also known as a terminal or shell, is a text-based interface in which users can interact with their computer's operating system by typing commands. It allows you to execute various tasks, perform system operations, and run programs without the need for a graphical user interface (GUI).


#### 2. Accessing the Terminal

Open the terminal clicking on the applications icon in the lower left corner, search for "Terminal" in the applications menu and click on it.

#### 3. Navigating the File System
The command line operates within the file system hierarchy. You can navigate through directories (folders) using commands such as:
* **cd** (change directory): Moves to a different directory.
* **ls** (list): Displays the contents of the current directory.
* **pwd** (print working directory): Shows the current directory's path.
 
Some example can be seen in the next section.

#### 4. Executing Commands
Users can run programs, execute tasks, and interact with the system by typing commands into the command line. Commands typically follow the format:

```bash
$ command_name [options] [arguments]

```
**Examples**

**cd (change directory) examples**:

* **cd** or **cd ~**: Takes you to your home directory.
* **cd /**: Changes to the root directory.
* **cd /path/to/directory**: Moves to a specific directory by providing its absolute path.
* **cd ..**: Goes up one level in the directory hierarchy.
* **cd ../../**: Moves up two levels in the directory hierarchy.
* **cd Documents**: Changes to a directory named "**Documents**" within the current directory.

**ls (list) examples**:

* **ls**: Lists the files and directories in the current directory.
* **ls -l**: Displays the files and directories in a long format, including additional details like permissions, owner, size, and modification time.
* **ls -a**: Shows all files, including hidden files and directories (ones that start with a dot).

#### 5. Getting Help: 

Users can access documentation and learn about command options and usage by referring to the manual pages. The command "**man**" followed by the command name displays its manual. For instance, "**man ls**" shows the manual for the "**ls**" command.


#### 6. Running Programs: 
Users can execute programs directly from the command line and open softwares as well. For example:

* typing "**python**" in the command line and pressing **enter** launches the Python interpreter.
* typing "**python filename.py**" in the command line and pressing **enter** can run/execute the Python file "**filename.py**".
* typing "**matlab**" in the command line and pressing **enter** starts the MATLAB environment.



Further commands for the Linux command line and useful information can be found [here](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview)






