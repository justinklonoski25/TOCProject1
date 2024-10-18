# TOCProject1
SATSolver

Project Overview
This project centers around the development of a SAT (Satisfiability) solver using Python. The solver is designed to determine whether a Boolean formula in Conjunctive Normal Form (CNF) is satisfiable. The focus of the project lies in implementing and analyzing two main algorithms for solving SAT problems: 2SAT and kSAT, with the aim of exploring their efficiency and performance.
Project Contributor
Justin Klonoski
Time Allocation
Total project duration: Around 10 hours
Code Management
To maintain the codebase and track changes effectively, I established a Git repository for this project. It allowed me to document revisions and ensure the SAT solver's development followed a structured approach.
Testing Strategy
Testing played an integral role in the development process. A range of test cases was carefully created to account for multiple scenarios, including common use cases and edge cases that could potentially break the solver. The tests were automated using the pytest framework, streamlining the process of verifying the correctness of the SAT solver's outputs. This approach ensured that both 2SAT and kSAT algorithms performed as expected across diverse inputs.
Programming Language and Libraries
Programming language: Python
Libraries used:
matplotlib: For generating graphs and visualizing performance metrics.
csv: To facilitate reading from and writing to CSV files.
random: For randomization of variables and clauses, essential for test generation and stress testing.


Key Data Structures
Representation of well-formed formulas (wffs): Formulas were internally structured as a list of clauses, where each clause itself was a list of literals (Boolean variables or their negations).
Variable assignments: Stored as Boolean lists, representing the truth values assigned to each variable during the solving process.
Choice point stacks: Implemented using lists to track the state of variable assignments throughout the backtracking algorithm, enabling efficient exploration of solution spaces.
Execution Time Analysis
For each SAT problem and corresponding test file, I analyzed execution times by generating charts that plotted execution time against the number of variables in the formula. Different symbols were used to distinguish between satisfiable and unsatisfiable well-formed formulas (wffs), specifically in 2SAT problems:
Satisfiable formulas were marked with green points.
Unsatisfiable formulas were represented with red points.
The results were exported to CSV files for further analysis and could be easily imported into spreadsheet tools for graphing and data visualization.
Curve Fit to Worst-Case Times
I performed a curve fitting analysis on the worst-case execution times, based on both the number of variables (V) and the total number of literals present in each well-formed formula. This allowed me to quantify how the performance of the solver scaled with problem complexity.
Observations and Insights
Throughout the testing process, I observed that solving SAT problems becomes increasingly difficult as the number of literals per clause (denoted by k) grows. The shift from solving 2SAT problems to 3SAT and higher complexity versions resulted in a significant rise in execution time, highlighting the rapid increase in computational complexity when handling formulas with more than two literals per clause.
