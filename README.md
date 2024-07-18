# CGPA Calculator

Welcome to the CGPA Calculator! This is a fun project to calculate the SGPA needed for the next 4 semesters to reach a desired CGPA from the current CGPA.

## Description

This program calculates the SGPA needed for the next 4 semesters based on the current CGPA and the desired CGPA. It includes validation to ensure the CGPA values are within a realistic range and provides humorous responses for certain conditions.

## How to Use

1. **Command Line Program**
    - Clone the repository.
    - Compile the program using a C++ compiler.
    - Run the executable and follow the prompts to enter the current and desired CGPA.

2. **Web Interface**
    - Open the `index.html` file in a web browser.
    - Enter the current and desired CGPA in the provided fields.
    - Click the "Calculate" button to see the required SGPA.

## Example

### Command Line Program

```cpp
#include<iostream>
using namespace std;

int main()
{
    double current_cgpa;
    double desired_cgpa;
    double needed_sgpa;
    
    cout << "Welcome to the CGPA Calculator!" << endl;
    
  
    cout << "Enter your current CGPA: ";
    while (!(cin >> current_cgpa) || current_cgpa < 0 || current_cgpa > 10) {
        cin.clear();
        cin.ignore(numeric_limits<streamsize>::max(), '\n');
        cout << "Invalid input. Please enter a valid CGPA (0-10): ";
    }
    
  
    cout << "Enter your desired CGPA: ";
    while (!(cin >> desired_cgpa) || desired_cgpa < 0 || desired_cgpa > 10) {
        cin.clear();
        cin.ignore(numeric_limits<streamsize>::max(), '\n');
        cout << "Invalid input. Please enter a valid CGPA (0-10): ";
    }
    
    
    needed_sgpa = ((desired_cgpa * 232) - (112 * current_cgpa)) / 120;
    
    // Display results
    if (desired_cgpa > 10) {
        cout << "NOT POSSIBLE! AUKAAT ME REH DALLE\n";
    } else if (desired_cgpa < current_cgpa) {
        cout << "PADHAI CHOD DE!\n";
    } else {
        cout << "SGPA needed for next 4 semesters: " << needed_sgpa << endl;
    }

    cout << "Thank you for using the CGPA Calculator!" << endl;
    
    return 0;
}
