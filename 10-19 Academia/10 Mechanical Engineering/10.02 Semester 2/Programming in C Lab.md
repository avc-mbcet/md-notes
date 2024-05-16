---
date: 2024-05-03
title: Programming in C Lab
tags:
  - Academia
---
1. Familiarisation of console I/O and operations in C.

1. Display "Hello World".
```c
#include <stdio.h>
int main() {
  printf("Hello World\n");
  return 0;
}
```

2. Read two numbers, add them and display their sum.
```c
#include <stdio.h>
int main() {
  int a, b, sum;
  printf("Input two numbers\n");
  scanf("%d %d", &a, &b);
  sum = a + b;
  printf("Sum of %d and %d is %d\n", a, b, sum);
  return 0;
}
```

3. Read the radius of  a circle, calculate its area and display it
```c
#include <stdio.h>
int main() {
  int radius;
  float area;
  printf("Input radius of the circle\n");
  scanf("%d", &radius);
  area = 3.14 * radius * radius;
  printf("Area of the circle with radius %d is %f\n", radius, area);
  return 0;
}
```

4. Area of triangle after reading its sides.
```c
#include <stdio.h>

int main() {
  int height, base;
  float area;
  printf("Enter the length of base and height respectively");
  scanf("%d %d", &base, &height);
  area = base * height * 0.5;
  printf("Area of the triangle with base %d and height %d is %f\n", base,
         height, area);
  return 0;
}
```

2. Read three integer values and find largest of three numbers.
```c
#include <stdio.h>

int main() {
  int a, b, c;
  printf("Enter three numbers\n");
  scanf("%d %d %d", &a, &b, &c);
  if (a > b) {
    if (a > c) {
      printf("The largest number is %d\n", a);
    } else {
      printf("The largest number is %d\n", c);
    }
  } else {
    if (b > c) {
      printf("The largest number is %d\n", b);
    } else {
      printf("The largest number is %d\n", c);
    }
  }
}
```

3. Check whether given year is leap year.
```c
#include <stdio.h>

int main() {
  int year;
  printf("Enter year\n");
  scanf("%d", &year);
  if (year % 4 == 0 && year % 100 != 0 || year % 400 == 0) {
    printf("%d is a leap year\n", year);
  } else {
    printf("%d is not a leap year\n", year);
  }
  return 0;
}
```

4. Display the grade of a student after reading his mark for a subject.
```c
#include <stdio.h>

int main() {
  int grade;
  printf("Enter Grade\n");
  scanf("%d", &grade);
  switch (grade / 10) {
  case 10:
  case 9:
    printf("Grade A+");
    break;
  case 8:
    printf("Grade A");
    break;
  case 7:
    printf("Grade B");
    break;
  case 6:
    printf("Grade C");
    break;
  case 5:
    printf("Grade D");
    break;
  case 4:
  case 3:
  case 2:
  case 1:
  case 0:
    printf("Grade F");
    break;
  default:
    printf("Something went wrong");
    break;
  }
  return 0;
}
```

5. Read a natural number and check whether the number is prime or not.
```c
#include <stdio.h>

int main() {
  int N, i = 2, flag = 1;
  printf("Enter natural number\n");
  scanf("%d", &N);
  while (i < (N / 2)) {
    if (N % i == 0) {
      flag = 0;
      break;
    } else {
      i = i + 1;
    }
  }
  if (flag == 1) {
    printf("Prime Number");
  } else {
    printf("Composite Number");
  }
  return 0;
}
```

6. Read a Natural number and check whether the number is Armstrong or not.
```c
#include <math.h>
#include <stdio.h>

int main() {
  int a, s = 0, b, c = 0;
  printf("Enter Number\n");
  scanf("%d", &a);
  b = a;
  while (a > 0) {
    a = a / 10;
    c = c + 1;
  }
  a = b;
  while (a > 0) {
    s = s + pow((a % 10), c);
    a = a / 10;
  }
  if (b == s) {
    printf("armstrong number\n");
  } else {
    printf("not armstrong number\n");
  }
}
```

7. Display second largest number after reading n numbers from user.
```c
#include <stdio.h>

int main() {
  int first = 0, second = 0, input;
  while (1) {
    printf("Input number\n");
    scanf("%d", &input);
    if (input > first) {
      second = first;
      first = input;
    } else if (input > second) {
      second = input;
    }
    printf("Do you want to input more numbers? 1 or 0\n");
    scanf("%d", &input);
    if (input == 1) {
      continue;
    } else {
      printf("Second largest number is %d\n", second);
      break;
      return 0;
    }
  }
}
```

8. Read n integers, store them in an array and find their sum and average.
```c
#include <stdio.h>
int main() {
  int n;
  printf("Enter the size of array\n");
  scanf("%d", &n);
  int array[n], i;
  float sum = 0, average;
  printf("Enter n values\n");
  for (i = 0; i < n; i++) {
    scanf("%d", &array[i]);
  }
  for (i = 0; i < n; i++) {
    sum = sum + array[i];
  }
  printf("Sum is %f\n", sum);
  average = sum / n;
  printf("Average is %f\n", average);
  return 0;
}
```

9. Read n integers, store them in an array and search for an element in the array using an algorithm for Linear Search.
 ```c
#include <stdio.h>

int main() {
  int n;
  printf("Enter the size of array\n");
  scanf("%d", &n);
  int array[n], i, searchterm, flag = 0;
  printf("Enter n values\n");
  for (i = 0; i < n; i++) {
    scanf("%d", &array[i]);
  }
  printf("Enter search term\n");
  scanf("%d", &searchterm);
  for (i = 0; i < n; i++) {
    if (array[i] == searchterm) {
      flag = 1;
      break;
    }
  }
  if (flag == 1) {
    printf("The search term is at index %d\n", i);
  } else {
    printf("The search term is not in the array\n");
  }
}
```

10.Read n integers, store them in an array and sort the elements in the array using Bubble Sort algorithm.
```c
#include <stdio.h>

int main() {
  int size;
  printf("Enter size of the array\n");
  scanf("%d", &size);
  int array[size], i, j, temp;
  printf("Enter values of array\n");
  for (i = 0; i < size; i++) {
    scanf("%d", &array[i]);
  }
  for (i = 0; i < size; i++) {
    for (j = 0; j < size; j++) {
      if (array[i] < array[j]) {
        temp = array[i];
        array[i] = array[j];
        array[j] = temp;
      } else {
        continue;
      }
    }
  }
  for (i = 0; i < size; i++) {
    printf("%d ", array[i]);
  }
  return 0;
}
```

11. Write a program for performing matrix addition, multiplication and finding the transpose.
```c
#include <stdio.h>

int main() {
  int operation, i, j;
  printf(
      "Enter operation type.\n1. Addition\n2. Multiplication\n3. Transpose\n");
  scanf("%d", &operation);
  switch (operation) {
  case 1: {
    int ax, ay;
    printf("Enter size of Matrix A and B\n");
    scanf("%d %d", &ax, &ay);
    int matrixa[ax][ay], matrixb[ax][ay];
    printf("Enter values for Matrix A\n");
    for (i = 0; i < ax; i++) {
      for (j = 0; j < ay; j++) {
        printf("A[%d,%d]: ", i, j);
        scanf("%d", &matrixa[i][j]);
      }
      printf("\n");
    }
    printf("Enter values for Matrix B\n");
    for (i = 0; i < ax; i++) {
      for (j = 0; j < ay; j++) {
        printf("B[%d,%d]: ", i, j);
        scanf("%d", &matrixb[i][j]);
      }
      printf("\n");
    }
    printf("Sum of Matrix A and Matrix B\n");
    for (i = 0; i < ax; i++) {
      for (j = 0; j < ay; j++) {
        printf("%d\t", matrixa[i][j] + matrixb[i][j]);
      }
      printf("\n");
    }

  } break;
  case 2: {
    int ax, ay, bx, by, sum, m;
    printf("Enter size of Matrix A(rows columns)\n");
    scanf("%d %d", &ax, &ay);
    printf("Enter size of Matrix B(rows columns)\n");
    scanf("%d %d", &bx, &by);
    int matrixb[bx][by], matrixa[ax][ay];
    if (ax != by) {
      printf("Error! Operation not Supported\n");
      break;
    }
    printf("Enter values for Matrix A\n");
    for (i = 0; i < ax; i++) {
      for (j = 0; j < ay; j++) {
        printf("A[%d,%d]: ", i, j);
        scanf("%d", &matrixa[i][j]);
      }
      printf("\n");
    }
    printf("Enter values for Matrix B\n");
    for (i = 0; i < bx; i++) {
      for (j = 0; j < by; j++) {
        printf("B[%d,%d]: ", i, j);
        scanf("%d", &matrixb[i][j]);
      }
      printf("\n");
    }

    int matrixab[ax][by];
    for (i = 0; i < ax; i++) {
      for (m = 0; m < by; m++) {
        for (j = 0; j < ay; j++) {
          sum = sum + (matrixa[i][j] * matrixb[j][m]);
        }
        printf("%d\t", sum);
        sum = 0;
      }
      printf("\n");
    }
  } break;
  case 3: {
    int ax, ay;
    printf("Enter size of Matrix A(rows columns)\n");
    scanf("%d %d", &ax, &ay);
    int matrixa[ax][ay];
    printf("Enter values for Matrix A\n");
    for (i = 0; i < ax; i++) {
      for (j = 0; j < ay; j++) {
        printf("A[%d,%d]: ", i, j);
        scanf("%d", &matrixa[i][j]);
      }
      printf("\n");
    }
    printf("Transpose of Matrix A\n");
    for (i = 0; i < ax; i++) {
      for (j = 0; j < ay; j++) {
        printf("%d\t", matrixa[j][i]);
      }
      printf("\n");
    }
  } break;
  default:
    printf("Operation not supported");
    break;
  }
  return 0;
}
```

12. Display the sum of diagonal elements of a matrix.
```c
#include <stdio.h>
int main() {
  int sum, m, n, i, j;
  printf("Enter the order of matrix A\n");
  scanf("%d %d", &m, &n);
  int A[m][n];
  for (i = 0; i < m; i++) {
    for (j = 0; j < n; j++) {
      printf("A[%d,%d]: ", i, j);
      scanf("%d", &A[i][j]);
    }
    printf("\n");
  }
  for (i = 0; i < m; i++) {
    sum = sum + A[i][i];
  }
  printf("Sum=%d", sum);
  return 0;
}
```

13. Read a string(word), store it in array and check whether it is a palindrome word or not
```c
#include <string.h>
int main() {
  char str[20];
  printf("Enter the string: ");
  scanf("%[^\n]", str);
  int i, len = strlen(str), flag = 0;
  for (i = 0; i < len / 2; i++) {
    if (str[i] != str[len - i - 1]) {
      flag = 1;
      break;
    }
  }
  if (flag == 1) {
    printf("Not Palindrone");
  } else {
    printf("Palindrome");
  }
}
```

14. Read a string (ending with $ symbol), store it in an array and count the number of vowels, consonants and spaces in it.
```c
#include <stdio.h>
#include <string.h>

int main() {
  char str[20];
  scanf("%[^\n]", str);
  int i, vowels = 0, consonants = 0, spaces = 0;
  for (i = 0; i < strlen(str); i++) {
    switch (str[i]) {
    case 'A':
    case 'E':
    case 'I':
    case 'O':
    case 'U':
    case 'a':
    case 'e':
    case 'i':
    case 'o':
    case 'u': {
      vowels++;
      break;
    }
    case ' ': {
      spaces++;
      break;
    }
    default: {
      consonants++;
      break;
    }
    }
  }
  printf("Consonants: %d\nVowels: %d\n Spaces: %d", consonants, vowels, spaces);
}
```

15. 