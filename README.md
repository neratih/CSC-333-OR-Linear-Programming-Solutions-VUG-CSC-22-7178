Project Description

This project focuses on solving various Linear Programming (LP) problems using Python. LP is a mathematical method for determining the optimal allocation of limited resources to achieve a specific objective, such as minimizing cost or maximizing profit/revenue. The project involves several real-world scenarios, including manufacturing, resource allocation, production planning, and advertising campaigns.

The problems are solved using Python libraries like **SciPy**, which provides tools for optimization, and **Matplotlib** for visual representation (if needed). Each problem is solved programmatically by defining the objective function, constraints, and bounds, and then finding the optimal solution.

---

### Objectives of LP Problems

1. **Minimizing Costs**  
   Problems involve reducing production or operational costs under resource constraints.

2. **Maximizing Profit/Revenue**  
   Problems aim to achieve the highest profit or revenue given limited resources and predefined constraints.

3. **Efficient Resource Allocation**  
   Problems deal with distributing limited resources (e.g., labor, materials, time) optimally across different activities.

---

### How the Problems Were Solved

Each problem was approached using the following steps:

1. **Define the Objective Function**  
   This represents the goal of the optimization, e.g., maximizing profit (\( Z = c_1x + c_2y \)) or minimizing cost (\( Z = c_1x + c_2y \)).

2. **Set Up Constraints**  
   Constraints represent the limitations of resources, e.g., \( a_1x + b_1y \leq d_1 \).

3. **Solve Using `SciPy`**  
   Python's **SciPy** library was used to solve the LP problems using the `linprog` function, which finds the optimal solution by minimizing or maximizing the objective function under the given constraints.

4. **Validate Results**  
   Ensure that the solutions satisfy all constraints and meet the objective.

---

### Instructions for Running the Python Code

Create a `README.md` file with the following content to guide users on running the code.

---

#### README.md

### Linear Programming Optimization Project

This project demonstrates the use of Python to solve linear programming problems. The problems span various real-world applications, such as minimizing costs, maximizing profits, and optimizing resource allocation.

---

#### Requirements

Ensure you have Python 3.7+ installed along with the required libraries:

1. **SciPy** (for optimization)
2. **NumPy** (for numerical operations)
3. **Matplotlib** (optional, for visualizations)

Install the required libraries using:

```bash
pip install scipy numpy matplotlib
```

---

#### Running the Code

1. **Clone the Repository**  
   Clone the project repository to your local machine:

   ```bash
   git clone <repository_url>
   cd <repository_name>
   ```

2. **Run the Python Script**  
   Execute the main script to solve all LP problems:

   ```bash
   python solve_lp_problems.py
   ```

3. **Output**  
   The script will display the optimal solutions for all problems in the terminal. Example:

   ```
   Problem 1: Optimal solution: [x1, x2], Optimal value: Z
   Problem 2: Optimal solution: [x1, x2], Optimal value: Z
   ```

---

#### Adding Your Problems

To add custom LP problems:

1. Edit `solve_lp_problems.py` and append your problem definitions in the `problems` list.
2. Use the same structure as the examples provided in the script.

---

#### Sample Code Snippet

Below is a simplified example of the Python code:

```python
from scipy.optimize import linprog

# Define the objective function, constraints, and bounds
objective = [2, 5]  # Minimize 2x + 5y
A_ub = [[1, 2], [2, 1]]  # Constraints: x + 2y <= 5, 2x + y <= 6
b_ub = [5, 6]
bounds = [(0, None), (0, None)]  # x >= 0, y >= 0

# Solve the problem
result = linprog(c=objective, A_ub=A_ub, b_ub=b_ub, bounds=bounds, method="highs")
if result.success:
    print("Optimal solution:", result.x)
    print("Optimal value:", result.fun)
else:
    print("Problem could not be solved.")
```

---

#### Contributing

Contributions to extend the project or improve solutions are welcome. Fork the repository, make your changes, and submit a pull request.

--- 

If you’d like, I can help refine this further or include additional explanations about each problem.
