# C++ Memory Management Error: Deleting a Stack Variable

This repository demonstrates a common C++ memory management error: attempting to delete a variable allocated on the stack using the `delete` operator. This operation leads to undefined behavior and may cause program crashes or other unpredictable outcomes.

## The Bug

The `bug.cpp` file contains the erroneous code. The integer variable `x` is allocated on the stack.  The `delete` operator, however, is used to deallocate memory, which is only appropriate for dynamically allocated memory (using `new`).

## The Solution

The `bugSolution.cpp` file shows the corrected code. It removes the incorrect `delete` statement and the code functions correctly as expected.

## How to Reproduce

1. Clone this repository.
2. Compile `bug.cpp` using a C++ compiler (e.g., g++).  Observe that compilation succeeds. However running the program might cause a crash or unpredictable behavior.
3. Compile `bugSolution.cpp`. This should compile and run without errors.

This example highlights the importance of understanding the difference between stack and heap memory in C++ and using appropriate memory management techniques.