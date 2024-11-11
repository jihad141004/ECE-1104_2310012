## *Lab No : 02*

## *Lab Workout : Solve some basic problem in c*

## *Submission Date : November 11, 2024*

---

## *Problem 1 :*
<div align="justify">
  Write a program in C to make such a pattern like a right angle triangle
with a number which will repeat a number in a row.
</div>

## *Code :*
```C
#include <stdio.h>
void solve()
{
  int n = 4;
  for (int i = 1; i <= n; i++)
  {
    for (int j = 1; j <= i; j++)
    {
      printf("%d", i);
    }
    printf("\n");
  }
}
int main()
{
  solve();
}
```


## *Output :* 
*Printing right angle triangle*
<p align="center">
<img alt="2310012_lab2_prob_1" src="https://github.com/user-attachments/assets/3e45dba4-33c7-4039-93a1-a17c5ffc18f6">
</p>

## *Discussion :*
<div align="justify">
In this Problem,we made such a pattern like a right angle triangle
with a number which will repeat a number in a row.
</div>


## *Problem 2 :*
<div align="justify">
 Write a C program to make such a pattern like a pyramid with a
number which will repeat the number in the same row.

</div>

## *Code :*
```C
#include <stdio.h>
void solve()
{
  int n = 4;
  for (int i = 1; i <= n; i++)
  {
    for (int j = 1; j <= n; j++)
    {
      if (i + j >= n + 1)
      {
        printf("%d ", i);
      }
      else
      {
        printf(" ");
      }
    }
    printf("\n");
  }
}
int main()
{
  solve();
}

```


## *Output :* 
*Printing a Pyramid with number*
<p align="center">
<img alt="2310012_lab2_prob_2" src="https://github.com/user-attachments/assets/e0c49797-b114-41b1-8e24-9deaec5ae500">
</p>

## *Discussion :*
<div align="justify">
In this Problem,we made a C program to make such a pattern like a pyramid with a
number which will repeat the number in the same row.

  
## *Problem 3 :*
<div align="justify">
Write a C program to display the pattern as a pyramid using
asterisks, with each row containing an odd number of asterisks
</div>

## *Code :*
```C
#include <stdio.h>
void solve()
{
  int n = 3;
  for (int i = 0; i < n; i++)
  {
    for (int j = 0; j < 2*n-1; j++)
    {
      if (i>=j-n+1 && i+j>=n-1)
      {
        printf("*");
      }
      else
      {
        printf(" ");
      }
    }
    printf("\n");
  }
}
int main()
{
  solve();
}

```


## *Output :* 
*Printing pyramid with asterisks*
<p align="center">
<img alt="2310012_lab2_prob_3" src="https://github.com/user-attachments/assets/28c9471a-c8f8-416a-946e-255272c8e787">
</p>

## *Discussion :*
<div align="justify">
In this Problem,we made a C program to display the pattern as a pyramid using
asterisks, with each row containing an odd number of asterisks.
</div>


## *Problem 4 :*
<div align="justify">
  Write a program in C to find the number and sum of all integers
  between 100 and 200 which are divisible by 9.

</div>

## *Code :*
```C
#include <stdio.h>
void solve()
{
  printf("Numbers between 100 and 200, divisible by 9 :");
  int sum = 0;
  for (int i = 100; i <= 200; i++)
  {
    if (i % 9 == 0)
    {
      printf("%d ", i);
      sum += i;
    }
  }
  printf("\nSum:  %d", sum);
}
int main()
{
  solve();
}

```


## *Output :* 
*Calculating Average*
<p align="center">
<img alt="2310012_lab2_prob_4" src="https://github.com/user-attachments/assets/0ef5bd9d-82ce-4d6a-8540-c7d332157b5f">
</p>

## *Discussion :*
<div align="justify">
In this Problem, we created a program in C to find the number and sum of all integers
between 100 and 200 which are divisible by 9.
</div>


## *Problem 5 :*
<div align="justify">
  Write a program in C to display a pattern like a diamond.
</div>

## *Code :*
```C
#include <stdio.h>
void solve()
{
  int n = 5;
  for (int i = 0; i < n; i++)
  {
    for (int j = 0; j < 2 * n - 1; j++)
    {
      if (i >= j - n + 1 && i + j >= n - 1)
      {
        printf("*");
      }
      else
      {
        printf(" ");
      }
    }
    printf("\n");
  }

  n--;
  for (int i = 0; i < n; i++)
  {
    printf(" ");
    for (int j = 0; j < 2 * n - 1; j++)
    {
      if (i <= j && i + j <= 2 * n - 2)
      {
        printf("*");
      }
      else
      {
        printf(" ");
      }
    }
    printf("\n");
  }
}
int main()
{
  solve();
}

```


## *Output :* 
*Printing Diamond shape*
<p align="center">
<img alt="2310012_lab2_prob_5" src="https://github.com/user-attachments/assets/e6f9a149-5b52-4ba4-9cda-c20f1e9247cb">
</p>

## *Discussion :*
<div align="justify">
In this Problem, we created   a program in C to display a pattern like a diamond.

</div>


## *Problem 6 :*
<div align="justify">
 Write a C program to check whether a number is a palindrome or not.
</div>

## *Code :*
```C
#include <stdio.h>
void solve()
{
  int n;
  printf("Enter the Number: ");
  scanf("%d", &n);
  int copy = n, reverse = 0;
  while (n)
  {
    int rem = n % 10;
    reverse = (reverse * 10) + rem;
    n /= 10;
  }
  printf("%d ", copy);
  if (copy == reverse)
  {
    printf("is a palindrome number. \n");
  }
  else
  {
    printf(" is not a palindrome number. \n");
  }
}
int main()
{
  solve();
}

```


## *Output :* 
*Checking Palindrome or not*
<p align="center">
<img alt="2310012_lab2_prob_6" src="https://github.com/user-attachments/assets/8fc5fc60-e94c-491d-aedf-f71bab89cd78">
</p>

## *Discussion :*
<div align="justify">
In this Problem, we craeted a program that checks if the given number in palindrome or not
</div>


## *Problem 7 :*
<div align="justify">
Write a C program that calculates the sum of even and odd numbers from 1 to
50 using do-while loops.

## *Code :*
```C
#include <stdio.h>
void solve()
{
  int i = 1;
  int odd_sum = 0, even_sum = 0;
  do
  {
    if (i & 1)
    {
      odd_sum += i;
    }
    else
    {
      even_sum += i;
    }
    i++;
  } while (i <= 50);

  printf("Sum of Even number: %d\n", even_sum);
  printf("Sum of Odd number : %d\n", odd_sum);
}
int main()
{
  solve();
}

```


## *Output :* 
*Calculating sum*
<p align="center">
<img alt="2310012_lab2_prob_7" src="https://github.com/user-attachments/assets/1efb6614-095e-4a7b-a073-30cc18ec5d5a">
</p>

## *Discussion :*
<div align="justify">
In this Problem, we created a C program that calculates the sum of even and odd numbers from 1 to
50 using do-while loops0
</div>


## *Problem 8 :*
<div align="justify">
8. Write a C program to find the largest of three numbers.
</div>

## *Code :*
```C
#include <stdio.h>

void solve()
{
  int a, b, c;
  printf("1st Number : ");
  scanf("%d", &a);
  printf("2nd Number : ");
  scanf("%d", &b);
  printf("3rd Number : ");
  scanf("%d", &c);
  if (a >= b && a >= c)
  {
    printf("The 1st Number is the greatest among the three.\n");
  }
  else if (b >= c && b >= a)
  {
    printf("The 2nd Number is the greatest among the three.\n");
  }
  else
  {
    printf("The 3rd Number is the greatest among the three.\n");
  }
}

int main()
{
  solve();
}
```


## *Output :* 
*Checking the largest number*
<p align="center">
<img alt="2310012_lab2_prob_8" src="https://github.com/user-attachments/assets/4503e75c-3c86-49b1-85a2-8a8aebd1a8b8">
</p>

## *Discussion :*
<div align="justify">
In this Problem,we created a C program to find the largest of three numbers.

</div>

