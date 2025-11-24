# EX3 Write a program to count the number of digits in an integer.
## DATE: 24-09-2025
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1. Read the integer n from input.
2. Initialize count to 0.
3. Repeat while n is greater than 0.
4. Divide n by 10 each time and increment count.
5. After the loop ends, print the value of count as the number of digits.

## Program:
```JAVA
/*
Program to to count the number of digits in an integer
Developed by: Prajin S
RegisterNumber: 212223230151
*/
import java.util.Scanner;

public class CountDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n=sc.nextInt();
        int count=0;
        while(n>0){
            n/=10;
            count++;
        }
        System.out.println("Number of digits: " + count);
    }
}

```

## Output:
<img width="741" height="359" alt="image" src="https://github.com/user-attachments/assets/d7a42b94-7bb1-4c33-b21b-7f69d5c20900" />



## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.
