# Ex2 Count how many times a number appears in an array recursively.
## DATE: 18.08.2025
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1. Start
2. Read the size of the array (size).
3. If size ≤ 0
   → Print "Invalid array size. Must be positive."
   → Stop
4. Create an integer array arr of length size.
5. Input array elements one by one and store them in arr.
6. Read the target number to be counted.
7. Call the recursive function
   countOccurrences(arr, size, target)

## Program:
```
import java.util.Scanner;
public class CountOccurrences {
    public static int countOccurrences(int[] arr, int n, int target) {
        if (n==0)
        return 0;
        if (arr[n-1]==target)
        {
            return 1+countOccurrences(arr,n-1,target);
        }
        else
        return countOccurrences(arr,n-1,target);
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int size = scanner.nextInt();
        if (size <= 0) {
            System.out.println("Invalid array size. Must be positive.");
            return;
        }
        int[] arr = new int[size];
        for (int i = 0; i < size; i++) {
            arr[i] = scanner.nextInt();
        }
        int target = scanner.nextInt();
        int count = countOccurrences(arr, size, target);
        System.out.println("The number " + target + " appears " + count + " time(s) in the array.");
        scanner.close();
    }
}
```
Developed by: B. Mahalakshmi

Reg No: 212224040182
## Output:
<img width="1076" height="400" alt="image" src="https://github.com/user-attachments/assets/ca50b63a-8ef4-4db4-a0a6-36f485d76869" />

## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
