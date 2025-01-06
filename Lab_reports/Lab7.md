
## *Lab No : 07*

## *Lab Workout : Pointers*

## *Submission Date : 7 January, 2025*

---

## *Problem 1 :*
<div align="justify"> Write a program in C to add two numbers using pointers. </div>

## *Code :*
~~~C
#include <stdio.h>
void solve()
{
    int a, b;
    printf("Enter two number:  ");
    scanf("%d%d", &a, &b);
    int *p1, *p2;
    p1 = &a;
    p2 = &b;
    printf("Output: %d\n", *p1 + *p2);
}
int main()
{
    solve();
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/dca18bc2-76b7-4a88-991d-26e370c36b30">
</p>

## *Discussion :*
<div align="justify"> This program takes two numbers as input, passes them by reference to a function, and calculates their sum using pointers. </div>

---

## *Problem 2 :*
<div align="justify"> Write a program in C to add three numbers using pointers. </div>

## *Code :*
~~~C
#include <stdio.h>
void solve()
{
    int a, b, c;
    printf("Enter three numbers:  ");
    scanf("%d%d%d", &a, &b, &c);
    int *p1, *p2, *p3;
    p1 = &a;
    p2 = &b;
    p3 = &c;
    printf("Output: %d\n", *p1 + *p2 + *p3);
}
int main()
{
    solve();
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 2 output image" src="https://github.com/user-attachments/assets/1e8b3f1c-2aec-4853-a14e-74a63c292263">
</p>

## *Discussion :*
<div align="justify"> This program takes three numbers as input, passes them by reference to a function, and calculates their sum using pointers. </div>

---

## *Problem 3 :*
<div align="justify"> Write a program in C to find the maximum number between two numbers using a pointer. </div>

## *Code :*
~~~C
#include <stdio.h>
void solve()
{
    printf("Enter two numbers: ");
    int a, b;
    scanf("%d%d", &a, &b);
    int *p1, *p2;
    p1 = &a;
    p2 = &b;
    printf("Maximum  :  ");
    if (*p1 > *p2)
    {
        printf("%d\n", *p1);
    }
    else
    {
        printf("%d\n", *p2);
    }
}
int main()
{
    solve();
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 3 output image" src="https://github.com/user-attachments/assets/cff55cf5-63ae-4b75-bef4-b761d5770373">
</p>

## *Discussion :*
<div align="justify"> This program takes two numbers as input and uses pointers to determine and print the larger number. </div>

---

## *Problem 4 :*
<div align="justify"> Write a program in C to store n elements in an array and print the elements using a pointer. </div>

## *Code :*
~~~C
#include <stdio.h>
#define ll long long
void solve()
{
    int arr[5] = {10, 20, 30, 40, 50};
    for (int i = 0; i < 5; i++)
    {
        printf("%d  ", *(arr + i));
    }
}
int main()
{
    solve();
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 4 output image" src="https://github.com/user-attachments/assets/a0d0cc35-5721-42f7-8908-fad5c10b3ad5">
</p>

## *Discussion :*
<div align="justify"> This program stores n elements in an array and prints them using a pointer. The pointer is used to access each element in the array. </div>

---

## *Problem 5 :*
<div align="justify"> Write a program in C to swap elements using call by reference. </div>

## *Code :*
~~~C
#include <stdio.h>
void swap(int *a, int *b)
{
    (*a) = (*a) ^ (*b);
    (*b) = (*a) ^ (*b);
    (*a) = (*a) ^ (*b);
}
int main()
{
    int a = 10, b = 20;
    printf("Before swap:  a = %d      b = %d\n", a, b);
    swap(&a, &b);
    printf("After swap :  a = %d      b = %d\n", a, b);
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 5 output image" src="https://github.com/user-attachments/assets/2abadee7-6f73-4362-b6ad-ffeb09e7612f">
</p>

## *Discussion :*
<div align="justify"> This program swaps two numbers using call by reference. The addresses of the two numbers are passed to the function, and the swap is performed directly on the original variables. </div>

---

## *Problem 6 :*
<div align="justify"> Write a program in C to sort an array using a pointer. </div>

## *Code :*
~~~C
#include <stdio.h>
void sort(int arr[], int *n)
{
    for (int i = 0; i < *n - 1; i++)
    {
        for (int j = i + 1; j < *n; j++)
        {
            if (arr[i] > arr[j])
            {
                arr[i] = arr[i] ^ arr[j];
                arr[j] = arr[i] ^ arr[j];
                arr[i] = arr[i] ^ arr[j];
            }
        }
    }
}
int main()
{
    int n = 5;
    int arr[5] = {50, 30, 10, 40, 20};
    sort(arr, &n);
    for (int i = 0; i < n; i++)
    {
        printf("%d  ", arr[i]);
    }
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 6 output image" src="https://github.com/user-attachments/assets/eabbe584-de1a-4f12-aeab-7d93021e321b">
</p>

## *Discussion :*
<div align="justify"> This program sorts an array using a pointer. It uses pointer arithmetic to access and compare array elements, performing the sorting in-place. </div>

---

## *Problem 7 :*
<div align="justify"> Write a C program to demonstrate how a function returns a pointer. </div>

## *Test Data :*
Input the first number: 5  
Input the second number: 6  

## *Expected Output :*
The number 6 is larger.

## *Code :*
~~~C
#include <stdio.h>
int *max(int p1, int p2)
{
    if (p1 > p2)
    {
        return (&p1);
    }
    else
    {
        return (&p2);
    }
}
int main()
{
    int a, b;
    printf("Input Two NUmbers:  ");
    scanf("%d %d", &a, &b);
    printf("Maximum NUM:   %d \n", *max(a, b));
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 7 output image" src="https://github.com/user-attachments/assets/ff14e3b2-d797-408d-91a6-7537e8a6a9b6">
</p>

## *Discussion :*
<div align="justify"> This program demonstrates a function returning a pointer. The function `find_max` returns a pointer to the larger of two numbers, and the main function dereferences this pointer to print the larger value. </div>

---

## *Problem 8 :*
<div align="justify"> Write a program in C to compute the sum of all elements in an array using pointers. </div>

## *Code :*
~~~C
#include <stdio.h>
#define ll long long
int sum()
{
    int arr[5] = {10, 20, 30, 40, 50};
    int sum = 0;
    for (int i = 0; i < 5; i++)
    {
        sum += *(arr + i);
    }
    return sum;
}
int main()
{
    printf("Sum:    %d \n", sum());
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 8 output image" src="https://github.com/user-attachments/assets/fc59de01-2cea-4105-b722-7fe9bfa9ce90">
</p>

## *Discussion :*
<div align="justify"> This program calculates the sum of all elements in an array using pointers. It iterates over the array using pointer arithmetic to access and sum the elements. </div>

---

## *Problem 9 :*
<div align="justify"> Write a program in C to print the elements of an array in reverse order. </div>

## *Code :*
~~~C
#include <stdio.h>
#define ll long long
void solve()
{
    int arr[5] = {10, 20, 30, 40, 50};
    for (int i = 4; i >= 0; i--)
    {
        printf("%d  ", *(arr + i));
    }
}
int main()
{
    solve();
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 9 output image" src="https://github.com/user-attachments/assets/9e88af93-ad74-4a60-bc80-9f0ce69ebb30">
</p>

## *Discussion :*
<div align="justify"> This program prints the elements of an array in reverse order using a pointer. The pointer accesses array elements starting from the end. </div>

---

## *Problem 10 :*
<div align="justify"> Write a program in C to print all the alphabets using a pointer. </div>

## *Code :*
~~~C
#include <stdio.h>
#define ll long long
void solve()
{
    char ch = 'A';
    char *p = &ch;
    for (int i = 0; i < 26; i++)
    {
        printf("%c  ", (*p)++);
    }
}
int main()
{
    printf("Alphabets:  ");
    solve();
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 10 output image" src="https://github.com/user-attachments/assets/ec62d999-260b-454d-8ac3-4c0803b14784">
</p>

## *Discussion :*
<div align="justify"> This program prints all the alphabets using a pointer. The pointer traverses the string containing the alphabets and prints each character. </div>

---

## *Problem 11 :*
<div align="justify"> Access values of 1- and 2-dimensional arrays using pointers. </div>

## *Code :*
~~~C
#include <stdio.h>
#define ll long long
void array_2d(int n, int m, int arr[n][m])
{
    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < m; j++)
        {
            printf("%d ", *(*(arr + i) + j));
        }
        printf("\n");
    }
}
void array_1d(int arr[], int n)
{
    for (int i = 0; i < n; i++)
    {
        printf("%d ", *(arr + i));
    }
}
int main()
{
    int arr2[3][3] = {{1, 2, 3}, {3, 4, 5}, {6, 7, 7}};
    int arr1[4] = {2, 3, 5, 6};
    array_1d(arr1, 4);
    printf("\n\n");
    array_2d(3, 3, arr2);
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 11 output image" src="https://github.com/user-attachments/assets/24631a6f-ab8b-4e7d-b100-672ff456c936">
</p>

## *Discussion :*
<div align="justify"> This program demonstrates accessing values of both 1D and 2D arrays using pointers. The pointer is used to access the array elements by incrementing the pointer values appropriately. </div>

---
