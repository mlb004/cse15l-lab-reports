# Week 2 Lab Report

Part 1
---

Part 2
---
In this part, I will outline the process of identifying and fixing a bug from Lab 3.
I chose a bug from the provided file ArrayExamples.java and the method `reversed`, which takes an int array as a parameter. 

`static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
 }`

**First, let's include a failure-inducing input for the buggy program (using an associated JUnit test):**

`@Test
  public void testReversedFailedInput(){
    int[] failedInput = {3,2,1};
    assertArrayEquals(new int[]{1,2,3}, ArrayExamples.reversed(failedInput));
  }`
  
**Then, let's write a test for a non-failure-inducing input:**

`@Test
  public void testReversedPassingInput(){
    int[] passingInput = {0};
    assertArrayEquals(new int[]{0}, ArrayExamples.reversed(passingInput));
  }`
  
**Here is the symptom (output of running the tests in JUnit):**
testReversedFailedInput:
![Image](https://user-images.githubusercontent.com/122575873/215287394-1a026b87-02e5-4733-894c-df8be9cddbf4.png)
The error message reads: *arrays first differed at element [0]; expected:[1] but was:[0]...*

testReversedPassingInput:
![Image](https://user-images.githubusercontent.com/122575873/215287446-e6da757a-17d2-43f6-b799-fe3cd6896ddf.png)
As expected, the test passes even though the program is buggy.

**Finally, here is the bug itself (before and after it's fixed):**
Before:
`static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
 }`
 
 After:
 `static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }`

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
