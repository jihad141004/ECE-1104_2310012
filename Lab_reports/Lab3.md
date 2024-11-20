## *Lab No : 03*

## *Lab Workout : Pattern Problems in C*

## *Submission Date : 20 Novermber 2024*

---

## *Problem 1 :*  
<div align="justify">  
Write a program in C to create a Right Half Pyramid.  
</div>  

## *Code :*  
~~~
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
<img alt="output_problem_1" src=""/>  
</p>  

---

## *Problem 2 :*  
<div align="justify">  
Write a program in C to create an Inverted Left Half Pyramid.  
</div>  

## *Code :*  
~~~
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
<img alt="output_problem_2" src=""/>  
</p>  

---

## *Problem 3 :*  
<div align="justify">  
Write a program in C to create an Inverted Full Pyramid.  
</div>  

## *Code :*  
~~~
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
<img alt="output_problem_3" src=""/>  
</p>  

---

## *Problem 4 :*  
<div align="justify">  
Write a program in C to create a Rhombus Pattern.  
</div>  

## *Code :*  
~~~
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
<img alt="output_problem_4" src=""/>  
</p>  

---

## *Problem 5 :*  
<div align="justify">  
Write a program in C to create a Hollow Square.  
</div>  

## *Code :*  
~~~
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
<img alt="output_problem_5" src=""/>  
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
<img alt="output_problem_6" src=""/>  
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
<img alt="output_problem_7" src=""/>  
</p>  

