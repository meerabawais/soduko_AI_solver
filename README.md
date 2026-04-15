# soduko_AI_solver
Overview:

This project implements a Constraint Satisfaction Problem (CSP) based Sudoku solver using:

Backtracking Search
AC-3 (Arc Consistency Algorithm)
MRV (Minimum Remaining Values Heuristic)

The solver is designed to solve Sudoku puzzles of varying difficulty levels, including:

Easy
Medium
Hard
Very Hard
Objective:

The goal of this assignment is to:

Implement a CSP-based Sudoku solver.
Solve four given Sudoku boards.
Track:
Number of backtracking calls
Number of backtracking failures
Analyze solver performance based on difficulty.
Input Format:

Each Sudoku board is stored in a .txt file with the following format:

Exactly 9 lines
Each line contains 9 digits (0–9)
0 represents an empty cell
Example (easy.txt)
004030050
609400000
005100489
000060930
300807002
026040000
453009600
000004705
090050200

How It Works:
1. CSP Representation
Each cell = Variable
Domain = {1–9} (or fixed value if given)
Constraints:
Row constraint
Column constraint
3×3 box constraint
2. Algorithms Used
AC-3 (Arc Consistency)
Reduces domains before search begins
Removes inconsistent values
Backtracking Search
Assigns values recursively
Explores possible solutions
MRV Heuristic
Selects the variable with the smallest domain
Improves efficiency
How to Run:
Make sure all input files are in the same directory:
easy.txt
medium.txt
hard.txt
veryhard.txt
Then run:
python your_file_name.py
Output
For each Sudoku board, the program prints:
Solved Sudoku grid
Number of backtracking calls
Number of backtracking failures
Expected values (for comparison)
Performance Analysis
Easy Board
Very few backtracking calls and failures
Puzzle is simple with fewer empty cells
Medium Board
Increased number of calls and failures
Requires moderate search
Hard Board
Large number of backtracking steps
More complex constraints
Very Hard Board
Very high number of calls and failures
Demonstrates exponential growth in complexity
