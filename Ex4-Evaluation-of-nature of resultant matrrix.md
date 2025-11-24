# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE: 19-08-2025
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1. Read m and n, then create three m×n matrices arr1, arr2, and arr3.
2. Read all elements of arr1 from input.
3. Read all elements of arr2 from input.
4. Add corresponding elements of arr1 and arr2 and store the result in arr3.
5. Print all elements of arr3 in matrix form.  

## Program:
```JAVA
/*
Program to ind the nature of resultant matrrix.
Developed by: Prajin S
RegisterNumber: 212223230151
*/
import java.util.Scanner;
public class matrix{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int m=sc.nextInt();
        int n=sc.nextInt();
        int[][] arr1=new int[m][n];
        int[][] arr2=new int[m][n];
        int[][] arr3=new int[m][n];
        for(int i=0;i<m;i++){
            for(int j=0;j<n;j++){
                arr1[i][j]=sc.nextInt();
            }
        }
        for(int i=0;i<m;i++){
            for(int j=0;j<n;j++){
                arr2[i][j]=sc.nextInt();
            }
        }
        for(int i=0;i<m;i++){
            for(int j=0;j<n;j++){
                arr3[i][j]=arr1[i][j]+arr2[i][j];
            }
        }
        for(int i=0;i<m;i++){
            for(int j=0;j<n;j++){
                System.out.print(arr3[i][j]+" ");
            }
            System.out.println();
        }
    }
}
```

## Output:
<img width="1125" height="668" alt="image" src="https://github.com/user-attachments/assets/7e9bf911-37d3-4dc8-8e57-b0e4e1d8802d" />



## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.
