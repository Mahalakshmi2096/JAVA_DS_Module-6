# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE: 25.08.2025
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1. Start
2. Read number of rows and columns.
3. Create matrices A, B, and C of size rows × cols.
4. Input all elements of matrix A.
5. Input all elements of matrix B.
6. Set flags:

   ->allEven = true

   ->allOdd = true
7. For each position (i, j) in the matrices:

   ->Compute C[i][j] = A[i][j] + B[i][j].

   ->Print C[i][j].

   ->If C[i][j] is even → set allOdd = false.

   ->Else (odd) → set allEven = false.
8. After processing all elements, stop.
9. End   

## Program:
```
import java.util.Scanner;
public class MatrixAdditionCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int rows = sc.nextInt();
        int cols = sc.nextInt();
        int[][] A = new int[rows][cols];
        int[][] B = new int[rows][cols];
        int[][] C = new int[rows][cols];
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                A[i][j] = sc.nextInt();
            }
        }
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                B[i][j] = sc.nextInt();
            }
        }
        boolean allEven = true, allOdd = true;
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                C[i][j] = A[i][j] + B[i][j];
                System.out.print(C[i][j] + " ");
                if (C[i][j] % 2 == 0) {
                    allOdd = false;
                } else {
                    allEven = false;
                }
            }
            System.out.println();
        }
        sc.close();
    }
}
```
Developed by: B. Mahalakshmi

Reg No: 212224040182
## Output:
<img width="537" height="425" alt="image" src="https://github.com/user-attachments/assets/4a9d7054-4cca-45aa-8142-38026212b293" />

## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.
