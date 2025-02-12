# Input and Validation Library

## Overview

This project provides an **Input and Validation Library** built using **Object-Oriented Programming (OOP)** in C++. The library offers robust input handling and validation functions for various data types, ensuring user inputs are correctly formatted and within defined constraints.

## Features

- **Modular OOP Design**: Well-structured classes for input handling and validation.
- **Number Validation**: Check if a number is within a specific range.
- **Date Validation**: Validate date formats and check if a date falls within a given range.
- **User Input Handling**: Read and validate integers and double numbers with error handling.
- **Reusability**: Easily integrates into other C++ projects.

## Installation

1. Clone or download the repository.
2. Include the header file `clsInputValidate.h` in your project.
3. Ensure you have the necessary dependencies (such as `clsDate.h` if date validation is used).

## Usage

### Example Code:

```cpp
#include <iostream>
#include "clsInputValidate.h"

int main()
{
    // Check if a number is within a range
    std::cout << clsInputValidate::IsNumberBetween(5, 1, 10) << std::endl;
    std::cout << clsInputValidate::IsNumberBetween(5.5, 1.3, 10.8) << std::endl;

    // Date validation
    std::cout << clsInputValidate::IsDateBetween(clsDate(), clsDate(8, 12, 2022), clsDate(31, 12, 2022)) << std::endl;
    std::cout << clsInputValidate::IsDateBetween(clsDate(), clsDate(31, 12, 2022), clsDate(8, 12, 2022)) << std::endl;

    // Read an integer from user input
    std::cout << "\nPlease Enter a Number:\n";
    int x = clsInputValidate::ReadIntNumber("Invalid Number, Enter again:\n");
    std::cout << "x=" << x;

    // Read an integer within a specified range
    std::cout << "\nPlease Enter a Number between 1 and 5:\n";
    int y = clsInputValidate::ReadIntNumberBetween(1, 5, "Number is not within range, enter again:\n");
    std::cout << "y=" << y;

    // Read a double number from user input
    std::cout << "\nPlease Enter a Double Number:\n";
    double a = clsInputValidate::ReadDblNumber("Invalid Number, Enter again:\n");
    std::cout << "a=" << a;

    // Read a double number within a specified range
    std::cout << "\nPlease Enter a Double Number between 1 and 5:\n";
    double b = clsInputValidate::ReadDblNumberBetween(1, 5, "Number is not within range, enter again:\n");
    std::cout << "b=" << b;

    // Validate a date
    std::cout << std::endl << clsInputValidate::IsValideDate(clsDate(35, 12, 2022)) << std::endl;

    system("pause>0");
    return 0;
}

