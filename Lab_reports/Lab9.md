## *Lab No : 09*

## *Lab Workout : Programming Exercises*

## *Submission Date : 21 January, 2025*

---

## *Problem 1 :*
<div align="justify"> Write a program in C to find the length of a string without using library functions. </div>

## *Code :*
~~~C
#include <stdio.h>
void solve()
{
    char str[40];
    printf("Enter the String:   ");
    scanf("%[^\n]", str);
    int i = 0;
    while (str[i] != '\0')
    {
        i++;
    }
    printf("Length: %d", i);
}
int main()
{
    solve();
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/b95438d8-f4c0-4ee9-8feb-ba4ebedb22ca">
</p>

## *Discussion :*
<div align="justify"> This program calculates the length of a given string by iterating through its characters until the null terminator is reached, without relying on any standard library functions like `strlen`. </div>

---

## *Problem 2 :*
<div align="justify"> Write a program in C to separate individual characters from a string. </div>

## *Code :*
~~~C
#include <stdio.h>
#include <string.h>
void solve()
{
    char str[40];
    printf("Input the string : ");
    scanf("%[^\n]", str);
    for (int i = 0; str[i] != '\0'; i++)
    {
        printf("%c ", str[i]);
    }
}
int main()
{
    solve();
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 2 output image" src="https://github.com/user-attachments/assets/6f6c5dcb-47cb-472d-99ed-e03a88219bcc">
</p>

## *Discussion :*
<div align="justify"> This program separates each character of the string and displays them individually. </div>

---

## *Problem 3 :*
<div align="justify"> Write a program in C to print individual characters of a string in reverse order. </div>

## *Code :*
~~~C
#include <stdio.h>
#include <string.h>
void solve()
{
    char str[40];
    printf("Input the string : ");
    scanf("%[^\n]", str);
    int i = 0;
    while (str[i] != '\0')
    {
        i++;
    }
    i--;
    for (i; i >= 0; i--)
    {
        printf("%c ", str[i]);
    }
}
int main()
{
    solve();
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 3 output image" src="https://github.com/user-attachments/assets/5c974c54-f5fd-4d1c-b82d-1fb353c8b1b9">
</p>

## *Discussion :*
<div align="justify"> This program prints the characters of the string in reverse order, starting from the last character to the first. </div>

---

## *Problem 4 :*
<div align="justify"> Write a program in C to count the total number of words in a string. </div>

## *Code :*
~~~C
#include <stdio.h>
#include <string.h>
void solve()
{
    char str[40];
    printf("Input the string : ");
    scanf("%[^\n]", str);
    int count = 0;
    for (int i = 0; str[i] != '\0'; i++)
    {
        if (str[i] == ' ')
        {
            count++;
        }
    }
    count++;

    printf("Number of words:  %d ", count);
}
int main()
{
    solve();
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 4 output image" src="https://github.com/user-attachments/assets/16a3a75e-dc12-4041-a97d-f572639bba19">
</p>

## *Discussion :*
<div align="justify"> This program counts the number of words in a string by identifying spaces between words. </div>

---

## *Problem 5 :*
<div align="justify"> Write a program in C to compare two strings without using string library functions. </div>

## *Code :*
~~~C
#include <stdio.h>
#include <string.h>

void solve()
{
    char str1[40], str2[40];
    printf("Input the 1st string:  ");
    scanf("%[^\n]", str1);
    getchar();
    printf("Input the 2nd string:  ");
    scanf("%[^\n]", str2);

    for (int i = 0; str1[i] != '\0'; i++)
    {
        if (str1[i] != str2[i])
        {
            printf("Strings are not equal\n");
            return;
        }
    }
    printf("Strings are equal\n");
}

int main()
{
    solve();
    return 0;
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 5 output image" src="https://github.com/user-attachments/assets/ebe6d102-2853-4c4a-ae15-876d2e9e58aa">
</p>

## *Discussion :*
<div align="justify"> This program compares two strings character by character and checks if they are equal or not. </div>

---

## *Problem 6 :*
<div align="justify"> Write a program in C to count the total number of alphabets, digits and special characters in a string. </div>

## *Code :*
~~~C
#include <stdio.h>
#include <string.h>
void solve()
{
    char str[40];
    printf("Input the string:  ");
    scanf("%[^\n]", str);
    int digit = 0, alpha = 0, special = 1;
    for (int i = 0; str[i] != '\0'; i++)
    {
        if (str[i] >= '0' && str[i] <= '9')
        {
            digit++;
        }
        else if (str[i] >= 'a' && str[i] <= 'z')
        {
            alpha++;
        }
        else if (str[i] >= 'A' && str[i] <= 'Z')
        {
            alpha++;
        }
        else
        {
            special++;
        }
    }

    printf("Number of alphabets :  %d\nNumber of digits: %d \nNumber of speical char:%d", alpha, digit, special);
}
int main()
{
    solve();
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 6 output image" src="https://github.com/user-attachments/assets/4a1c6cc6-243e-4266-9e3a-1d715609448a">
</p>

## *Discussion :*
<div align="justify"> This program counts and displays the number of alphabets, digits, and special characters in the input string. </div>
