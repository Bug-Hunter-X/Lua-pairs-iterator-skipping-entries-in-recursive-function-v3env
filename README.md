# Lua pairs iterator skipping entries in recursive function

This repository demonstrates a potential issue with Lua's `pairs` iterator when used recursively on tables that are modified during iteration. The `bug.lua` file contains a function that recursively iterates through a table. If a nested table is modified while the function is iterating through it, the `pairs` iterator may skip entries.

The `bugSolution.lua` provides the solution by using a copy of the table to iterate through instead of modifying the original table during iteration. This avoids the iterator from skipping entries.  The solution also includes better error handling and clarity.