## *CODEFORCES*

## *Number of solves: 07*
## *From 3 December  2024    To        9 December 2024*
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/d73657a6-82be-4829-8bdb-45ffc77251ba">
</p>



## *Lab No : 06*

## *Lab Workout : Recursions*

## *Submission Date : 10 December, 2024*

---
## *Problem 1 :*
<div align="justify"> Write a C program to calculate the power of a number using recursion. </div>

## *Code :*
~~~C
#include <stdio.h>
#define ll long long
ll binary_exp(ll base, ll pow)
{
    if (pow == 0)
    {
        return 1;
    }
    ll temp = binary_exp(base, pow / 2);
    if (pow % 2 == 0)
    {
        return temp * temp;
    }
    else
    {
        return base * temp * temp;
    }
}
int main()
{
    ll a, b;
    printf("Enter the base and pow:  ");
    scanf("%d %d", &a, &b);
    printf("%lld ", binary_exp(a, b));
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/c4aee1aa-25a4-4cd4-8731-a61ab8586c5b">
</p>

## *Discussion :*
<div align="justify"> This program calculates the power of a number using a recursive function. It recursively multiplies the base with itself until the exponent becomes zero. </div>

---

## *Problem 2 :*
<div align="justify"> Write a C program to generate the Fibonacci series up to a given number using recursion. </div>

## *Code :*
~~~C
#include <stdio.h>
int fib(int n)
{
    if (n == 1 || n == 0)
    {
        return n;
    }
    else
    {
        return fib(n - 1) + fib(n - 2);
    }
}
int main()
{
    int n;
    printf("Enter the number of series you want to print : ");
    scanf("%d", &n);
    for (int i = 0; i < n; i++)
    {
        printf("%d ", fib(i));
    }
}


~~~

## *Output :* 
<p align="center">
<p align="center"> <img src="https://github.com/user-attachments/assets/6922e8ac-0cb1-47c0-b2be-0aa372027056" alt="Output for Problem 2"> </p>

## *Discussion :*
<div align="justify"> This program generates the Fibonacci series up to a given number using recursion. It recursively computes each term of the series by summing the two preceding terms, starting from 0 and 1. </div>

---

## *Problem 3 :*
<div align="justify"> Write a C program to calculate the Fibonacci number at a given position using iteration. </div>

## *Code :*
~~~C
#include <stdio.h>

void fib(int x)
{

    if (x == 1)
    {
        printf("%d ", 0);
    }
    else if (x == 2)
    {
        printf("%d %d ", 0, 1);
    }
    else
    {
        int a = 1, b = 2;
        printf("%d %d ", 0, 1);
        for (int i = 2; i < x; i++)
        {
            printf("%d ", a);
            b = a + b;
            a = b - a;
        }
    }
}

int main()
{
    int n;
    printf("Enter the number of series you want to print : ");
    scanf("%d", &n);
    fib(n);
}


~~~

## *Output :* 
<p align="center">
<p align="center"> <img src="https://github.com/user-attachments/assets/62854bf8-e728-4b8b-ac9e-9f02d11bf72e" alt="Output for Problem 3"> </p>

## *Discussion :*
<div align="justify"> This program calculates the Fibonacci number at a specified position using an iterative approach. It iteratively adds the previous two numbers to find the next number in the Fibonacci sequence. </div>
---
