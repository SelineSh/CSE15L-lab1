1. Share an example of using the command with no arguments.
![Image](1.jpg)
-The "cd" is used to change direction, but since I didn't command with argument, it will go 
back to the previous folder, and the direction in Q1 is /Home, so it won't change direction.
-The "ls" is used to show the names of the files and folders inside the current working 
directory, so it showed "lecture1".
-The "cat" is used to show the contents of one or more files given by the paths. Since 
I didn't make an argument; it doesn't show anything and lets me enter something. I use Ctrl+C to continue.

2. Share an example of using the command with a path to a directory as an argument.
  [user@sahara ~]$ cd lecture1
  [user@sahara ~/lecture1]$ ls messages
  en-us.txt  es-mx.txt  th.txt  zh-cn.txt
  [user@sahara ~/lecture1]$ cat messages
  cat: messages: Is a directory
-The "cd lecture1" changes the direction to /lecture1.
The "ls messages" because "messages" is a directory, so it showed the names inside the messages directory.
-The "cat messages" because "messages" isn't a file, it's a directory, so it showed "Is a directory".

3. Share an example of using the command with a path to a file as an argument.
  [user@sahara ~/lecture1]$ cd README
  bash: cd: README: Not a directory
  [user@sahara ~/lecture1]$ ls README
  README
  [user@sahara ~/lecture1]$ cat README
  To use this program:
  
  javac Hello.java
  java Hello messages/en-us.txt
-The "cd README" because README isn't a directory; it's a file, so it showed as "Not a directory".
-The "ls README" because README is a file, so it showed the "README".
-The "cat README" showed the contents of the README file.
