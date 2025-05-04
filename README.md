# 📌 SquareMat – C++ Matrix Class Implementation

## 👨‍💻 Project Overview
This project implements a `SquareMat` class in C++ that represents square matrices of integers. The class supports dynamic memory allocation, copy semantics, operator overloading, and matrix operations such as addition, subtraction, multiplication, transposition, and more. The project strictly follows object-oriented design without using `std::vector`, `using namespace std`, or any STL container.

## 🧩 File Structure
- `SquareMat.hpp` – Header file defining the `SquareMat` class interface.
- `SquareMat.cpp` – Implementation of the class methods and overloaded operators.
- `main.cpp` – Demonstrates how to use the class through various operations.
- `tests.cpp` – Contains comprehensive tests using the [doctest](https://github.com/doctest/doctest) framework.
- `Makefile` – Builds both `main` and `tests` executables and supports `valgrind`.
- `doctest.h` – Header-only testing framework for unit testing.

## ⚙️ Features
- ✅ Constructor, Destructor, Copy Constructor, and Assignment Operator.
- ✅ Matrix element access via `get`, `set`, and `operator()(i, j)`.
- ✅ Matrix addition (`+`, `+=`), subtraction (`-`, `-=`), and multiplication (`*`, `*=`).
- ✅ Comparison operators: `==`, `!=`.
- ✅ Increment/Decrement: prefix/postfix `++`, `--`.
- ✅ Negation operator: `-matrix`.
- ✅ Transposition and identity matrix generation.
- ✅ Stream I/O operators (`<<`, `>>`).
- ✅ Full bounds checking with exception throwing.
- ✅ Memory-leak free (validated using Valgrind).

## 🛠️ Build & Run

To compile the main program:
```bash
make main
./main
```

To run the unit tests:
```bash
make test
./tests
```

To check for memory leaks:
```bash
make valgrind
```

## 📊 Sample Output

From `main.cpp`:
```
Matrix A:
0 1 2 
1 2 3 
2 3 4 
...
Identity matrix:
1 0 0 
0 1 0 
0 0 1 
```

From `tests.cpp`:
```
[doctest] test cases: 14 | 14 passed | 0 failed
[doctest] assertions: 55 | 55 passed | 0 failed
```

## 🧪 Memory Check (Valgrind)
```
== HEAP SUMMARY:
== in use at exit: 0 bytes in 0 blocks
== total heap usage: 64 allocs, 64 frees, 115,139 bytes allocated
== All heap blocks were freed -- no leaks are possible
```

## 📎 Notes
- The code avoids STL usage to meet assignment requirements.
- Comprehensive unit testing was applied including edge cases.
- Fully compliant with C++17 and runs cleanly under `-Wall -Wextra`.