# Haskell Space Leak: Unboxed Tuples in Recursion

This repository demonstrates a potential space leak in Haskell caused by the inefficient use of unboxed tuples within a recursive function.  The `bug.hs` file contains the problematic code, while `bugSolution.hs` provides a corrected version.

**Problem:** The original code uses unboxed tuples, which while offering performance advantages, can lead to significant memory consumption in recursive scenarios if not properly managed.  Each recursive call creates a new tuple, potentially leading to a large build-up of memory that is only released upon termination of the function.

**Solution:** The solution employs techniques to mitigate the memory issues, primarily by changing the structure to avoid unnecessary tuple creation during recursion, improving memory management.