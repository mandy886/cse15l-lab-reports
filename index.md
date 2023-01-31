# Part 1
The methods [method] and [method] are called.
The relevant arguments to those methods are [] and they have [x] values.
[] fields of the class cahnge from this specific requestion.

# Part 2
This input induces a failture for ```reverseInPlace(int arr[])```
```
int[] input2 = { 2, 4, 6 };
    assertArrayEquals(new int[]{ 6, 4, 2 }, input2);
```
This input induces a failure for ```reversed(int arr[])```
```
int[] input2 = { 5, 3, 1 };
    assertArrayEquals(new int[]{ 1, 3, 5 }, input2);
```
This input does not induce a failure when ```reversed(int arr[])``` is called because the loop does not run as 0 is not less than arrLength. Thus, the contents of the array remain the same which in this case is equal to its reverse order.
```
int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
```
Symptoms for the failure-inducing input for ```reverseInPlace(int arr[])```
![Image](https://user-images.githubusercontent.com/57383573/215667247-7b3182e4-34b3-4673-b4b3-638b1c77ff90.png)
![Image](https://user-images.githubusercontent.com/57383573/215673578-62cb1289-4a18-4d6c-8851-70b4ad797b6e.png)
Symptoms for the failure-inducing input for ```reversed(int arr[])```
![Image](https://user-images.githubusercontent.com/57383573/215667247-7b3182e4-34b3-4673-b4b3-638b1c77ff90.png)
![Image](https://user-images.githubusercontent.com/57383573/215667249-c13d025e-7dbc-43fd-a01c-af145f5ac9d1.png)
The bug is initializing length of the new array but not copying over the contents. When information is pulled from the new Array it is the null value 0.
```
int[] newArray = new int[arr.length]
```
Instead, you can copy the array and reverse by pulling numbers from the copied array.
```
static int[] reversedNew(int[] arr) {
  // Create a deep copy of arr
  int[] newArray = new int[arr.length];
  for (int i=0; i<newArr.length; i++) {
    newArray[i] = arr[i];
  }
  // Reverse array by accessing objects of deep copy
  for (int=1; i<arr.length; i+=1) {
    arr[i] = newArray[arr.length-i-1];
  }
  return arr;
}
```


# Part 3
A key takeaway for me from week 2 was that programs can take a URL and respond with text of a web page. To do this, I can write a ```URLHandler``` that does the processing and a class that takes the ```URLHandler``` and starts up the server that listens for incoming connections. 
