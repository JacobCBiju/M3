# EX-11-EMI-CALCULATOR

## AIM

To write a program to prepare EMI calculator using function without return type and with arguments.

## ALGORITHM

1.	Start the program.
2.	Read principal amount, rate of interest and months.
3.	Pass these values as arguments to function.
4.	Calculate EMI using the formula, amt=(prpow(1+r,t))/(pow(1+r,t)-1)
5.	Display the result.
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <math.h>


void calculate_emi(double principal, double rate, int months) {
    double emi, amt;

    
    rate = rate / (12 * 100);
    
    
    amt = pow(1 + rate, months);
    emi = (principal * rate * amt) / (amt - 1);

    
    printf("The EMI for the loan is: %.2lf\n", emi);
}

int main() {
    double principal, rate;
    int months;

    
    printf("Enter the principal amount: ");
    scanf("%lf", &principal);

    printf("Enter the annual rate of interest: ");
    scanf("%lf", &rate);

    printf("Enter the number of months: ");
    scanf("%d", &months);

   
    calculate_emi(principal, rate, months);

    return 0;
}
```

## OUTPUT
```
Enter the principal amount: 500000
Enter the annual rate of interest: 7.5
Enter the number of months: 24
The EMI for the loan is: 22411.28
```





## RESULT

Thus the program to prepare EMI calculator using function without return type with arguments has been executed successfully
 
 


# EX-12-FIBONACCI-SERIES
## AIM
To write a C program to generate the Fibonacci series for the value 6.

## ALGORITHM
1.	Start the program.
2.	Read number of terms to display.
3.	Add the previous two terms and store it in new term.
4.	Assign 2nd term to 1st term and 3rd term to 2nd term.
5.	Repeat steps 3 and 4 n number of times.
6.	Display the result.
7.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int n = 6;  
    int t1 = 0, t2 = 1, nextTerm;

    printf("Fibonacci Series for %d terms: \n", n);

    
    printf("%d, %d, ", t1, t2);

    
    for (int i = 3; i <= n; ++i) {
        nextTerm = t1 + t2;
        printf("%d, ", nextTerm);
        
       
        t1 = t2;
        t2 = nextTerm;
    }

    return 0;
}
```

## OUTPUT
```
Fibonacci Series for 6 terms: 
0, 1, 1, 2, 3, 5, 
```








## RESULT
Thus the program to generate the Fibonacci series for the value 6 has been executed successfully.
 
 


# EX-13-ONE-DIMENSIONAL-ARRAY
## AIM
To write a C program to read n elements as input and print the last element of the array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	Print the last element.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int n;

   
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];


    printf("Enter the elements: \n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

   
    printf("The last element of the array is: %d\n", arr[n-1]);

    return 0;
}
```
## OUTPUT
```
Enter the number of elements: 5
Enter the elements:
1 2 3 4 5
The last element of the array is: 5
```









## RESULT
Thus the program to read n elements as input and print the last element of the array has been executed successfully.
 
 


# EX-14-POSITIVE-ARRAY-ELEMENTS
## AIM
To write a C Program to count total number of positive elements in an array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	If the array value can be divided by 2 then increment count by 1.
5.	Display result.
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int n, count = 0;

    
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];

   
    printf("Enter the elements: \n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    
    for (int i = 0; i < n; i++) {
        if (arr[i] > 0) {
            count++;
        }
    }

  
    printf("The total number of positive elements is: %d\n", count);

    return 0;
}
```


## OUTPUT
```
Enter the number of elements: 5
Enter the elements:
-1 2 3 0 -4
The total number of positive elements is: 2
```





## RESULT
Thus the program to count total number of positive elements in an array has been executed successfully.





 
 


# EX -15 - Replace All Even Elements With 'E' In One Dimensional Array

## Aim:
To write a C program to replace all even elements with 'E' in one dimensional array

## Algorithm:
1.	Input the array:
  Read the size of the array.
  Input the elements of the array.
2.	Iterate through the array:
 	For each element of the array, check if the element is even (i.e., if the element modulo 2 equals 0).
3.	Replace even elements with 'E':
     If an element is even, replace that element with the character 'E'.
4.	Output the updated array:
 Print the updated array after replacements.

## Program:
```
#include <stdio.h>

int main() {
    int n;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];

    printf("Enter the elements: \n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    for (int i = 0; i < n; i++) {
        if (arr[i] % 2 == 0) {
            arr[i] = -1;
        }
    }

    printf("Updated array: \n");
    for (int i = 0; i < n; i++) {
        if (arr[i] == -1) {
            printf("E ");
        } else {
            printf("%d ", arr[i]);
        }
    }

    printf("\n");

    return 0;
}
```

## Output:
```
Enter the number of elements: 6
Enter the elements:
1 2 3 4 5 6
Updated array: 
1 E 3 E 5 E
```
 


## Result:

Thus, the program to replace all even elements with 'E' in one dimensional array was verified successfully.



