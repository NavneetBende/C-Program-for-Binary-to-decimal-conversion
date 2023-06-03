# C-Program-for-Binary-to-decimal-conversion

Binary to decimal conversion in C++
Binary Numbers are used by computers to do almost all operations. We will look at how Binary to decimal conversion in C++ works.

Ex:-  (11011)2 = 1 * 24 + 1 * 23 + 0 * 22 + 1 * 21 + 2 * 20
               = 16 + 8 + 0 + 2 + 1
               = (27)10
Binary to Decimal in C++
Different Methods discussed
We will discuss the following methods in the post –

Algorithmic way (Binary to Decimal)
Inbuilt Method (Binary to Decimal)
Method 1
Binary To Decimal Conversion in C++ new
Algorithm
For user input num

Initialize i = 0, decimal = 0
Extract the last digit (digit = num% 10)
Calculate decimal equivalent of this digit
Add it to decimal variable
decimal += digit * pow(2,i);
Reduce the number (num /= 10
increment i value
C++ Code:-
Run
#include<bits/stdc++.h>
using namespace std;

// function to convert binary to decimal
int getDecimal(long long num)
{
    int i = 0, decimal= 0;
    
    //converting binary to decimal
    while (num!=0)
    {
        int digit = num % 10;
        decimal += digit * pow(2,i);

        num /= 10;
        i++;
    }
    return decimal;
}

// main program
int main()
{
    // long used rather than int to store large values
    // Ex : int wont store 111111111111 (12 digits) as
    // limit for int is 2147483647 (10 digits)
    long long binary = 11011;
    
    cout << getDecimal(binary);   
    
    return 0;
}
Output
27
While loop in C
Method 2
Methods used
The following method uses inbuilt function stoi(), which has given template -

stoi(binary_in_string_format, 0, base_value)
C++ Code:-
Run
#include <iostream>
using namespace std;
 
int main()
{
  string binaryNumber;
    cin >> binaryNumber;
    
    // format stoi(binary_in_string_format, 0, base_value)
    cout << stoi(binaryNumber, 0, 2);
 
    return 0;
}
Output
10110101
181
