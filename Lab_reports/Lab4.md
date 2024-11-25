

## *Lab No : 04*

## *Lab Workout : Opperation on Arrays*

## *Submission Date : 25 November, 2024*

---

## *Problem 1 :*
<div align="justify">
  Write a C program to copy the elements of one array into another array.
</div>

## *Code :*
```C
#include <stdio.h>


void solve(){
    int n;
    printf("Input the number of elements to be stored in the array: ");
    scanf("%d", &n);

    int arr1[n], arr2[n];
    printf("Input %d elements in the array:\n", n);
    for(int i = 0; i < n; i++) {
        printf("element - %d : ", i);
        scanf("%d", &arr1[i]);
    }
    for(int i = 0; i < n; i++) {
        arr2[i] = arr1[i];
    }
    printf("The elements stored in the first array are:\n");
    for(int i = 0; i < n; i++) {
        printf("%d ", arr1[i]);
    }
    printf("\n");
    printf("The elements copied into the second array are:\n");
    for(int i = 0; i < n; i++) {
        printf("%d ", arr2[i]);
    }
    printf("\n");
}
int main() {
   solve();
}

```

## *Output :* 
*Output description goes here*

<p align="center">
<img alt="Problem 1 output image" src="image_url">
</p>

## *Discussion :*
<div align="justify">
This program copies all elements from one array to another using simple iteration.
</div>

---

## *Problem 2 :*
<div align="justify">
  Write a C program to count the total number of duplicate elements in an array.
</div>

## *Code :*
```C
#include <stdio.h>

void solve() {
    int n;
    printf("Input the number of elements to be stored in the array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Input %d elements in the array:\n", n);
    for (int i = 0; i < n; i++) {
        printf("element - %d : ", i);
        scanf("%d", &arr[i]);
    }

    int duplicateCount = 0;
    for (int i = 0; i < n; i++) {
        int count = 0;
        for (int j = 0; j < n; j++) {
            if (arr[i] == arr[j] && i!=j && arr[i]!=-1) {
                count++;
                arr[j]= -1;
            }
        }
        if (count>0) {
            duplicateCount++;
        }
    }

    printf("Total number of duplicate elements found in the array is : %d\n", duplicateCount);
}

int main() {
    solve();
}

```

## *Output :* 
*Output description goes here*

<p align="center">
<img alt="Problem 2 output image" src="image_url">
</p>

## *Discussion :*
<div align="justify">
This program counts how many elements appear more than once in the array.
</div>

---

## *Problem 3 :*
<div align="justify">
  Write a C program to print all unique elements in an array.
</div>

## *Code :*
```C
#include <stdio.h>

void solve() {
    int n;
    printf("Input the number of elements to be stored in the array: ");
    scanf("%d", &n);

    int hash[100000] = {0};
    int arr[n];
    printf("Input %d elements in the array:\n", n);
    for (int i = 0; i < n; i++) {
        printf("element - %d : ", i);
        scanf("%d", &arr[i]);
        hash[arr[i]]++;
    }
    printf("The unique elements found in the array are:\n");
    for (int i = 0; i < n; i++) {
        if (hash[arr[i]] == 1) {
            printf("%d ", arr[i]);
            hash[arr[i]] = -1;
        }
    }
    printf("\n");
}

int main() {
    solve();
}

```

## *Output :* 
*Output description goes here*

<p align="center">
<img alt="Problem 3 output image" src="image_url">
</p>

## *Discussion :*
<div align="justify">
This program identifies and prints all elements that appear only once in the array.
</div>

---

## *Problem 4 :*
<div align="justify">
  Write a C program to count the frequency of each element of an array.
</div>

## *Code :*
```C
#include <stdio.h>

void solve() {
    int n;
    printf("Input the number of elements to be stored in the array: ");
    scanf("%d", &n);

    int hash[100000] = {0};
    int arr[n];
    printf("Input %d elements in the array:\n", n);
    for (int i = 0; i < n; i++) {
        printf("element - %d : ", i);
        scanf("%d", &arr[i]);
        hash[arr[i]]++;
    }
    printf("The frequency of all elements of an array:\n");
    for (int i = 0; i < n; i++) {
        if (hash[arr[i]] != -1) {
            printf("%d occurs %d times\n", arr[i], hash[arr[i]]);
            hash[arr[i]] = -1;
        }
    }
}

int main() {
    solve();
}

```

## *Output :* 
*Output description goes here*

<p align="center">
<img alt="Problem 4 output image" src="image_url">
</p>

## *Discussion :*
<div align="justify">
This program counts how often each distinct element appears in the array.
</div>

---

## *Problem 5 :*
<div align="justify">
  Write a C program to separate odd and even integers into separate arrays.
</div>

## *Code :*
```C
#include <stdio.h>

void solve() {
    int n;
    printf("Input the number of elements to be stored in the array: ");
    scanf("%d", &n);

    int arr[n], even[n], odd[n];
    int e_count = 0, o_count = 0;

    printf("Input %d elements in the array:\n", n);
    for (int i = 0; i < n; i++) {
        printf("element - %d : ", i);
        scanf("%d", &arr[i]);
        if (arr[i] % 2 == 0) {
            even[e_count] = arr[i];
            e_count++;
        } else {
            odd[o_count] = arr[i];
            o_count++;
        }
    }
    printf("The Even elements are :\n");
    for (int i = 0; i < e_count; i++) {
        printf("%d ", even[i]);
    }
    printf("\n");
    printf("The Odd elements are :\n");
    for (int i = 0; i < o_count; i++) {
        printf("%d ", odd[i]);
    }
    printf("\n");
}

int main() {
    solve();
}

```

## *Output :* 
*Output description goes here*

<p align="center">
<img alt="Problem 5 output image" src="image_url">
</p>

## *Discussion :*
<div align="justify">
This program separates the odd and even numbers from the original array into two different arrays.
</div>

---

## *Problem 6 :*
<div align="justify">
  Write a C program to find the smallest missing element in a sorted array.
</div>

## *Code :*
```C
#include <stdio.h>

void solve() {
    int arr[8] = {0, 1, 3, 4, 5, 6, 7, 9};
    int pattern = arr[0] - 0;

    for (int i = 0; i < 8; i++) {
        if (arr[i] != i + pattern) {
            printf("Missing smallest element is: %d\n", i + pattern);
            return;
        }
    }
}

int main() {
    solve();
}

```

## *Output :* 
*Output description goes here*

<p align="center">
<img alt="Problem 6 output image" src="image_url">
</p>

## *Discussion :*
<div align="justify">
This program identifies the smallest integer that is missing in a sorted array.
</div>

---

## *Problem 7 :*
<div align="justify">
  Write a C program to sort an array of 0s, 1s, and 2s.
</div>

## *Code :*
```C
#include <stdio.h>

void solve() {
    int n = 12;
    int arr[12] = {0, 1, 2, 2, 1, 0, 0, 2, 0, 1, 1, 0};
    printf("The given array is : ");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
   for(int i = 0; i<n-1; i++){
    for(int j = i+1; j<n; j++){
        if(arr[i]>arr[j]){
            arr[i] = arr[i]^arr[j];
            arr[j] = arr[i]^arr[j];
            arr[i] =  arr[i]^arr[j];
            }
        }
   }
    printf("After sorting the elements in the array are:\n");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

int main() {
    solve();
}

```

## *Output :* 
*Output description goes here*

<p align="center">
<img alt="Problem 7 output image" src="image_url">
</p>

## *Discussion :*
<div align="justify">
This program sorts an array containing only 0s, 1s, and 2s using a counting or sorting algorithm.
</div>

---

## *Problem 8 :*
<div align="justify">
  Write a C program to insert values into a sorted array.
</div>

## *Code :*
```C
#include <stdio.h>

void solve() {
    int n;

    printf("Input number of elements you want to insert (max 100): ");
    scanf("%d", &n);

    int arr[n + 1];

    printf("Input %d elements in the array in ascending order:\n", n);
    for (int i = 0; i < n; i++) {
        printf("element - %d : ", i);
        scanf("%d", &arr[i]);
    }
    int key ;
    printf("Input the value to be inserted: ");
    scanf("%d", &key);

    int j = n-1;
    while(arr[j]>key){
        arr[j+1] = arr[j];
        j--;
    }
    arr[j+1] = key;

    printf("After Insert the list is :\n");
    for (int i = 0; i <= n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

int main() {
    solve();
    return 0;
}

```

## *Output :* 
*Output description goes here*

<p align="center">
<img alt="Problem 8 output image" src="image_url">
</p>

## *Discussion :*
<div align="justify">
This program inserts a new value into the correct position in a sorted array, maintaining the order.
</div>

---
