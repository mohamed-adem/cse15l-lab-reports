# Part 1: Bugs
  ## Failure Inducing Input
    ```java
@Test
public void testReversedFailure() {
    int[] input = {1, 2, 3, 4};
    int[] expected = {4, 3, 2, 1};
    int[] result = ArrayExamples.reversed(input);
    assertArrayEquals("The reversed array does not match the expected output", expected, result);
}
```
 

  ## Non-Failure Inducing Input
    abc

  ## Symptom
    abc

  ## The Bug
    ABC

# Part 2: Researching Commands
