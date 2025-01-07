## *CODEFORCES*

## *Number of solves: 21*
## *From 26 November 2024    To        2 December 2024*
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/f707045f-908c-4a7b-8c5e-20d880de9c2f">
</p>



## *Lab No : 05*

## *Lab Workout : Functions*

## *Submission Date : 3 December, 2024*

---

## *Problem 1 :*
<div align="justify">
  Write a C program to use three separate functions to:
  a) Take input from a 1D array,
  b) Sum the elements,
  c) Show the sum and elements.
</div>

## *Code :*
~~~C
#include <stdio.h>
void input(int arr[], int n)
{
    for (int i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
    }
}
void print(int arr[], int n)
{
    printf("Printing array: \n");
    for (int i = 0; i < n; i++)
    {
        printf("%d ", arr[i]);
    }
    printf("\n");
}
int sum(int arr[], int n)
{
    int total = 0;
    for (int i = 0; i < n; i++)
    {
        total += arr[i];
    }
    return total;
}
int main()
{
    int n;
    printf("Enter the number of array you want:  ");
    scanf("%d", &n);
    int arr[n];
    input(arr, n);
    print(arr, n);
    printf("sum : %d\n", sum(arr, n));
}
~~~

## *Output :* 
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/c5f82344-81ff-4ff2-95bf-db7e4a52dd1f">
</p>

## *Discussion :*
<div align="justify">
This program takes input for a 1D array, calculates the sum of the elements, and displays the sum along with the elements.
</div>

---

## *Problem 2 :*
<div align="justify">
  Write a C program to use three separate functions to:
  a) Take input from a 2D array,
  b) Sum the elements,
  c) Show the sum and elements.
</div>

## *Code :*
~~~C
#include <stdio.h>

void input(int n, int m, int arr[n][m])
{
    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < m; j++)
        {
            scanf("%d", &arr[i][j]);
        }
    }
}
void print(int n, int m, int arr[n][m])
{
    printf("Printing array: \n");
    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < m; j++)
        {
            printf("%d ", arr[i][j]);
        }
        printf("\n");
    }
    printf("\n");
}
int sum(int n, int m, int arr[n][m])
{
    int total = 0;
    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < m; j++)
        {
            total += arr[i][j];
        }
    }
    return total;
}
int main()
{
    int n, m;
    printf("Enter row : column:  ");
    scanf("%d%d", &n, &m);
    int arr[n][m];
    input(n, m, arr);
    print(n, m, arr);
    printf("sum : %d\n", sum(n, m, arr));
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/eef304c7-db9f-4e22-9934-74f3fa0ee930">
</p>

## *Discussion :*
<div align="justify">
This program takes input for a 2D array, calculates the sum of the elements, and displays the sum and elements.
</div>

---

## *Problem 3 :*
<div align="justify">
  Write a C program to swap two numbers using a function.
</div>

## *Code :*
~~~C
#include <stdio.h>
void swap(int *a, int *b)
{
    *a = (*a) ^ (*b);
    *b = (*a) ^ (*b);
    *a = (*a) ^ (*b);
}

int main()
{
    int a = 10, b = 20;
    printf("a : b  =  %d : %d\n", a, b);
    swap(&a, &b);
    printf("a : b  =  %d : %d\n", a, b);
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/fe71b3aa-c0c5-45b5-b73e-baa563120705">
</p>

## *Discussion :*
<div align="justify">
This program swaps two numbers using a function and displays the results before and after the swap.
</div>

---

## *Problem 4 :*
<div align="justify">
  Write a C program to check if a given number is even or odd using a function.
</div>

## *Code :*
~~~C
#include <stdio.h>

int odd(int n)
{
    return n % 2;
}

int main()
{
    int n;
    printf("Enter the number: ");
    scanf("%d", &n);
    if (odd(n))
    {
        printf("The number is odd\n");
    }
    else
    {
        printf("The number is even\n");
    }
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/88d6aa30-bf7e-4b98-b0ac-e3cbe21953cb">
</p>

## *Discussion :*
<div align="justify">
This program checks whether a number is even or odd using a function.
</div>

---

## *Problem 5 :*
<div align="justify">
  Write a C program to get the largest element of an array using a function.
</div>

## *Code :*
~~~C
#include <stdio.h>

int max_element(int arr[], int n)
{
    int max = arr[0];
    for (int i = 0; i < n; i++)
    {
        if (arr[i] > max)
        {
            max = arr[i];
        }
    }
    return max;
}

int main()
{
    int n;
    printf("Input the numer of element to be sorted: ");
    scanf("%d", &n);
    int arr[n];
    for (int i = 0; i < n; i++)
    {
        printf("element - %d :  ", i);
        scanf("%d", &arr[i]);
    }
    printf("Max element of the array is:  %d \n", max_element(arr, n));
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/6a76b557-a176-459d-b674-ab9af20364ef">
</p>

## *Discussion :*
<div align="justify">
This program finds the largest element of an array using a function.
</div>

---

## *Problem 6 :*
<div align="justify">
  Write a C program to check Armstrong and Perfect numbers using a function.
</div>

## *Code :*
~~~C
#include <stdio.h>
#include <math.h>
int is_armstrong(int n, int len)
{
    int sum = 0, x = n;
    while (x)
    {
        int rem = x % 10;
        sum += pow(rem, len);
        x /= 10;
    }
    return sum == n;
}
int is_perfect(int n)
{
    int sum = 0;
    for (int i = 1; i < n; i++)
    {
        if (n % i == 0)
        {
            sum += i;
        }
    }
    return sum == n;
}

int main()
{
    int n;
    printf("Enter the number:  ");
    scanf("%d", &n);
    int len = 0;
    int x = n;
    while (x)
    {
        int rem = x % 10;
        len++;
        x /= 10;
    }
    if (is_armstrong(n, len))
    {
        printf("The number %d is an Armstrong number\n", n);
    }
    else
    {
        printf("The number %d is NOT an armstrong number\n", n);
    }
    if (is_perfect(n))
    {
        printf("The number %d is a perfect number\n", n);
    }
    else
    {
        printf("The number %d is NOT a perfect number\n", n);
    }
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/a716d382-a5c8-439b-aa43-b93407ef895b">
</p>

## *Discussion :*
<div align="justify">
This program checks whether a number is an Armstrong number and a Perfect number using a function.
</div>

---

## *Problem 7 :*
<div align="justify">
  Write a C program to find the maximum and minimum of some values using a function that returns an array.
</div>

## *Code :*
~~~C
#include <stdio.h>

int max_element(int arr[], int n)
{
    int max = arr[0];
    for (int i = 0; i < n; i++)
    {
        if (arr[i] > max)
        {
            max = arr[i];
        }
    }
    return max;
}
int min_element(int arr[], int n)
{
    int min = arr[0];
    for (int i = 0; i < n; i++)
    {
        if (arr[i] < min)
        {
            min = arr[i];
        }
    }
    return min;
}

int main()
{
    int n = 5;
    printf("Input 5 numers: \n");

    int arr[n];
    for (int i = 0; i < n; i++)
    {
        printf("element - %d :  ", i);
        scanf("%d", &arr[i]);
    }
    printf("Max element of the array is:  %d \n", max_element(arr, n));
    printf("MIN element of the array is:  %d \n", min_element(arr, n));
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/2ff4bc15-3127-458e-bb40-102673358191">
</p>

## *Discussion :*
<div align="justify">
This program finds the maximum and minimum values from an array using a function that returns both values.
</div>

---

## *Problem 8 :*
<div align="justify">
  Write a C program to perform the following operations on two n × m matrices using functions:
  a) Addition,
  b) Subtraction,
  c) Multiplication,
  d) Transpose.
  Input matrix size and elements from the user, and display the results for all operations.
</div>

## *Code :*
~~~C
#include <stdio.h>

void add(int n, int m, int A[n][m], int B[n][m]) {
    printf("Addition of matrices A and B:\n");
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < m; j++) {
            printf("%d ", A[i][j] + B[i][j]);
        }
        printf("\n");
    }
}

void subtract(int n, int m, int A[n][m], int B[n][m]) {
    printf("Subtraction of matrices A and B:\n");
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < m; j++) {
            printf("%d ", A[i][j] - B[i][j]);
        }
        printf("\n");
    }
}

void transpose(int n, int m, int A[n][m]) {
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            printf("%d ", A[j][i]);
        }
        printf("\n");
    }
}

int main() {
    int n, m;

    printf("Enter the number of rows and columns for the matrices (n x m): ");
    scanf("%d %d", &n, &m);

    int A[n][m], B[n][m];

    printf("Enter the elements of matrix A:\n");
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < m; j++) {
            scanf("%d", &A[i][j]);
        }
    }

    printf("Enter the elements of matrix B:\n");
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < m; j++) {
            scanf("%d", &B[i][j]);
        }
    }

    add(n, m, A, B);
    subtract(n, m, A, B);
    printf("Transpose of matrix A:\n");
    transpose(n, m, A);
    printf("Transpose of matrix B:\n");
    transpose(n, m, B);

    return 0;
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/5074972d-0fa6-446c-8147-c629bb08ba04">
</p>

## *Discussion :*
<div align="justify">
This program performs matrix operations such as addition, subtraction, multiplication, and transpose on two n × m matrices.
</div>
