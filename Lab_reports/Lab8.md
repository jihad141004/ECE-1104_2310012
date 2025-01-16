## *CODEFORCES*

## *Number of solves: 11*
## *From 7 January 2025   To        13 January 2025*
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/de1eeb47-1f3a-4c93-940b-869a1588d176"/>
</p>


## *Lab No : 08*

## *Lab Workout : Programming Exercises*

## *Submission Date : 14 January, 2025*

---

## *Problem 1 :*
<div align="justify"> Write a program in C to sort an array using a pointer. </div>

## *Code :*
~~~C
#include <stdio.h>
void sort(int arr[], int *n)
{
    for (int i = 0; i < *n - 1; i++)
    {
        for (int j = 0; j < *n; j++)
        {
            if (*(arr + i) < *(arr + j))
            {
                *(arr + i) = *(arr + i) ^ *(arr + j);
                *(arr + j) = *(arr + i) ^ *(arr + j);
                *(arr + i) = *(arr + i) ^ *(arr + j);
            }
        }
    }
}

int main()
{
    printf("Enter the Number of element to store in the array: ");
    int n;
    scanf("%d", &n);
    int arr[n];
    for (int i = 0; i < n; i++)
    {
        printf("element %d : ", i + 1);
        scanf("%d", &arr[i]);
    }
    sort(arr, &n);
    printf("After sorting: ");
    for (int i = 0; i < n; i++)
    {
        printf("%d  ", arr[i]);
    }
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/827ec4a9-c829-44b6-ab8d-0323e7743c66">
</p>

## *Discussion :*
<div align="justify"> This program takes an array as input, uses pointers to sort the array in ascending order, and then prints the sorted array. </div>

---

## *Problem 2 :*
<div align="justify"> Write a program in C to find the GCD of two numbers using recursion. </div>

## *Code :*
~~~C
#include <stdio.h>
#define ll long long
int gcd(int a, int b)
{
    if (b == 0)
    {
        return a;
    }
    return gcd(b, a % b);
}
int main()
{
    int a, b;
    printf("Enter 1st number: ");
    scanf("%d", &a);
    printf("Enter 2nd number: ");
    scanf("%d", &b);
    printf("The GCD of %d and %d is:  %d ",a, b, gcd(a, b));
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 2 output image" src="https://github.com/user-attachments/assets/849ae094-0fc0-45da-919d-6cd22303c609">
</p>

## *Discussion :*
<div align="justify"> This program computes the GCD of two numbers using recursion. The function `gcd` recursively finds the greatest common divisor by applying the Euclidean algorithm. </div>

---

## *Problem 3 :*
<div align="justify"> Write a C program to multiply two matrices using recursion. </div>

## *Code :*
~~~C
....
~~~

## *Output :* 
<p align="center">
<img alt="e" src="">
</p>

## *Discussion :*
<div align="justify">. </div>

---

## *Problem 4 :*
<div align="justify"> Codeforces Problem. </div>

## *Code :*
~~~C
#include <stdio.h>
void solve()
{
    int n;
    scanf("%d", &n);
    int count = 0;
    for (int i = 1; i <= n; i++)
    {
        for (int j = 1; j < n; j++)
        {
            if (i + j == n)
            {
                count++;
            }
        }
    }
    printf("%d\n", count);
}

int main()
{
    int tt;
    scanf("%d", &tt);
    while (tt--)
        solve();
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 4 output image" src="https://github.com/user-attachments/assets/b8196115-babd-43f1-b43f-246d11e69f06">
</p>

## *Discussion :*
<div align="justify"> This problem involves solving a given problem from Codeforces. The solution approach will depend on the specific problem statement. </div>

---

## *Problem 5 :*
<div align="justify"> Codeforces Problem. </div>

## *Code :*
~~~C
#include <stdio.h>
void solve()
{
    int n;
    scanf("%d", &n);
    int count = 0;
    for (int i = 0; i < n; i++)
    {
        int sum = 0;
        for (int j = 0; j < 3; j++)
        {
            int x;
            scanf("%d", &x);
            sum += x;
        }
        if (sum >= 2)
        {
            count++;
        }
    }
    printf("%d", count);
}
int main()
{

    solve();
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 5 output image" src="https://github.com/user-attachments/assets/d348a9cd-d457-4feb-9f2a-808b08327547">
</p>

## *Discussion :*
<div align="justify"> This problem involves solving another given problem from Codeforces. The solution approach will depend on the specific problem statement. </div>

---
