# Occurrence-of-a-digit-in-a-given-number-using-CPP

Occurrence of a digit in a given number using C++
Here, in this page we will discuss the program that count the occurrence of a digit in a given number using C++.
The input may lie within the range of integer.
Method Discussed
Method 1 : Iterative way
Method 2 : Recursive way.
Let’s discuss the working and algorithm of both methods in brief.

Method 1
Declare variable count that will count the required number of occurrences
Take a while loop.
Declare a variable rem to store every digit of the number to be compared.
Compare rem with the digit
if rem equals digit increment count.
n=n/10
Print the value of count.
Method 1 : Code in C++
Run
//Write a program to print the Occurrence of a Digit in a given Number in C++
#include <iostream>
using namespace std;
int main() {

    int n = 890190798; 
    int d = 9; 

    int count=0; 

    while(n) {

        int rem = n%10; 
        if(rem == d){
            count++;
        }
        n=n/10; 
    }

    cout<<count;

    return 0;

}
Output:
3
Related Pages
Convert digit/number to words

Counting number of days in a given month of a year
 
Finding number of integers which has exactly x divisors

Finding Roots of a quadratic equation

Power of a Number 

Method 2 :
In this method we will implement the recursive code for the algorithm discuss in method 1.

Method 2 : Code in C++
Run
//Write a program to print the Occurrence of a Digit in a given Number in C++
#include <iostream>
using namespace std;

int count(int n, int d){
    if(n<=0)
    return 0;
    
    int rem = n%10;
    
    if(rem == d){
        return 1 + count(n/10, d);
    }
    
    return count(n/10, d);
}
int main() {

    int n = 890190798; 
    int d = 9; 
    
    int x = count(n, d);
    cout<<x;

    return 0;

}

Output:
3
