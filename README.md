# Reversing-a-Number-using-Recursion-in-C

Reversing a Number using Recursion in C
Given a Number num as an input, write a program for Reversing a Number using Recursion in C Language.

For instance,

Input : 1234
Output : The number after Reversing is 4321
Reversing a Number using Recursion in C
Reversing a Number using Recursion in C
The objective of the program is to recursively reverse the number by break the process down bit by bit. We define a recursive function and set the base case as if Number num exists, if true be perform the required operations shown in the image adjacent. We pop out the last digit and add it to the sum value in such a way that Sum = Sum*10 + Rem where Rem is the popped out digit. We recursively keep on performing these operations until the base base fails and then we return sum val as the output. The recursive step call for the function is  revNumFunc(num/10).

Let’s try and understand the concept better using an example. Let’s Number 1234. In order to reverse the number we’ll first pop out the last element i.e 4. Now we perform the operation Sum = Sum*10 + rem, which will be Sum = 0+ 4. Now we recursively call the function. We check is the number exists, which is true as we’re still lefy with 123. The we perform the same operation again, pop out three, Sum = 40 + 3, Recursive call. We check again, the number is 12, we pop out 2, Sum = 430 +2, recursive call. Check again , the number is 1, pop out 1, Sum = 4320 +1, recursive call. Now when we check if the number exists, the if statement fails as all the digits have been popped out. So we return the sum as the output.

Reversing a Number using Recursion in C
Related Pages
Finding Number of times x digit occurs in a given input
 
Finding number of integers which has exactly x divisors
 
Smallest element in an array

Prime Number

Largest element in an array

While loop in C
C Code
Run
#include <stdio.h>
static int sum=0,rem;

int revNumFunc(int num){
   if(num){
      rem=num%10;
      sum=sum*10+rem;
      revNumFunc(num/10);
   }
   else
      return sum;
}

int main(){
   int num = 1357 ,revNum;
   revNum=revNumFunc(num);
   printf("The number after reversing is :%d",revNum);
   return 0;
}
Output
The number after reversing is :7531
Explanation

The objective of the above code is to break the input number into tiny bits of individual numbers and join them back in a the reverse order using recursion algorithm in C language.

The algorithm for the above code is as follows,

Include all the required libraries using include keyword.
Define a function revNumFunc() which accepts an integer as an argument and returns an integer.
Set base case for the function as if num!=0 or None.
Check is the number exists and then keep breaking down the number num and store the output in sum variable.
Return the sum variable.
In the int main() function initialize all the variables and call the function revNumFunc().
Print the output using printf() function.
The output for the above code is the reverse of the input number i.e 7531.
