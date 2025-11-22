# Ex5 Count Inversions in an Array
## DATE:23.08.2025
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1. Start
2. Read integer n and array arr of size n.
3. Call mergeSortAndCount(arr, 0, n-1):
4. If left >= right, return 0.
5. Find midpoint mid = (left + right) / 2.
6. Recursively count inversions in left half.
7. Recursively count inversions in right half.
8. Count inversions while merging the two halves using mergeAndCount().
9. Return total count.
10. In mergeAndCount(arr, left, mid, right):
11. Create leftArr and rightArr from the two halves.
12. Merge them back while counting:
13. If leftArr[i] > rightArr[j], then all elements from leftArr[i ... end] form inversions → add (leftArr.length - i) to count
14. Return the merge inversion count.
15. Print the total inversion count.
16. End  

## Program:
```
import java.util.Scanner;
public class CountInversions {
    public static int mergeSortAndCount(int[] arr, int left, int right) 
    {
           // Type your code here
       if (left >= right) return 0;
       int mid = (left + right) / 2;
       int count =0;
       count += mergeSortAndCount(arr,left,mid);
       count += mergeSortAndCount(arr,mid+1,right);
       count += mergeAndCount(arr, left, mid, right);
       return count;
    }

    private static int mergeAndCount(int[] arr, int left, int mid, int right)
    {
        // Type your code here
        int[] leftArr= new int[mid-left+1];
        int[] rightArr= new int[right-mid];
        for (int i=0;i<leftArr.length;i++){
            leftArr[i]=arr[left+i];
        }
        for (int i=0;i<rightArr.length;i++)
        {
            rightArr[i]= arr[mid+1+i];
        }
        int i=0,j=0,k=left,count=0;
        while(i<leftArr.length && j < rightArr.length){
            if(leftArr[i] <= rightArr[j]){
                arr[k++]=leftArr[i++];
            }
            else
            {
                arr[k++]= rightArr[j++];
                count += (leftArr.length-i);
            }
        }
        while(i<leftArr.length){
            arr[k++]=leftArr[i++];
        }
        while(j<rightArr.length){
            arr[k++]=rightArr[j++];
        }
        return count;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) arr[i] = sc.nextInt();
        System.out.println(mergeSortAndCount(arr, 0, n - 1));
    }
}
```
Developed by: Mahalakshmi B

Reg No: 212224040182
## Output:
<img width="437" height="307" alt="image" src="https://github.com/user-attachments/assets/46f18aaa-5371-4ca0-8c2d-39622463a4fc" />

## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
