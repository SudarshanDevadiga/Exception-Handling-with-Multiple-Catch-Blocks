# Exception Handling with Multiple Catch Blocks

A C++ program demonstrating exception handling using multiple catch blocks to handle different types of exceptions.

## Description

This program illustrates how to use try-catch blocks in C++ to handle exceptions of different types. It throws an integer or a character based on the input value and catches them using separate catch blocks.

### Key Features
- Exception handling with try-catch
- Multiple catch blocks for different types
- Conditional exception throwing
- Simple error handling demonstration

## Code Structure

```cpp
#include <iostream>
using namespace std;

void test(int x) {
    try {
        if (x > 0)
            throw x;
        else
            throw 'x';
    } catch(int x) {
        cout << "Caught an integer and that integer is:\n" << x << endl;
    } catch (char x) {
        cout << "Caught a character and that character is:\n" << x << endl;
    }
}

int main() {
    cout << "Testing multiple catches:\n";
    test(10);
    test(0);
    return 0;
}
