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
```java
@Test
public void testReversedNoFailure() {
    int[] input = {};
    int[] expected = {};
    int[] result = ArrayExamples.reversed(input);
    assertArrayEquals("The reversed array of an empty input should also be empty", expected, result);
}
```


  ## Symptom
    abc

  ## The Bug
    
### Before the Code Change:


```java
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
        arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
}
```



  ### After the Code Change:


```java
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i++) {
        newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
}
```



# Part 2: Researching Commands
