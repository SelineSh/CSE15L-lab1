
Step 4: Log into ieng6
![Image](4-1.jpg)
Keys pressed: ```ssh cs15lfa23gw@ieng6.ucsd.edu <enter>``` 

This is login my ieng6 account.

Step 5: Clone your fork of the repository from your Github account (using the SSH URL)
![Image](4-2.jpg)
Keys pressed: ```git clone git@github.com:SelineSh/lab7.git <enter>```

This is clone my fork of the repository, and  ```git@github.com:SelineSh/lab7.git``` is the SSH URL from my Github account.

Step 6: Run the tests, demonstrating that they fail
![Image](4-3.jpg)
Keys pressed: ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter>``` , ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests <enter>``` 

This is run the tests.



Step 7: Edit the code file ListExamples.java to fix the failing test (as a reminder, the error in the code is just that index1 is used instead of index2 in the final loop in merge)
![Image](4-4.jpg)
Keys pressed: ```vim ListExamples.java <enter>``` 

This is open ListExamples.java

![Image](4-12.jpg)
Keys pressed: ```<up><up><up><up><up><up><up>``` + ```<left><left><left><left><left><left><left>``` 

This is move to 44,13, behind the ```index1```.

![Image](4-6.jpg)
Keys pressed:  ```i``` 

This is change to INSERT mode.

Keys pressed: ``` <backspace> 2``` 

This is to change ```index1``` to ```index2``` .

![Image](4-7.jpg)
```<esc> :(````<shift> + ;````)  w  q ``` 

This is save and exit. ```<esc>```is exit the INSERT mode, ```w```is save, ```q``` is exit.


Step 8: Run the tests, demonstrating that they now succeed
![Image](4-8.jpg)
Keys pressed: ```<up><up><up><enter>```, ```<up><up><up><enter>```

This is find and run ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java```, since it's third from the bottom in the history, I use the ```<up><up><up>``` to access it. And then since after run ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java```, ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests``` is third from the bottom in the history, I use the ```<up><up>``` to access it.

Step 9: Commit and push the resulting change to your Github account
![Image](4-9.jpg)
Keys pressed: ```git push <enter>``` 

This is push the resulting change to my Github account

![Image](4-11.jpg)
Keys pressed: ```git commit -m + "message" <enter>``` 

This is commit message for the resulting change to my Github account
