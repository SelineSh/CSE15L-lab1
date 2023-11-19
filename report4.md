
Step 4: Log into ieng6
![Image](4-1.jpg)
Enter the ```ssh``` + account + <enter> to login.

Step 5: Clone your fork of the repository from your Github account (using the SSH URL)
![Image](4-2.jpg)
Enter git clone + link  ```SSH URL``` + <enter> to clone

Step 6: Run the tests, demonstrating that they fail
![Image](4-3.jpg)
Enter ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` + <enter> and then ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests``` + <enter> to run the tests.



Step 7: Edit the code file ListExamples.java to fix the failing test (as a reminder, the error in the code is just that index1 is used instead of index2 in the final loop in merge)
![Image](4-4.jpg)
Enter ```vim ListExamples.java```+<enter> to open ListExamples.java

![Image](4-12.jpg)
<up><up><up><up><up><up><up>+<left><left><left><left><left><left><left> move to 44,13

![Image](4-6.jpg)
check ```i``` + <backspace> + ```2``` to change ```index1``` to ```index2``` 

![Image](4-7.jpg)
<esc> + ```:``` (<shift> + <:>) + w + q to save and exit.


Step 8: Run the tests, demonstrating that they now succeed
![Image](4-8.jpg)
<up><up> to find ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` + <enter> and then  <up><up> to find ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests``` + <enter> to run the tests.

Step 9: Commit and push the resulting change to your Github account
![Image](4-9.jpg)
Enter ```git push``` +<enter> to push
![Image](4-11.jpg)
Enter ```git commit -m + "message"```+<enter> to comiit message
