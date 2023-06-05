# Lab Report 5

## Debugging Scenario

Student Post:

![Image](0605_0936_45.png)

![Image](firefox_0605_0937_01.png)

Their initial test and output:

![Image](Code_0604_1703_09.png)

TA Response:

Are you sure your merge condition is working properly? What have you tried to debug your issue so far? It seems your method is causing the exception because of an incorrect loop condition. The while loops' conditions in your merge method should be less than the size of the ArrayList, you may have your loop contidion set to be less than or equal to the ArrayList size instead of less than. Try the suggested change and see if it fixes the bug.

Student Response to Changes:

The student's implementation of the merge method in ListExamples was incorrectly done. In their implementation of `ListExamples.java`. They had the following condition on the first while loop in the method on line 27:

`while(index1 <= list1.size() && index2 <= list2.size()) {`

The student saw the suggested change by the TA and changed the line removing the `=` sign so the while loop runs as `index1 < list1.size()` and `index2 < list2.size()`. The changed line 27 appears as this:

`while(index1 < list1.size() && index2 < list2.size()) {`

After the change, the ListExamples test passes appearing as this now:

![Image](Code_0605_0956_00.png)

The bug was that the while loop in merge() in `ListExamples.java` was incorrectly implemented. The condition makes the loop call for an index that does not exist in list1 and list2 causing the `ArrayIndexOutOfBoundException`.

## Reflection


