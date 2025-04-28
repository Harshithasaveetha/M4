# EX-16-LEFT-SHIFT-OPERATION
## AIM
To write a C Program to perform the basic left shift operation for 44 integer number with 3 shifts.

## ALGORITHM
1.	Start the program.
2.	Assign values of a and b as 44 and 3.
3.	Use left shift operator (<<) and shift the value of a three times.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int num = 44;    
    int shifts = 3;  

    int result = num << shifts;

    printf("The original number: %d\n", num);
    printf("The result after left shifting %d by %d positions: %d\n", num, shifts, result);

    return 0;
}
```
## OUTPUT

![Screenshot 2025-04-28 190933](https://github.com/user-attachments/assets/9cfef4bf-27f0-49ca-bb58-db74aeda2bf2)








## RESULT
Thus the program to perform the basic left shift operation for 44 integer number with 3 shifts has been executed successfully.




 
 


# EX-17-TWO-NUMBERS-ARE-EQUAL-OR-NOT


## AIM

Write a C Program to check whether the two numbers are equal or not using simple if statement.

## ALGORITHM

1.	Start the program.
2.	Read two numbers.
3.	If first number is equal to second number, display both are equal.
4.	Otherwise display both are not equal.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int num1, num2;

    printf("Enter the first number: ");
    scanf("%d", &num1);

    printf("Enter the second number: ");
    scanf("%d", &num2);
    
    if (num1 == num2) {
        printf("The two numbers are equal.\n");
    } else {
        printf("The two numbers are not equal.\n");
    }

    return 0;
}
```

## OUTPUT
![Screenshot 2025-04-28 191227](https://github.com/user-attachments/assets/3c4dc5a9-96dc-4821-8c6a-654d9fbd94ec)
           
## RESULT

Thus the program to check whether the two numbers are equal or not using simple if statement has been executed successfully
 
 


# EX-18-STRING-LOWERCASE-CONVERSION
## AIM
Write a C Program to convert the given string into lowercase.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using tolower( ) function convert the given string into its lowercase.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <ctype.h>  
int main() {
    char str[100];

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);  
    for (int i = 0; str[i] != '\0'; i++) {
        str[i] = tolower(str[i]);  
    }

    printf("The string in lowercase: %s", str);

    return 0;
}
```
## OUTPUT
![Screenshot 2025-04-28 191449](https://github.com/user-attachments/assets/22e942bb-a410-4572-a36c-02083c8a4e9d)




## RESULT
Thus the program to convert the given string into lowercase has been executed successfully
 
 


# EX-19-COUNT-OF-WORDS-IN-A-STRING
## AIM
Write a C Program to count the total number of words in a given string using do While loop.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using for loop, inspect the string character by character.
4.	Whenever a space is encountered increment count by 1.
5.	Display the result.
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <ctype.h>  
int main() {
    char str[100];
    int count = 0, i = 0;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    do {
        
        while (str[i] == ' ' || str[i] == '\t' || str[i] == '\n') {
            i++;
        }

        if (str[i] != '\0') {
            count++;  
            while (str[i] != ' ' && str[i] != '\0' && str[i] != '\t' && str[i] != '\n') {
                i++;
            }
        }
    } while (str[i] != '\0');  

    printf("Total number of words: %d\n", count);

    return 0;
}
```
## OUTPUT

![Screenshot 2025-04-28 191749](https://github.com/user-attachments/assets/58c953cc-dc98-460d-a22b-8c58be982c9f)




## RESULT
Thus the program to count the total number of words in a given string using do While loop has been executed successfully
 
 


# EX  -20 -COMPARING TWO STRINGS
## AIM
write a Program to compare two strings without using strcmp().
## ALGORITHM
Step 1: Start the program.
Step 2: Declare two character arrays c1 and c2 of size 100 to store the strings. Also, declare an integer variable
             flag and initialize it to 0, and i for indexing.      
Step 3: Read the first string c1 using scanf("%[^\n]", c1); — this reads input until a newline is encountered 
            (i.e., can include spaces).
Step 4: Read the second string c2 using scanf("%s", c2); — this reads input until a space or newline (i.e., no 
            spaces in the second string).
Step 5: Start comparing characters of both strings from index i = 0.
Step 6: Repeat the following while neither c1[i] nor c2[i] is '\0' (i.e., end of string):
•	If c1[i] is not equal to c2[i], set flag = 1.
•	Increment i by 1.
Step 7: After the loop, check the value of flag:
•	If flag == 0, print "strings are same".
•	Otherwise, print "strings are not same".
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

int compareStrings(const char *str1, const char *str2) {
   
    int i = 0;
    while (str1[i] != '\0' && str2[i] != '\0') {
        if (str1[i] > str2[i]) {
            return 1;
        } else if (str1[i] < str2[i]) {
            return -1;
        }
        i++;
    }

    if (str1[i] == '\0' && str2[i] == '\0') {
        return 0;
    } else if (str1[i] == '\0') {
        return -1;
    } else {
        return 1;
    }
}

int main() {
    char string1[100], string2[100];

    printf("Enter the first string: ");
    scanf("%99s", string1); 
    printf("Enter the second string: ");
    scanf("%99s", string2); 
    int result = compareStrings(string1, string2);

    if (result == 0) {
        printf("The strings are equal.\n");
    } else if (result > 0) {
        printf("'%s' is lexicographically greater than '%s'.\n", string1, string2);
    } else {
        printf("'%s' is lexicographically smaller than '%s'.\n", string1, string2);
    }

    return 0;
}
```

## OUTPUT
 ![Screenshot 2025-04-28 192413](https://github.com/user-attachments/assets/d35efe77-444e-4890-9ff6-f1b7ef195d68)


## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.

