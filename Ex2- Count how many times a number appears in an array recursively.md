# Ex2 Count how many times a number appears in an array recursively.
## DATE: 19-08-2025
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1. Read the array size, then read all elements into the array arr.
2. Read the target value whose occurrences need to be counted.
3. Call the recursive function countOccurrences(arr, size, target).
4. In the recursive function, if n becomes 0, return 0; otherwise check if the last element equals the target and add 1 if it matches. 
5. Return the total count obtained by recursively processing the remaining elements and print the final count.  

## Program:
```JAVA
/*
Program Count how many times a number appears in an array recursively.
Developed by: Prajin S
RegisterNumber: 212223230151
*/
import java.util.Scanner;
public class CountOccurrences {

    // Recursive function to count occurrences of a target number
    public static int countOccurrences(int[] arr, int n, int target) {
        //write your code here
        if (n == 0) {
            return 0;
        }

        // Check the last element and add 1 if it matches the target
        if (arr[n - 1] == target) {
            return 1 + countOccurrences(arr, n - 1, target);
        } else {
            return countOccurrences(arr, n - 1, target);
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input: Size of array
        int size = scanner.nextInt();

        if (size <= 0) {
            System.out.println("Invalid array size. Must be positive.");
            return;
        }

        // Input: Array elements
        int[] arr = new int[size];
        for (int i = 0; i < size; i++) {
            arr[i] = scanner.nextInt();
        }

        // Input: Target number to count
        int target = scanner.nextInt();

        // Compute and display result
        int count = countOccurrences(arr, size, target);
        System.out.println("The number " + target + " appears " + count + " time(s) in the array.");

        scanner.close();
    }
}

```

## Output:
<img width="1226" height="728" alt="image" src="https://github.com/user-attachments/assets/9f24cd3f-95c5-448b-8e29-5891fcafec33" />



## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
