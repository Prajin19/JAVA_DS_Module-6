# Ex5 Count Inversions in an Array
## DATE: 19-08-2025
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1. Read n and store the n elements into the array arr.
2. Call mergeSortAndCount(arr, 0, n−1) to count inversions using a modified merge sort.
3. Recursively divide the array into two halves and count inversions in each half.
4. Merge the two sorted halves and count cross-inversions during the merge step.
5. Return and print the total inversion count obtained from left, right, and merge phases.

## Program:
```JAVA
/*
Program to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by: Prajin S
RegisterNumber: 212223230151
*/
import java.util.Scanner;

public class CountInversions {

    // Function to sort the array and return inversion count
    public static int mergeSortAndCount(int[] arr, int left, int right) {
        int count = 0;
        if (left < right) {
            int mid = (left + right) / 2;

            // Count inversions in left subarray
            count += mergeSortAndCount(arr, left, mid);

            // Count inversions in right subarray
            count += mergeSortAndCount(arr, mid + 1, right);

            // Count inversions while merging
            count += mergeAndCount(arr, left, mid, right);
        }
        return count;
    }

    // Merge two sorted subarrays and count inversions
    private static int mergeAndCount(int[] arr, int left, int mid, int right) {
        int[] leftArr = new int[mid - left + 1];
        int[] rightArr = new int[right - mid];

        for (int i = 0; i < leftArr.length; i++)
            leftArr[i] = arr[left + i];
        for (int i = 0; i < rightArr.length; i++)
            rightArr[i] = arr[mid + 1 + i];

        int i = 0, j = 0, k = left, swaps = 0;

        while (i < leftArr.length && j < rightArr.length) {
            if (leftArr[i] <= rightArr[j]) {
                arr[k++] = leftArr[i++];
            } else {
                arr[k++] = rightArr[j++];
                swaps += (leftArr.length - i); // Count inversions
            }
        }

        while (i < leftArr.length) arr[k++] = leftArr[i++];
        while (j < rightArr.length) arr[k++] = rightArr[j++];

        return swaps;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) arr[i] = sc.nextInt();

        int result = mergeSortAndCount(arr, 0, n - 1);
        System.out.println(result);
    }
}
```

## Output:
<img width="646" height="535" alt="image" src="https://github.com/user-attachments/assets/ecd8cfb9-7569-49fd-bf1a-ba2e3a980bd5" />



## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
