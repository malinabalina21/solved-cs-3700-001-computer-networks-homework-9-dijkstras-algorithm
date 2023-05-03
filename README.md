Download Link: https://assignmentchef.com/product/solved-cs-3700-001-computer-networks-homework-9-dijkstras-algorithm
<br>
<strong>An option of peer programming</strong>: You may choose to work on this assignment individually or in a team of two students.  If you choose to work in a <strong><em>team of two students</em></strong>, you <strong>must</strong> 1) <strong>add</strong> both team members’ first and last names as the <strong>comments</strong> on Blackboard when submitting the .java files (both team members are required to submit the same .java files on Blackboard), and 2) put a <strong><em>team.txt</em></strong> file including both team members’ names under your HW9/ on cs3700a (both team members are required to complete Task II under both home directories on cs3700a).  For grading, I will randomly pick the submission in one of the two <em>home directories</em> of the team members on <strong>cs3700a</strong> and <strong>cs3700b</strong>, and then give both team members the same grade.  If the team information is <em>missing</em> on Blackboard or cs3700a, two or more submissions with similar source codes with just variable name/comment changes will be considered to be a violation of the Integrity described in the course policies and both or all will be graded as 0.

<strong>Grading: </strong>Your programs will be graded via testing and points are associated with how much task it can complete.  <u>A program that</u> <u>cannot be compiled or crashes while running will receive up to 5% of the total points.</u>  <u>A submission of .java files that are similar to any</u> <u>online Java program with only variable name changes will receive 0% of the total points.</u>

<strong>Programming in Java is highly recommended and NO library function(s) related to the algorithm/protocol may be used</strong>, since all requirements in this assignment are guaranteed to be supported in Java.  If you choose to use any other language such as Python or C/C++, it is YOUR responsibility, before the cutoff deadline, to (2) set up the compiling and running environment on cs3700a, (2) make sure that I can run/test your programs in your home directory on cs3700a, and (3) provide a README file under HW9/ on cs3700a to include the commands that I need to use.




<strong>Part I (90%)</strong>: Write a <strong>Java program</strong> to build up the forwarding table at <strong>source router V0</strong> using the Dijkstra’s algorithm.

<ul>

 <li>The routers in the network are labeled as <strong>V0</strong>, <strong>V1</strong>, <strong>V2</strong>, …, etc (for display, such labels are <strong>required</strong> to use, please do NOT use 0, 1,</li>

</ul>

2, 3, … etc. However, it is perfectly okay for you to use indices 0, 1, …, and <em>n</em> – 1 internally in your program.)

<ul>

 <li>Your routing program needs to

  <ol>

   <li>Display a prompt message to ask the user to input the total number of routers, <strong><em>n</em></strong>, in the network. Validate <strong><em>n</em></strong> to make sure that it is greater than or equal to 2.</li>

   <li>Use a topo.txt file that contains costs of all links. Each line in this file provides the cost between a pair of routers as below, where <strong>tab (‘t’)</strong> is used to separate the numbers in each line.</li>

  </ol></li>

</ul>

&lt;# of one router&gt; &lt;# of the other router&gt; &lt;link cost between these two routers&gt;

…                 …                       …            where the first and the second numbers in each row need to be validated to be between 0 and <strong><em>n</em> – <em>1</em></strong>, the third number needs to be validated to be positive.  For example, for the link (V0, V3) whose cost is 10, <strong>only</strong> <strong>ONE of the following two lines needs to be included in the topo.txt file</strong>.

0              3              10           // only <strong>ONE</strong> of this or the next line needs to be included in the topo.txt file

3              0              10           // only <strong>ONE</strong> of this or the above line needs to be included in the topo.txt file

This topo.txt file can locate in the same directory where this program runs such that a path is not needed. Display a message saying that in which row the first invalid number is detected, close the txt file, and KEEP asking for the name of the cost input file until all numbers are checked to be valid.  Record the cost information in the Cost matrix.

<ol start="3">

 <li>Implement the Dijsktra’s algorithm to build up the shortest-path tree rooted at source router V0. As the intermediate results, at the end of <strong>Initialization</strong> and each iteration of the <strong>Loop</strong>, display The set <strong>N’</strong></li>

</ol>

The set <strong>Y’ </strong>

The distance vector <strong>D</strong>, i.e., D(i) for each i between 1 and <strong><em>n –</em> 1</strong>

The predecessor vector <strong>P</strong>, i.e., p(i) for each i between 1 and <strong><em>n – </em>1</strong>

<ol start="4">

 <li>Use the shortest-path tree resulted from the Dijsktra’s algorithm to build up the forwarding table for router V0. Display the forwarding table in the following format:</li>

</ol>

Destination                           Link

V1                                          (V0, …)

V2                                          (V0, …)

…

Vn-1                                      (V0, …)

<strong> </strong>

<strong>Part II (10%): Test your programs on the Virtual Server cs3700a.msudenver.edu </strong>

<strong> </strong>

<strong>                                                                                                                                                                (more on next page!) </strong>

MSU Denver, M&amp;CS                                               CS 3700-001: Computer Networks, Spring 2020                                                  Dr. Weiying Zhu

<strong>Warning</strong>: to complete this part, especially when you work at home, you must first (1) <strong>connect to GlobalProtect </strong>using your NetID account (please read “<strong>how to connect to GlobalProtect …</strong>” at <a href="https://msudenver.edu/vpn/">https://msudenver.edu/vpn/</a><a href="https://msudenver.edu/vpn/">)</a>; then (2) <strong>connect to the virtual servers cs3700a </strong>using <strong><em>sftp</em></strong> and <strong><em>ssh</em></strong> command on MAC/Linux or <strong><em>PUTTY</em></strong> and <strong><em>PSFTP</em></strong> on Windows.




<table width="720">

 <tbody>

  <tr>

   <td colspan="2" width="720">ITS only supports GlobalProtect on MAC and Windows machines.  If your home computer has a different OS, it is your responsibility to figure out how to connect to cs3700a for programming assignments and submit your work by the cutoff deadline.  Such issues cannot</td>

  </tr>

  <tr>

   <td width="246">be used as an excuse to request any extension.</td>

   <td width="474"><strong> </strong></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<ol>

 <li>MAKE a directory “<strong>HW9</strong>” under your home directory on <strong>cs3700a</strong>.msdenver.edu</li>

 <li>UPLOAD and COMPILE <strong><em>your program</em></strong> under “<strong>HW9</strong>” on <strong>cs3700a</strong>.msdenver.edu</li>

 <li>TEST <strong><em>your program</em></strong> running on <strong>cs3700a</strong>.msudenver.edu</li>

 <li>SAVE a file named <strong><em>txt</em></strong> under “<strong>HW9</strong>” on <strong>cs3700a</strong>.msudenver.edu, which captures the outputs of your program when you test it. You can use the following command to redirect the standard output (stdout) and the standard error (stderr) to a <strong>file</strong> on UNIX, Linux, or Mac, and view the contents of the file</li>

</ol>

<strong>java prog_name_args | tee testResultsClient.txt //copy stdout to the .txt file  //if you want, you may also use “script” command instead of the “tee” command </strong>

<strong>     //to write both stdin and stdout into testResultsClient.txt while testing your </strong>

<strong>      //client program on cs3700a.  For how to use “script”, see  </strong>

<strong> //</strong> <a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>https://www.geeksforgeeks.org/script</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>–</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>command</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>–</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>in</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>–</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>linux</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>–</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>with</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>–</strong></a><a href="https://www.geeksforgeeks.org/script-command-in-linux-with-examples/"><strong>examples/</strong></a> <strong> //or Google “script command in Linux” if the above link is broken. </strong>

<strong>cat file-name     //display the file’s contents.  </strong>

<strong> </strong>

<strong> </strong>