# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE:18.08.2025
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1. Start the program.
2. Read the number of elements and store them in an array.
3. Define a recursive function findMin() that compares elements to find the minimum.
4. Base condition: If the array has one element, return that element.
5. Recursive step: Compare the last element with the minimum of the rest of the array and return the smaller one.
6. Display the minimum value.
7. Stop the program.  

## Program:
```
import java.util.*;
public class Main {
    static int getMin(int[] arr, int i, int n) {
        if (i == n - 1) {
            return arr[i];
        }
        int minRest = getMin(arr, i + 1, n);
        return Math.min(arr[i], minRest);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}
```
Developed By: Mahalakshmi B

Reg No: 212224040182
## Output:
<img width="405" height="177" alt="image" src="https://github.com/user-attachments/assets/15ea8809-6655-48e3-889c-255ea6462f54" />

## Result:
Thus the JAVA program to find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully
