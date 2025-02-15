## *Lab No : 01*

## *Lab Workout : Solve some basic problem in c*

## *Submission Date : November 4, 2024*

---

## *Problem 1 :*
<div align="justify">
  Write a C program that accepts two integers from the user and calculates the
sum of the two integers.
</div>

## *Code :*
```C
#include<stdio.h>
void solve(){
    long long a, b;
    printf("Enter number 1:   ");
    scanf("%lld", &a);
    printf("Enter number 2:   ");
    scanf("%lld", &b);
    printf("Sum:  %lld", a+b);
}

int main(){
    solve();
}

```


## *Output :* 
*Doing a Sum*
<p align="center">
<img alt="2310012_lab1_prob_1" src="https://github.com/user-attachments/assets/c7db6759-ea2b-448d-9be2-6f98645a5db2">
</p>

## *Discussion :*
<div align="justify">
In this Problem, this program accepts two integars from user & then calculates its sum.
</div>


## *Problem 2 :*
<div align="justify">
 Write a C program to convert specified days into years, weeks and days.
(Note: Ignore leap year.)
</div>

## *Code :*
```C
#include<stdio.h>
void solve(){
    long long days;
    printf("Enter the number of days:    ");
    scanf("%lld", &days);
    long long year = days/365;
    days%=365;
    int weeks = days/7;
    days%=7;

    printf("Year  : %lld\n", year);
    printf("Weeks : %d\n", weeks);
    printf("Days  : %lld\n", days);

}

int main(){
    solve();
}

```


## *Output :* 
*convertING specified days into years, weeks and days*
<p align="center">
<img alt="2310012_lab1_prob_2" src="https://github.com/user-attachments/assets/548948b6-a725-47ad-bfe3-a5cb8c0de44f">
</p>

## *Discussion :*
<div align="justify">
In this Problem, this program accepts Days and convert it into Years, weeks and days.
  


## *Problem 3 :*
<div align="justify">
 Write a C program to calculate the distance between two points.
</div>

## *Code :*
```C
#include<stdio.h>
#include<math.h>
void solve(){
    int x1, x2, y1, y2;
    printf("Input x1:  ");
    scanf("%d", &x1);
    printf("Input y1:  ");
    scanf("%d", &y1);
    printf("Input x2:  ");
    scanf("%d", &x2);
    printf("Input y2:  ");
    scanf("%d", &y2);

    double ans = sqrt((x1-x2)*(x1-x2) + (y1-y2)*(y1-y2));
    printf("Distance: %lf", ans);
}
int main(){
    solve();
}
```


## *Output :* 
*calculating distance*
<p align="center">
<img alt="2310012_lab1_prob_3" src="https://github.com/user-attachments/assets/8a9378b3-02ae-4e13-9ae0-b9ce41973cd1">
</p>

## *Discussion :*
<div align="justify">
In this Problem, this program accepts two points and calculate its distance.
</div>


## *Problem 4 :*
<div align="justify">
  Write a C program that accepts two item's weight and number of purchases
(floating point values) and calculates their average value..
</div>

## *Code :*
```C
#include<stdio.h>

void solve(){
    int w1, w2, i1, i2;
    printf("Weight-Item1  :  ");
    scanf("%d", &w1);
    printf("No of Item1   :  ");
    scanf("%d", &i1);
    printf("Weight-Item2  :  ");
    scanf("%d", &w2);
    printf("No of Item2   :  ");
    scanf("%d", &i2);
    double average = (double)(w1*i1 + w2*i2)/(i1+i2);
    printf("Average value :  %lf ", average);

}
int main(){
    solve();
}


```


## *Output :* 
*Calculating Average*
<p align="center">
<img alt="2310012_lab1_prob_4" src="https://github.com/user-attachments/assets/954d014b-f860-4891-8296-e42ea18a9983">
</p>

## *Discussion :*
<div align="justify">
In this Problem, this program accepts two item's weight and number of purchases
(floating point values) and calculates their average value..
</div>


## *Problem 5 :*
<div align="justify">
  Write a C program that Check if a given number is prime or not.
</div>

## *Code :*
```C
#include<stdio.h>

void solve(){
    int n;
    printf("Enter the number:  ");
    scanf("%d", &n);
    if(n<2){
        printf("NOT Prime\n");
        return;
    }
    for(int i = 2; i*i<=n; i++){
        if(n%i==0){
            printf("NOT Prime\n");
            return;
        }
    }

    printf("Prime\n");
}

int main(){
     solve();
}



```


## *Output :* 
*checking prime or not*
<p align="center">
<img alt="2310012_lab1_prob_5" src="https://github.com/user-attachments/assets/0081e554-4b9d-4954-9b88-e9069c39de92">
</p>

## *Discussion :*
<div align="justify">
In this Problem, this program accepts an integer and check if it is prime or not
</div>
---

## *Problem 6 :*
<div align="justify">
Add the sum of all even numbers (range:1-100)</div>

## *Code :*
```C
#include<stdio.h>

void solve(){
    int n = 100/2;
    // s = n/2{2a+(n-1)d}. Where a is the first number and d is the difference


    int ans = (n/2*(2*2+ (n-1)*2));
    printf("sum of all even numbers (range:1-100) :  %d", ans);
}

int main(){
solve();
}




```


## *Output :* 
*Calculating sum*
<p align="center">
<img alt="2310012_lab1_prob_6" src="https://github.com/user-attachments/assets/4d751d59-6762-42d9-8610-c564ab688c6d">
</p>

## *Discussion :*
<div align="justify">
In this Problem, it calculates the sum of all even number between 1 to 100
</div>
