# EX3 Write a program to count the number of digits in an integer.
## DATE: 23.08.2025
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1. Start
2. Input an integer num.
3. Convert num to its absolute value using: num = Math.abs(num) (This handles negative numbers.)
4. If num == 0
→ Print "Number of digits: 1"
→ Stop
5. Else

   ->Initialize count = 0

   ->Repeat while num > 0:

   ->Divide num by 10 → num = num / 10

   ->Increment count by 1
7. After loop ends, print:
"Number of digits: " + count
8. End

## Program:
```
import java.util.Scanner;
public class CountDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num=sc.nextInt();
        num=Math.abs(num);
        if(num==0)
        {
            System.out.println("Number of digits: 1");
        }
      else
      {
          int count=0;
          while(num>0)
          {
              num/=10;
              count++;
          }
          System.out.println("Number of digits: "+ count);
      }
      sc.close();
    }
}
```
Developed by : B. Mahalakshmi 

Reg No : 212224040182
## Output:
<img width="707" height="250" alt="image" src="https://github.com/user-attachments/assets/7f8a15fa-a2ae-403c-9df4-67cdc0c012e6" />

## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.
