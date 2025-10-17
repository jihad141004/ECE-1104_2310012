## *Lab No : 03*

## *Lab Workout : Pattern Problems in C*

## *Submission Date : 19 Novermber, 2024*

---

## *Problem 1 :*  
<div align="justify">  
Write a program in C to create a Right Half Pyramid.  
</div>  

## *Code :*  
~~~C
#include<stdio.h>

void solve(){
    int n = 5;
    for(int i = 0; i<n ;i++){
        for(int j = 0; j<n; j++){
            if(i+j <= n-1){
                printf("* ");
            }else{
                printf(" ");
            }
        }
        printf("\n");
    }
}

int main(){
    solve( );
}

~~~  

## *Output :*  
*Printing Right Half Pyramid*  
<p align="center">  
<img alt="output_problem_1" src="https://github.com/user-attachments/assets/4f4f0551-2d95-4c22-98a2-57b16f6292c6"/>  
</p>  

---

## *Problem 2 :*  
<div align="justify">  
Write a program in C to create an Inverted Left Half Pyramid.  
</div>  

## *Code :*  
~~~C
#include<stdio.h>
void solve(){
    int n = 5;
    for(int i = 0; i<n ;i++){
        for(int j = 0; j<n; j++){
            if(i <= j){
                printf("* ");
            }else{
                printf("  ");
            }
        }
        printf("\n");
    }
}

int main(){
    solve( );
}

~~~  

## *Output :*  
*Printing Inverted Left Half Pyramid*  
<p align="center">  
<img alt="output_problem_2" src="https://github.com/user-attachments/assets/f98d51a5-f245-486d-b77f-cacec7d18929"/>  
</p>  

---

## *Problem 3 :*  
<div align="justify">  
Write a program in C to create an Inverted Full Pyramid.  
</div>  

## *Code :*  
~~~C
#include<stdio.h>

void solve(){
    int n = 5;
    for(int i = 0; i<n ;i++){
        for(int j = 0; j<n; j++){
            if(i <= j){
                printf("* ");
            }else{
                printf(" ");
            }
        }
        printf("\n");
    }
}

int main(){
    solve( );
}

~~~  

## *Output :*  
*Printing Inverted Full Pyramid*  
<p align="center">  
<img alt="output_problem_3" src="https://github.com/user-attachments/assets/bc3e137d-8dd8-46bf-a588-11b818fc85ae"/>  
</p>  

---

## *Problem 4 :*  
<div align="justify">  
Write a program in C to create a Rhombus Pattern.  
</div>  

## *Code :*  
~~~C
#include<stdio.h>
void solve(){
    int n = 5, m = 4;
    for(int i = 0; i<n ;i++){
        for(int j = 0; j<n+m-1; j++){
            if(i <= j && i-j >= 1-m){
                printf("* ");
            }else{
                printf(" ");
            }
        }
        printf("\n");
    }
}

int main(){
    solve( );
}

~~~  

## *Output :*  
*Printing Rhombus Pattern*  
<p align="center">  
<img alt="output_problem_4" src="https://github.com/user-attachments/assets/aaf567ae-993a-4ada-b5cd-b57917b71f4f"/>  
</p>  

---

## *Problem 5 :*  
<div align="justify">  
Write a program in C to create a Hollow Square.  
</div>  

## *Code :*  
~~~C
#include<stdio.h>
void solve(){
    int n = 6, m = 5;
    for(int i = 0; i<n ;i++){
        for(int j = 0; j<m; j++){
            if(i==0 || i== n-1 || j==0 || j==m-1){
                printf("* ");
            }else{
                printf("  ");
            }
        }
        printf("\n");
    }
}

int main(){
    solve( );
}

~~~  

## *Output :*  
*Printing Hollow Square*  
<p align="center">  
<img alt="output_problem_5" src="https://github.com/user-attachments/assets/37f34672-6c8a-43fe-9ab6-6608b6f337ef"/>  
</p>  

---

## *Problem 6 :*  
<div align="justify">  
Write a program in C to create a Hollow Triangle.  
</div>  

## *Code :*  
~~~C
#include<stdio.h>

void solve() {
    int n = 5;
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < 2 * n - 1; j++) {
            if (i+j == n - 1 || j == n - 1 + i || (i == n - 1 && j % 2 == 0)) {
                printf("*");
            } else {
                printf(" ");
            }
        }
        printf("\n");
    }
}

int main() {
    solve();
    return 0;
}

~~~  

## *Output :*  
*Printing Hollow Triangle*  
<p align="center">  
<img alt="output_problem_6" src="https://github.com/user-attachments/assets/c4b2d5c3-9002-4e38-8f89-f0681c9cbc18"/>  
</p>  

---

## *Problem 7 :*  
<div align="justify">  
Write a program in C to create an **Inverted Hollow Triangle**.  
</div>  

## *Code :*  
~~~C
#include<stdio.h>

void solve() {
    int n = 5;
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < 2 * n - 1; j++) {
            if (j == i || j == 2 * n - 2 - i || (i == 0 && j%2==0)) {
                printf("*");
            } else {
                printf(" ");
            }
        }
        printf("\n");
    }
}

int main() {
    solve();
    return 0;
}

~~~  

## *Output :*  
*Printing Inverted Hollow Triangle*  
<p align="center">  
<img alt="output_problem_7" src="https://github.com/user-attachments/assets/c8943d80-5643-49bb-a7ea-ce9e942b7c46"/>  
</p>  

