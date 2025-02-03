# F# Mutability Bug: Swapping Variables

This example demonstrates a common mistake when working with mutability in F#. The `swap` function attempts to swap two mutable variables, but due to the immutable nature of function parameters in F#, it fails to modify the original variables.

## How to Reproduce

1. Compile and run `bug.fs`.
2. Observe that the output shows that the variables were not swapped.

## Solution

The solution involves passing mutable variables by reference using the `byref` keyword. This allows the function to modify the original variables directly.

See `bugSolution.fs` for the corrected code.