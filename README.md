# parentheses-problem
Expression Parenthesization Evaluator

This program computes the minimum and maximum possible values of a given arithmetic expression by adding parentheses in all valid ways. It returns both the value and the corresponding parenthesized expression that produces that value.
Problem Description

Given a string containing digits and arithmetic operators (+, -, *, /), the goal is to find the minimum and maximum value that can result from fully parenthesizing the expression in every possible valid way.

For example, the input 6+2*0-4 has many valid parenthesizations such as ((6+2)*(0-4)), ((6+(2*0))-4), and so on. The program should return both the lowest and highest values obtained and show the expressions that produce them.
Stipulations

The following conditions apply to the problem:

The original character order of digits and operators must be preserved.

Parentheses may be added aggressively in any valid configuration. This includes placing parentheses inside multi-digit numbers by splitting them into smaller sub-expressions. For instance, 66 may be split into 6*6 if the input expression includes operators between the digits introduced by parentheses.

No new operators may be added. Only the ones already present in the input string may be used.

All operations are integer-based. Division is performed using integer division and must avoid divide-by-zero errors.

Each evaluated expression must produce a valid integer result. Invalid operations such as divide-by-zero are skipped.

The output must include both the minimum and maximum values along with the expressions that produce them.
Features

Parses the input expression into a list of numbers and operators

Supports addition, subtraction, multiplication, and integer division

Recursively evaluates all valid parenthesizations using memoization

Tracks and returns both the minimum and maximum expression evaluations

Supports batch evaluation of multiple expressions
How to Use

Run the script with any string-based expression such as "6+2*0-4" or "66*23+2*0-4". The script will print the minimum and maximum values and the expressions that yield those results.
Example Output

Expression: 6+20-4
Min Value: -32 from ((6+2)(0-4))
Max Value: 2 from ((6+(2*0))-4)

Expression: 6623+20-4
Min Value: -6600 from ((66*(23+2))(0-4))
Max Value: 1518 from ((6623)+(2*(0-4)))
Dependencies

Python 3.6 or higher
No external libraries required (uses built-in functools and operator modules)
License

This project is free to use and modify.