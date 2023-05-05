Download Link: https://assignmentchef.com/product/solved-ece325-lab-2-debugging-with-eclipse-and-trees-objectives
<br>
<h2>Debugging Java Projects with Eclipse</h2>

In this lab we try to walk through debugging and its implementation in the Eclipse IDE. Debugging allows you to run a program interactively while watching the source code and the variables during the execution. By <em>breakpoints</em> in the source code, you specify where the execution of the program should stop. To stop the execution only if a field is read or modified, you can specify <em>watchpoints</em>. Eclipse allows you to start a Java program in debugging mode. It also has a special <em>Debug</em> perspective, which gives you a preconfigured set of views.

Setting Breakpoints

To set a breakpoint in your source code you can simply double click on the small left margin in of your source code editor, or right click on this part and select <em>Toggle Breakpoint</em>.

Starting the Debugger

To debug your application, select a Java file which can be executed, right-click on it and select <em>Debug As</em> =&gt; <em>Java Application</em>.

<strong>NOTE</strong>: If you have not defined any breakpoints, this will run your program as normal. To debug the program, you need to define breakpoints first.

Controlling the Program Execution

Eclipse provides toolbar buttons for controlling the execution of the program you are debugging. Typically, it is easier to use the corresponding shortcut keys to control this execution. You can use the F5, F6, F7 and F8 key to step through your coding. The meaning of these keys is explained in the following table.

<strong>Key     Description </strong>

F5        Executes the currently selected line and goes to the next line in your program. If the selected line is a method call the debugger steps into the associated code.

F6        Steps over the call, i.e. it executes a method without stepping into it in the debugger.

<strong>Key     Description </strong>

F7        Steps out to the caller of the currently executed method. This finishes the execution of the current method and returns to the caller of this method.

F8        Resume the execution of the program code until it reaches the next breakpoint or watchpoint.

Evaluating Variables in the Debugger

The <em>Variables</em> view displays fields and local variables from the current executing stack. Please note you need to run the debugger to see the variables in this view.

Breakpoints Properties

After setting a breakpoint you can check the properties of it by right-click =&gt; <em>Breakpoint Properties</em>. In the breakpoint properties you can define a condition that restricts the activation of this breakpoint.

<ul>

 <li>You can for example specify that a breakpoint should only become active after it has reached 3 or more times via the <em>Hit Count</em></li>

 <li>You can also create a conditional expression. The execution of the program only stops at the breakpoint if the condition becomes true. This mechanism can also be used for additional logging, as the code that specifies the condition is executed every time the program reaches that point.</li>

 <li>Different Types of Breakpoints</li>

</ul>

<ul>

 <li><em>Method breakpoint</em>: A method breakpoint is defined by double-clicking in the left margin of the editor next to the method header. You can configure it if you want to stop the program before entering or after leaving the method.</li>

 <li><em>A class load breakpoint</em>: It stops when the class is loaded. To set a class load breakpoint, right-click on a class in the <em>Outline</em> view and choose the <em>Toggle Class Load Breakpoint</em></li>

</ul>

<h1>2  Deliverable 1 — Arrays and Debugging</h1>

Consider the class in ResearchGroups.java. This class contains the name of nine research group members.

<em>Step 1: </em>

<table width="81">

 <tbody>

  <tr>

   <td width="81">searchMember</td>

  </tr>

 </tbody>

</table>

You need to write new method called  to search for a member and report the following

<ul>

 <li>His/her name’s existence in the list (yes or not)</li>

 <li>His/her group number (some members are in more than one group)</li>

 <li>Whether he/she is a group leader (the first person listed in each group is indicated as its leader)</li>

</ul>

<table width="159">

 <tbody>

  <tr>

   <td width="35">equal</td>

   <td width="89"> method from</td>

   <td width="35">Array</td>

  </tr>

 </tbody>

</table>

<strong>NOTE</strong>: You can use  class to check equality of names.

<em>Step 2: </em>

<table width="68">

 <tbody>

  <tr>

   <td width="68">sortGroups</td>

  </tr>

 </tbody>

</table>

In this step, you are required to write another method called  which is able to sort groups in terms of their length in ascending order. Luckily you just wrote heap sort in Lab 1, so work out how to reuse it. (Hint: consider hashing that maps objects into an integer) <strong>DEMO this deliverable to the lab instructor (10 points).</strong>

<em>Step 3: </em>

<table width="81">

 <tbody>

  <tr>

   <td width="81">searchMember</td>

  </tr>

 </tbody>

</table>

method. Debug your program and follow the execution of the

<em>Step 4: </em>

Follow the variable you have used in searching loop as a counter by setting a breakpoint. Fix a hit count to activate the breakpoint after a certain number of iterations.

<em>Step 5: </em>

Add a breakpoint for class loading. Debug your program again and verify that the debugger stops when your class is loaded.

<h1>3  Deliverable 2 — Red Black Tree</h1>

Let’s try something harder. It is where you really need to understand how to use debugging facilities. When things go wrong if you cannot use a debugger, you are DEAD.

<h2>Red Black Tree</h2>

The difficulties: – insertion as a binary search tree – tree balancing by rotation

Finish the methods in <em>RedBlackTree.java</em>. Red black tree is a more modern data structure than perhaps we are used to using. It becomes popular in the 1980’s and quickly replaces earlier ideas, such as simple binary trees in most applications. A description can be found at <a href="https://en.wikipedia.org/wiki/Red-black_tree">http://en.wikipedia.org/wiki/Red</a><a href="https://en.wikipedia.org/wiki/Red-black_tree">–</a><a href="https://en.wikipedia.org/wiki/Red-black_tree">black_tree</a><a href="https://en.wikipedia.org/wiki/Red-black_tree">.</a>

<table width="28">

 <tbody>

  <tr>

   <td width="28">null</td>

  </tr>

 </tbody>

</table>

<strong>Hint</strong>: Watch out for these NIL nodes — they are not ; they are black.

<strong>Note 1</strong>: Write carefully, you are going to reuse this code later!

<strong>Note 2</strong>: If you can’t remember what a binary search tree is — STOP. And go and revise.

<strong>NOTE 3</strong>: THIS IS A VERY DEMANDING ASSIGNMENT. It is expected that many students will not produce a perfect solution. Partial marks are available for reasonable attempts.