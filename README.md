Download Link: https://assignmentchef.com/product/solved-cmpt141-assignment8-testing-and-debugging
<br>
<strong>Question 1 </strong>

<strong>Purpose: </strong>To practice testing functions you wrote yourself.

<strong>Degree of Difficulty: </strong>Moderate

In digital advertising, data is extremely important to measure success of a campaign. In this assignment, we are going to calculate two commonly used digital advertising measurements, write test cases, and create a test driver for those test cases. The equations for the measurements are below:

<strong>eCPM </strong>(effective cost per mille)

<em>eCPM </em>= ( <em>Total Ad Spend / Total Ad Impressions </em>)∗1000

<strong>ARPDAU </strong>(average revenue per daily active user)

<em>ARPDAU </em>= ( <em>Revenue / Active Users / Days </em>)

Write the following functions:

<ul>

 <li>calculate_ecpm(ad_spend, ad_impresions) takes 2 <strong>integer </strong>parameters and returns a <strong>float </strong>representing calculated <strong>eCPM</strong>. Your function should return 0.0 for incorrect input.</li>

</ul>

<table>

 <tbody>

  <tr>

   <td> </td>

  </tr>

 </tbody>

</table>

For Example:

<table>

 <tbody>

  <tr>

   <td> </td>

  </tr>

 </tbody>

</table>

&gt; calculate_ecpm(152, 1013) &gt; 150.05

<ul>

 <li>calculate_arpdau(user_list, revenue_list) takes 2 <strong>list </strong>parameters and returns a <strong>float </strong>representing calculated <strong>ARPDAU</strong>. Both lists should be the same length and include numbers only. You will need to <strong>sum </strong>the values in each list. Your function should return 0.0 for incorrect input. For Example:</li>

</ul>

<table>

 <tbody>

  <tr>

   <td> </td>

  </tr>

 </tbody>

</table>

&gt; calculate_arpdau([54,36,30,96,112,130],[40.05,15.11,16.07,26.90,79.68,114.12]) &gt; 0.1062

<strong>Inside both functions</strong>, use the <strong>round() </strong>method to limit the number of decimal places shown in the results. <strong>calculate_ecpm </strong>should round to 2 decimal places while <strong>calculate_arpdau </strong>should round to 4 decimal

places. An example of using <strong>round()</strong>:

&gt; round(1.259483,2)

<table>

 <tbody>

  <tr>

   <td> </td>

  </tr>

 </tbody>

</table>

&gt; 1.25

To show that your functions are working correctly, implement a test driver which thoroughly tests both functions with a variety of white-box tests (at least six per function). You can use either plain if-statements (as demonstrated in readings 15.2.4) or a list-of-dictionaries to implement your test driver (as demonstrated in class during chapter 15 exercise 3).

<strong>Question 2 </strong>

<strong>Purpose: </strong>To practice testing and debugging code that someone else wrote.

<strong>Degree of Difficulty: </strong>Moderate

In the provided file a8q2_functions.py you’ll find two functions:

<ul>

 <li>isValidPhoneNumber(): Returns True if the provided phone number (represented as a string) is correctly formatted, otherwise False. To be considered correctly formatted, phone numbers must be written as ###-###-####, where # is a digit between 0 and 9.</li>

 <li>validatePhoneBook(): A phone book is a list where each entry is a phone book record (represented as a dictionary; see below for more details). This function checks each phone book record in the phone book for correctly formatted phone numbers.</li>

</ul>

A phone book record is a dictionary which initially has two keys: the key “name” mapped to the contact’s name (string) and the key “phone number” mapped to that contact’s phone number (also a string). validatePhoneBook() adds a new key “valid” to the record with the value True if the phone number is formatted correctly, otherwise False.

<table width="652">

 <tbody>

  <tr>

   <td width="652"># before[ { “name” : “Department of Computer Science”,“phone number” : “306-966-4886” },{ “name” : “Department of History”,“phone number” : “306.966.8712” } ]# after[ { “name” : “Department of Computer Science”,“phone number” : “306-966-4886”,“valid” : True },{ “name” : “Department of History”,“phone number” : “306.966.8712”,“valid” : False } ]</td>

  </tr>

 </tbody>

</table>

Here is how a sample phone book might look before and after validatePhoneBook():

The provided functions contain errors. Your task will be to find the errors by systematically testing. You’ll  hand in an explanation of what the errors are, and how you fixed them, but you will not hand in the corrected code.

Part of the exercise is figuring out what the code is supposed to do based on the documentation!

<ol>

 <li>Write white-box and black-box tests for the function isValidPhoneNumber(). You should do this without Python, either on paper, or in a simple document. Don’t worry about running your tests until you have thought about which test cases you want. Make sure you have <strong>at least </strong>3 black-box tests and 3 white-box tests. More tests may be useful.</li>

 <li>Implement a test driver using your test cases in a document named a8q2_testing.py. This should be done using the techniques seen in the textbook (Chapter 15) and as demonstrated in class (Chapter 15 Exercise 3).</li>

 <li>Run your tests and copy/paste the console output to a document named a8q2_output.txt. The console output you hand in should come from the program before you try to fix it!</li>

 <li>Try to deduce the problems with the isValidPhoneNumber() function from the output of your testing. Then fix the error(s) in the function!</li>

 <li>In the document a8q2_output.txt, describe the error(s) you found and how you fixed it (them). You do not need to write a lot; a sentence or two for each error is all we want. Write your explanation as if you are explaining the error to a colleague of yours who wrote the functions.</li>

 <li>Repeat the above steps for the second function validatePhoneBook().</li>

</ol>

<strong>Note: </strong>When writing your test driver for validatePhoneBook(), you can assume existing keys and values in a phone book will be unchanged. In other words, it is sufficient to only check whether the key ”valid” exists and is paired with the correct value in each phone book record after validatePhoneBook() is called.




Be sure to include your name, NSID, student number, course number, lecture section and laboratory section at the top of all documents submitted.