# F# Mutable Variable Swap Bug

This repository demonstrates a common error involving mutable variables in F#. The `swap` function attempts to swap the values of two mutable variables, but it doesn't work as expected due to the way F# handles mutable variables and function arguments.

## Bug Description

The `bug.fs` file contains a function `swap` that intends to exchange the values of two mutable variables. However, the function does not correctly swap the values, leading to unexpected results.  The issue is that `x` and `y` are passed *by value*, creating copies that are swapped, not the original variables.

## Solution

The `bugSolution.fs` file provides a corrected version of the `swap` function that utilizes tuples or ref cells to achieve the correct swapping of the original variable values.