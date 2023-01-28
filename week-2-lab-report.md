# Week 2 Lab Report

Part 1
---
In this part, I will write a web server called `StringServer` that displays a chain of String messages based on query arguments. 

**Code for StringServer:**
![StringServer](https://user-images.githubusercontent.com/122575873/215290348-4e4f313e-6cf1-4c84-acc5-a661bf6dfd19.png)
*This code was based on the NumberServer.java file in the Lab Tasks under Week 2. Server.java was also used as a "black box" file to allow the server to run.*

**Screenshot #1:**
![Screenshot1](https://user-images.githubusercontent.com/122575873/215290427-51261244-f45b-4dfe-b3a0-08defa29fdb9.png)

1. Methods called: `public String handleRequest(URI url)`,`public static void main(String[] args) throws IOException`, methods in Server.java
2. Relevant arguments/fields: The url is a relevant parameter to `handleRequest` because it will be split according to the presence of `/add-message` in the path and the argument in the query. The port number is also relevant since it will differentiate my server from others with the same name. 
3. Values changed: I made a String variable called `total` to include all the messages that were added to the webpage. When `handleRequest` is called, the current String message is added to that total. I didn't change the port number at any time, but I did change the query arguments in the URL every time I wanted to add a message. 

**Screenshot #2:**
![Screenshot2](https://user-images.githubusercontent.com/122575873/215290452-8337b5fa-48a1-4081-b448-b91396ec41f7.png)

1. Methods called: `public String handleRequest(URI url)`,`public static void main(String[] args) throws IOException`, methods in Server.java
2. Relevant arguments/fields:  Again, the url is a relevant parameter to `handleRequest` because it will be split according to the presence of `/add-message` in the path and the argument in the query. The port number is also relevant since it will differentiate my server from others with the same name. 
3. Values changed: Again, I made a String variable called `total` to include all the messages that were added to the webpage. When `handleRequest` is called, the current String message is added to that total. I didn't change the port number at any time, but I did change the query arguments in the URL every time I wanted to add a message. 

Part 2
---
In this part, I will outline the process of identifying and fixing a bug from Lab 3.   
I chose a bug from the provided file `ArrayExamples.java` and the method `reversed`, which takes an int array as a parameter.   

`static int[] reversed(int[] arr) {`
  `int[] newArray = new int[arr.length];`
    `for(int i = 0; i < arr.length; i += 1) {`
      `arr[i] = newArray[arr.length - i - 1];`
    `}`
    `return arr;`
 `}`

**First, let's include a failure-inducing input for the buggy program (using an associated JUnit test):**

`@Test`
  `public void testReversedFailedInput(){`
    `int[] failedInput = {3,2,1};`
    `assertArrayEquals(new int[]{1,2,3}, ArrayExamples.reversed(failedInput));`
  `}`
  
**Then, let's write a test for a non-failure-inducing input:**

`@Test`
  `public void testReversedPassingInput(){`
    `int[] passingInput = {0};`
    `assertArrayEquals(new int[]{0}, ArrayExamples.reversed(passingInput));`
  `}`
  
**Here is the symptom (output of running the tests in JUnit):**
testReversedFailedInput:
![Image](https://user-images.githubusercontent.com/122575873/215287394-1a026b87-02e5-4733-894c-df8be9cddbf4.png)

The error message reads: *arrays first differed at element [0]; expected:[1] but was:[0]...*

testReversedPassingInput:
![Image](https://user-images.githubusercontent.com/122575873/215287446-e6da757a-17d2-43f6-b799-fe3cd6896ddf.png)

As expected, the test passes even though the program is buggy.

**Finally, here is the bug itself (before and after it's fixed):**
Before:
`static int[] reversed(int[] arr) {`
  `int[] newArray = new int[arr.length];`
    `for(int i = 0; i < arr.length; i += 1) {`
      `arr[i] = newArray[arr.length - i - 1];`
    `}`
    `return arr;`
 `}`
 
 After:
 `static int[] reversed(int[] arr) {`
    `int[] newArray = new int[arr.length];`
    `for(int i = 0; i < arr.length; i += 1) {`
      `newArray[i] = arr[arr.length - i - 1];`
    `}`
    `return newArray;`
  `}`

Explanation: Since the method aims to return a *new array* with the elements of the input array reversed, we will change the return statement to newArray instead of arr.  
Additionally, we need to copy the input array to the new array (not the other way around), so within the for loop we should switch `arr[i] = newArray[arr.length - i - 1]` to `newArray[i] = arr[arr.length - i - 1]`.  
This successfully fixes the bug, and the JUnit tests all pass. 

![Image](https://user-images.githubusercontent.com/122575873/215287627-5bcab8c8-b82a-48c9-85f2-360a9546e8c9.png)

Part 3
---
During lab on weeks 2 and 3, I learned how to better write JUnit tests to cover all important cases for a given program.  
I agree with Week 3's article on correctness standards in that I often settle for "good enough" when testing my code (a combination of laziness and a need to move on to work from other classes).  
However, completing the activities for Lab 3 helped me test my code more thoroughly and make debugging a less painful process.  
And I'm finding that the more I write these tests, the quicker I can complete them!  
