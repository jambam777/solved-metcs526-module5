Download Link: https://assignmentchef.com/product/solved-metcs526-module5
<br>
<strong>Problem 1</strong>. Consider the following binary search tree:

Show the resulting tree if you add the entry with key = 13 to the above tree. You need to describe, step by step, how the resulting tree is generated.

<strong>Problem 2 </strong> Consider the following binary search tree:

Show the resulting tree if you delete the entry with key = 42 from the above tree. You need to describe, step by step, how the resulting tree is generated.

<strong>Problem 3 .</strong> Consider the following AVL tree, which is unbalanced:

Note that the nodes <em>F</em>, <em>B</em> and <em>D</em> are labeled <em>z</em>, <em>y</em>, and <em>x</em>, respectively, following the notational convention used in the textbook. Apply a trinode restructuring on the tree and show the resulting, balanced tree.

<strong>Problem 4</strong>. Consider the following AVL tree.

Show the resulting, balanced tree after inserting an entry with key = 54 to the above tree. You must describe, step by step, how the resulting tree is obtained.

<strong>Problem 5 . </strong>Consider the following Huffman tree:

<ul>

 <li>Encode the string “BDEGC” to a bit pattern using the Huffman tree.</li>

 <li>Decode the bit pattern “010111010011” to the original string using the Huffman tree.</li>

</ul>

<strong>Problem 6. </strong>This question is about the <em>World Series</em> problem that we discussed in the class. The following is the probability matrix for the problem.




<em>P</em>(<em>i</em>, <em>j</em>)

<table width="344">

 <tbody>

  <tr>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

  </tr>

  <tr>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

  </tr>

  <tr>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49">*</td>

   <td width="49"> </td>

   <td width="49"> </td>

  </tr>

  <tr>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

  </tr>

  <tr>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

  </tr>

  <tr>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49">*</td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

  </tr>

  <tr>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

   <td width="49"> </td>

  </tr>

 </tbody>

</table>

6

5

4

3

2

1          <em>j</em>

0

6          5          4          3          2          1          0

<em>i                                     </em>

Calculate the probabilities of <em>P</em>(4, 1) and <em>P</em>(2, 4), which are marked with *.

<strong>Problem 7 . </strong>The goal of this problem is to give students an opportunity to compare and observe how running times of sorting algorithms grow as the input size (which is the number of elements to be sorted) grows. Since it is not possible to measure an accurate running time of an algorithm, you will use an <em>elapsed time</em> as an approximation. How to calculate the elapsed time of an algorithm is described below.

You will use four sorting algorithms for this experiment: insertion-sort, merge-sort, quick-sort and heap-sort. A code of insertion-sort is in page 111 of our textbook. An array-based implementation of merge-sort is shown in pages 537 and 538 of our textbook. An array-based implementation of quick-sort is in page 553 of our textbook. You can use these codes, with some modification if needed, for this assignment. For heap-sort, our textbook does not have a code. You can implement it yourself or you may use any implementation you can find on the internet or any code written by someone else. If you use any material (pseudocode or implementation) that is not written by yourself, you must clearly show the source of the material in your report.

A high-level pseudocode is given below:

for <em>n</em> = 10,000, 20,000, . . ., 100,000 (for ten different sizes)

Create an array of <em>n</em> random integers between 1 and 1,000,000 Run <strong>insertionsort</strong> and calculate the elapsed time // make sure you use the initial, unsorted array Run <strong>mergesort</strong> and calculate the elapsed time

// make sure you use the initial, unsorted array

Run <strong>quicksort</strong> and calculate the elapsed time

// make sure you use the initial, unsorted array  Run <strong>heapsort</strong> and calculate the elapsed time




You can generate <em>n</em> random integers between 1 and 1,000,000 in the following way:




Random r = new Random( );  for <em>i</em> = 0 to <em>n</em> – 1                                          a[i] = r.nextInt(1000000) + 1




You can also use the <em>Math.random</em>( ) method. Refer to a Java tutorial or reference manual on how to use this method.




Note that it is important that you use the initial, unsorted array for each sorting algorithm. So, you may want to keep the original array and use a copy when you run each sorting algorithm.




You can calculate the elapsed time of the execution of a sorting algorithm in the following way:




long startTime = System.currentTimeMillis(); call a sorting algorithm

long endTime = System.currentTimeMillis(); long elapsedTime = endTime ‐ startTime;




Write a program that implements the above requirements and name it <em>SortingComparison.java</em>.




Collect all elapsed times and show the result (1) as a table and (2) as a line graph.




A table should look like:




<table width="623">

 <tbody>

  <tr>

   <td width="80">        <em>n</em><em>Algorithm </em></td>

   <td width="54">10000</td>

   <td width="54">20000</td>

   <td width="54">30000</td>

   <td width="54">40000</td>

   <td width="54">50000</td>

   <td width="54">60000</td>

   <td width="54">70000</td>

   <td width="54">80000</td>

   <td width="54">90000</td>

   <td width="58">100000</td>

  </tr>

  <tr>

   <td width="80">insertion</td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="58"> </td>

  </tr>

  <tr>

   <td width="80">merge</td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="58"> </td>

  </tr>

  <tr>

   <td width="80">quick</td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="58"> </td>

  </tr>

  <tr>

   <td width="80">heapsort</td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="58"> </td>

  </tr>

 </tbody>

</table>




Entries in the table are elapsed times in milliseconds.




A line graph should show the same information but as a graph with four lines, one for each sorting algorithm. The <em>x</em>-axis of the graph is the input size <em>n</em> and the <em>y</em>-axis of the graph is the elapsed time in milliseconds. Your graph should look like the following example (Note: this is just an example and your graph will look different):










You don’t’ need to write a Java program to generate the graph. Once you have all elapsed times, you can plot the graph using any other tools, such as a typical spreadsheet software.




Note that, in your result, the running time of an algorithm may not increase as (theoretically) expected. It is possible that the running time of an algorithm may decrease a bit as the input size increases in a part of your graph. As long as the general trend of your graphs are acceptable, there will be no point deduction. So, you should not be too much concerned about that.




Name the program <em>Hw4_P6.java</em>.

<strong> </strong>

<strong>Deliverable</strong>




You need to submit the following files:

<ul>

 <li><em>pdf</em>: This file must include:</li>

 <li>Answers to problems 1 through 5.</li>

 <li>Discussion/observation of Problem 6: This part must include what you observed and learned from this experiment and it must be “substantive.”</li>

 <li><em>java</em></li>

 <li>Other files, if any.</li>

</ul>




Combine all files into a single archive file and name it <em>LastName_FirstName_hw5.EXT</em>, where <em>EXT</em> is an appropriate archive file extension, such as <em>zip</em> or <em>rar</em>.