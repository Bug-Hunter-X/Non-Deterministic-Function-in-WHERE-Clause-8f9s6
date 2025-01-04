# Non-Deterministic Function in SQL WHERE Clause

This repository demonstrates a common, yet subtle, error in SQL: using a non-deterministic function (like `RAND()`) within a WHERE clause.  This can result in queries producing different results on each execution, making debugging and testing challenging.  The `bug.sql` file contains the problematic query, while `bugSolution.sql` offers a possible solution.

**Problem:**  Using functions that generate different outputs for the same input (non-deterministic) in WHERE clauses leads to unpredictable query behavior.

**Solution:** Avoid using non-deterministic functions in WHERE clauses whenever possible. If such a function is required, carefully consider its implications and potential workarounds.