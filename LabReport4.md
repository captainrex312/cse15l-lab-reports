# LabReport 4

## Step 1 : Log into ssh ieng6

[Image](Login)

## Steo 2 : Clone your fork of the repository from your Github account


[Image](Fork)

## Step 3 : Run tests to show they fail

[Image](Testfail)

## Step 4: Edit the code to fix the failing test

Open the file in order to edit the code by using the command :
~~~
vim ListExamples.java
~~~
Type in :
~~~
?index1
~~~
to search for index 1 from the bottom up. This will immediately go to the correct one that we need to alter.\
Next, type :
~~~
wq
~~~
and press the left arrow twice, <left><left> in order to get to the "1"\
Press "x" to remove the "1", followed by pressing "i" to enter insert mode. Type "2" in order to add it correctly.\
Press escape to exit insert mode.\
Type :
~~~
:wq
~~~
[Image](Openfail)

## Step 5 : Run tests to show they pass
  
[Image](Testpass)

## Step 6 : Commit and push to github
  
[Image](Gitpush)
