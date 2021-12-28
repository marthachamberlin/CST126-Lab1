# CST126-Lab1
Oregon Institute of Technology
CST 126 Solving Complex Problems
Lab #1: Files & Pointers


CST126
Module 1: Lab 1


Playing with Pointers
Use the following code to implement the exercises in this section. 
Write a program that includes all of the following statements. 
Label each part in your output.


int numbers[5] = { 99,34,1,88,100 };
int* int_ptr = numbers;
int** int_ptr_ptr = &int_ptr;


1. Write the statement that prints the address of the array using the array name.
2. Write the statement that prints the address of the array using int_ptr.
3. Write the statement that prints the address of the array using int_ptr_ptr.
4. Write the statement that prints the address of int_ptr using int_ptr.
5. Write the statement that prints the address of int_ptr using int_ptr_ptr.
6. Write the statement that prints the first element of the array using int_ptr.
7. Write the statement that prints the first element of the array using int_ptr_ptr.
8. Write the statement that changes int_ptr to point to the second element of the array.
9. Write the statement that prints the second element of the array using int_ptr.
10. Write the statement that prints the second element of the array using int_ptr_ptr.
11. Write the statement that changes the second element of the array to 101 using int_ptr.
12. Write the statement that changes the second element of the array to 102 using int_ptr_ptr.
13. Write the statement that changes int_ptr to point to the third element of the array using int_ptr_ptr.
14. Write the statement that changes the third element of the array to -1 using int_ptr.
15. Write the statement that changes the third element of the array to -1 using int_ptr_ptr.
16. Print the content of the array to the screen to verify the contents of the array were changed.


Submit: code & runs
10 pts




________________


References to Pointers
Rewrite the following program so that only passing by value and passing by pointer is used.


#include <iostream>
#include <cmath>
using std::cout;
using std::endl;
 
int Fun1 ( int a, int b );
void Fun2 ( int & a, int b );
void Fun3( int & c, int & d );
void PrintOutput( int a, int b);
 
int main ( )
{ // Call the functions
    int a = 2, b = 5;
 
    PrintOutput ( a, b );
    a = Fun1 ( a, b );
    cout << a << "\t" << b 
         << endl;
    Fun2 ( a, b );
    PrintOutput ( a, b );


    return 0;
}


void PrintOutput ( int a, int b )
{ // Print 2 integers
    cout << a << "\t" << b 
         << endl;
}


int Fun1 ( int a, int b )
{ // Do some arithmetic & print it out
    int c;
 
    c = a + b;
    a++;
    --b;
    cout << a << "\t" << b 
         << "\t" << c << endl;
    return c;
}




________________


void Fun2 ( int & a, int b )
{ // Math & function calls
    double temp = 0.0;
 
    a += 5;
    temp = pow(static_cast<double>(a), 2);
    b = static_cast<int>(temp);
    PrintOutput ( a, b );
    Fun3 ( a, b );
    PrintOutput ( a, b );
}


void Fun3 ( int & c, int & d )
{ // Simple assignments
    c = 25;
    d = 10;
 
    PrintOutput ( c, d );
}


Submit: code & runs
10 pts 


Arrays and Pointers
Write a program that declares a two-dimensional array of integers with four rows and five columns.
Initialize the array to any numbers of your choosing. 
Using a pointer, display the contents of the array.


Submit: full development process
10 pts


Pointers and Strings
Write a program including a function that takes two parameters:
* A pointer to a string
* A char
Returns:
* The number of instances of the character found in the string.


Submit: full development process
10 pts


Total: 40 pts
