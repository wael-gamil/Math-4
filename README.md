# Math 4 Solver

A comprehensive C++ console application implementing advanced numerical methods for solving non-linear algebraic equations, performing numerical differentiation and integration, curve fitting, and polynomial interpolation with step-by-step solution output.

## 📋 Table of Contents

- [Features](#features)
- [Supported Operations](#supported-operations)
- [Mathematical Functions](#mathematical-functions)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Project Structure](#project-structure)
- [Technologies](#technologies)
- [License](#license)

## ✨ Features

- **Root Finding Algorithms**

  - Bisection Method with automatic interval detection
  - Newton-Raphson Method with symbolic differentiation
  - Newton-Jacobian Method for systems of equations

- **Numerical Integration**

  - Trapezoidal Rule with error estimation
  - Simpson's Rule with error estimation

- **Numerical Differentiation**

  - Forward, Backward, and Central difference formulas
  - First and second derivative approximations

- **Curve Fitting**

  - Linear regression (y = ax + b)
  - Parabolic fitting (y = ax² + bx + c)
  - Exponential fitting (y = ae^bx)
  - Power law fitting (y = ax^b)

- **Polynomial Interpolation**

  - Lagrange's method (up to 1,000 data points)
  - Newton's Divided Difference method (up to 100 data points)

- **Expression Parser**

  - Custom infix-to-postfix conversion
  - Supports 13 mathematical functions
  - Handles multi-digit numbers and variables

- **Step-by-Step Solutions**
  - Optional detailed iteration tables
  - Formatted output with configurable precision

## 🔢 Supported Operations

### 1. Non-linear Algebraic Equations

- Bisection method
- Newton's method
- Newton-Jacobian method (for systems of 2 equations)

### 2. Interpolating Polynomials

- Lagrange polynomial method
- Divided difference method

### 3. Least Squares and Curve Fitting

- Straight line (y = ax + b)
- Parabola (y = ax² + bx + c)
- Exponential (y = ae^bx)
- Power curve (y = ax^b)

### 4. Numerical Differentiation

- Forward difference formula (1st & 2nd derivative)
- Backward difference formula (1st & 2nd derivative)
- Central difference formula (1st & 2nd derivative)

### 5. Numerical Integration

- Trapezoidal rule
- Simpson's rule

## 📐 Mathematical Functions

The expression parser supports the following functions:

| Function    | Syntax           | Example                     |
| ----------- | ---------------- | --------------------------- |
| Sine        | `sin(x)`         | `sin(x)`                    |
| Cosine      | `cos(x)`         | `cos(x)`                    |
| Tangent     | `tan(x)`         | `tan(x)`                    |
| Secant      | `sec(x)`         | `sec(x)`                    |
| Cosecant    | `csc(x)`         | `csc(x)`                    |
| Cotangent   | `cot(x)`         | `cot(x)`                    |
| Arc Sine    | `arcsin(x)`      | `arcsin(x)`                 |
| Arc Cosine  | `arccos(x)`      | `arccos(x)`                 |
| Arc Tangent | `arctan(x)`      | `arctan(x)`                 |
| Natural Log | `ln(x)` or `lnx` | `ln(x)`                     |
| Logarithm   | `log(x)`         | `2log(x)` for log base 2    |
| Exponential | `exp(x)`         | `exp(x)`                    |
| Nth Root    | `root(x, n)`     | `2root3` for cube root of 2 |

**Arithmetic Operators:** `+`, `-`, `*`, `/`, `^` (power)

## 🚀 Installation

### Prerequisites

- C++ compiler (GCC, Clang, or MSVC)
- C++11 or later
- Standard C++ libraries (no external dependencies)

### Compilation

#### Windows (Visual Studio)

```bash
# Open Math 4 Project.sln in Visual Studio
# Build -> Build Solution (or press F7)
# Run -> Start Without Debugging (or press Ctrl+F5)
```

#### Linux/macOS (GCC/Clang)

```bash
g++ -std=c++11 "Math 4 Project/Math 4 Project.cpp" -o math4solver -lm
./math4solver
```

## 💻 Usage

### Running the Application

1. Compile the source code
2. Run the executable
3. Follow the interactive menu prompts

### Main Menu

```
Methods That Project Solve, please Enter your number operation

1 - Non linear Algebraic
2 - Interpolating Polynomials
3 - Least Squares and Curve Fitting
4 - Numerical Differentiation
5 - Numerical Integration
```

### Example Workflow

#### Example 1: Finding Roots (Bisection Method)

```
1. Select option 1 (Non linear Algebraic)
2. Select option 1 (Bisection method)
3. Enter equation: x^2-4
4. Enter interval: 0 5
5. Choose to show steps: yes
```

**Output:**

```
f < 0 at x = a | f > 0 at x = b | midpoint c     | f(c)
________________|________________|________________|_________________
0.000000        |5.000000        |2.500000        |2.250000
0.000000        |2.500000        |1.250000        |-2.437500
1.250000        |2.500000        |1.875000        |-0.484375
1.875000        |2.500000        |2.187500        |0.785156
1.875000        |2.187500        |2.031250        |0.126953
...

x = 2.0000000000
f(x) = 0.0000000000
```

#### Example 2: Numerical Integration

```
1. Select option 5 (Numerical Integration)
2. Enter equation: x^2
3. Enter a: 0
4. Enter b: 2
5. Enter n (or h): y
6. Enter n: 10
```

**Output:**

```
TrapezoidalRule:
result = 2.6666666667
error = 0.0000000000

SimpsonRule:
result = 2.6666666667
error = 0.0000000000
```

## 📝 Examples

### Equation Input Format

- **No spaces** in equations
- Use parentheses for clarity: `(x+2)*(x-3)`
- Function syntax: `sin(x)`, `cos(x)`, `ln(x)`, etc.

**Valid Examples:**

```
x^2-4
x^3-x-2
sin(x)-x/2
x-cos(x)+3*sin(x)
exp(x)-2*x
ln(x)+x^2
```

**Invalid Examples:**

```
x ^ 2 - 4        (spaces not allowed)
x**2             (use ^ for power)
sin (x)          (no space after function name)
```

### Bisection Method Example

**Input:**

- Equation: `x^2-4`
- Interval: `[0, 5]`
- Show steps: `yes`

**Expected Result:** Root at x ≈ 2.0

### Newton's Method Example

**Input:**

- Equation: `x^3-x-2`
- Initial guess: `1.5`
- Show steps: `yes`

**Expected Result:** Root at x ≈ 1.5213797

### Curve Fitting Example

**Input:**

- Method: Linear regression
- Points: (1, 2), (2, 4), (3, 6), (4, 8)

**Expected Result:** y = 2x + 0

## 🏗️ Project Structure

```
Math 4 Project/
├── Math 4 Project.cpp          # Main source file (2,180 lines)
├── Math 4 Project.sln          # Visual Studio solution file
├── Math 4 Project.vcxproj      # Visual Studio project file
└── README.md                   # This file
```

### Class Hierarchy

```
CommonFunctions (base class)
├── Differentiation
│   ├── newtonthodMethod
│   ├── NumericalIntegration
│   └── NumericalDifferentiation
├── BisectionMethod
└── jacobianMethod

Standalone Classes:
├── leastSquavesCurveFitting
├── Lagrange
└── divDifference
```

## 🛠️ Technologies

- **Language:** C++11
- **Libraries:** Standard C++ Library only
  - `<iostream>` - Input/Output
  - `<string>` - String manipulation
  - `<cmath>` - Mathematical functions
  - `<vector>` - Dynamic arrays
  - `<iomanip>` - Output formatting
- **Paradigm:** Object-Oriented Programming with inheritance
- **Platform:** Windows (primary), Linux/macOS (with modifications)

## 📊 Technical Specifications

| Metric                               | Value               |
| ------------------------------------ | ------------------- |
| Lines of Code                        | 2,180               |
| Numerical Methods                    | 8+                  |
| Supported Functions                  | 13                  |
| Convergence Tolerance                | 1e-7 (0.0000001)    |
| Max Data Points (Lagrange)           | 1,000               |
| Max Data Points (Divided Difference) | 100                 |
| Precision                            | 4-10 decimal places |

## ⚙️ Configuration

### Tolerance Settings

- **Bisection Method:** 1e-7 (line 786)
- **Newton-Raphson:** 1e-7 (line 890)
- **Max Iterations:** 20 (Newton-Raphson, line 900)

### Precision Settings

- **Bisection:** 6 decimals (steps), 10 decimals (final)
- **Newton-Raphson:** 9 decimals
- **Integration:** 10 decimals
- **Interpolation:** 4 decimals

## 🐛 Known Limitations

1. **Parabola Curve Fitting:** Only displays computation table; coefficient solving not fully implemented
2. **Graph Plotting:** Requires Windows GDI (Windows-specific feature)
3. **Global Variables:** Uses global state for number encoding (may cause issues with multiple simultaneous evaluations)
4. **Error Handling:** Limited input validation; may crash on invalid expressions

## 🔧 Platform-Specific Features

This version includes Windows-specific features:

- **Graph Plotting:** Uses Windows GDI API for visual function plotting
- **Console Styling:** Uses Windows system calls for colored output and screen clearing
- **Windows Headers:** Includes `windows.h` and `mmsystem.h` for Windows API functionality

For cross-platform compatibility, these features would need to be conditionally compiled or disabled.

## 📚 Algorithm Details

### Expression Parsing

- Custom infix-to-postfix conversion (similar to Shunting Yard algorithm)
- Handles operator precedence (+, - = 1; \*, / = 2; functions = 3)
- Special encoding for multi-digit numbers and negative values

### Symbolic Differentiation

- Implements product rule, quotient rule, and chain rule
- Handles composite functions
- Supports all 13 mathematical functions

### Root Finding

- **Bisection:** Guaranteed convergence, slower
- **Newton-Raphson:** Fast convergence, requires good initial guess
- **Newton-Jacobian:** For systems of 2 non-linear equations

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
