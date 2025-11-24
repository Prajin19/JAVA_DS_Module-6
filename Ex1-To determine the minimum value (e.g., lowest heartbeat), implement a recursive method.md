# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE: 19-08-2025
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1. Read n and store the n input elements into the array.
2. Call getMin(arr, 0, n) to compute the minimum.
3. In getMin, if only one element remains (n == 1), return that element.
4. Otherwise recursively find the minimum of the rest of the array by calling getMin(arr, i+1, n-1).
5. Compare arr[i] with the minimum from recursion and return the smaller value.  

## Program:
```JAVA
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: Prajin S
RegisterNumber: 212223230151
*/
import java.util.*;

public class Main {
    static int getMin(int[] arr, int i, int n)
    {
        if (n==1){
            return arr[i];
        }
        
       int minRest = getMin(arr,i+1,n-1);
       return Math.min(arr[i],minRest);
        
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i=0; i<n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}

```

## Output:
<img width="799" height="358" alt="image" src="https://github.com/user-attachments/assets/0fc7371a-8f15-406b-8727-ab1411fbfc40" />



## Result:
Thus the JAVA prograM ti find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully
