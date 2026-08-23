# Runge-Kutta 4th Order Numerical Solver

A simple and interactive **web-based numerical solver** for solving first-order Ordinary Differential Equations (ODEs) using the **Runge-Kutta Fourth Order (RK4) method**.

The application is built with **Python, Gradio, Matplotlib, and Pandas** and provides the numerical result, step-by-step RK4 calculation table, and a graphical representation of the solution.

## Features

- Solve first-order ODEs using the **RK4 method**
- Interactive and user-friendly web interface
- Accepts equations in the form:

  `dy/dx = f(x, y)`

- User can provide:
  - Differential equation
  - Initial `x₀`
  - Initial `y₀`
  - Target `x`
  - Step size `h`
- Displays the final approximate value of `y`
- Shows a detailed step-by-step calculation table
- Generates a graph of the numerical solution
- Provides clear validation and error messages
- Supports common mathematical functions such as:
  - `sin`
  - `cos`
  - `tan`
  - `asin`
  - `acos`
  - `atan`
  - `sinh`
  - `cosh`
  - `tanh`
  - `exp`
  - `log`
  - `log10`
  - `sqrt`
  - `abs`
  - `pi`
  - `e`

## Technologies Used

- **Python**
- **Gradio** – Web interface
- **Matplotlib** – Solution graph
- **Pandas** – Calculation table
- **Math** – Mathematical functions

## How RK4 Works

For a first-order differential equation:

```text
dy/dx = f(x, y)
```

RK4 calculates four slope estimates at every step:

```text
k1 = h × f(xₙ, yₙ)

k2 = h × f(xₙ + h/2, yₙ + k1/2)

k3 = h × f(xₙ + h/2, yₙ + k2/2)

k4 = h × f(xₙ + h, yₙ + k3)
```

Then the next value of `y` is calculated using:

```text
yₙ₊₁ = yₙ + (k1 + 2k2 + 2k3 + k4) / 6
```

This process is repeated until the target `x` value is reached.

## Installation

Clone the repository:

```bash
git clone https://github.com/tanha-s-tusty/Graph-Generator.git
```

Go to the project directory:

```bash
cd Graph-Generator
```

Install the required packages:

```bash
pip install gradio matplotlib pandas
```

## Run the Application

Run the Python file:

```bash
python app.py
```

After running the program, Gradio will provide a local web interface where you can enter the equation and calculation parameters.

## Example

Suppose the differential equation is:

```text
dy/dx = x + y
```

Use:

```text
Initial x₀ = 0
Initial y₀ = 1
Target x = 1
Step Size h = 0.1
```

Then click:

**Calculate RK4 Solution**

The application will display:

1. The approximate final value of `y`
2. RK4 values of `k1`, `k2`, `k3`, and `k4`
3. The new `y` value at every step
4. A graph of the numerical solution
5. An explanation of how the result was calculated

## Input Format

The equation should use `x` and `y` as variables.

### Valid examples

```text
x + y
x*y
sin(x) + y
x**2 + y
exp(x) - y
sqrt(x + y)
```

Supported operators include:

```text
+   -   *   /   **
```

## Error Handling

The application validates user inputs and provides friendly error messages for problems such as:

- Empty differential equation
- Invalid numeric input
- Zero step size
- Incorrect step direction
- Unsupported mathematical expressions
- Division by zero
- Invalid mathematical results
- Too many required calculation steps
- Complex-number results

## Project Structure

```text
Runge-Kutta-4th-Order/
│
├── app.py
└── README.md
```

> Rename your uploaded Python file to `app.py` before pushing it to GitHub, if you want to use the structure above.

## Purpose

This project is designed as an educational tool for understanding and applying the **Runge-Kutta Fourth Order numerical method** to solve first-order ordinary differential equations.

It combines the mathematical calculation with an interactive interface so that users can easily understand both the **final result** and the **step-by-step RK4 process**.

## License

This project is intended for educational and academic purposes.
