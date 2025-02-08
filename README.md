# Unexpected Behavior with Mutable Variables in F#

This example demonstrates a common pitfall when working with mutable variables in F#: the unexpected modification of original variables due to pass-by-reference behavior.

## Bug

The `swap` function attempts to swap the values of `x` and `y`. However, because F# mutable variables are passed by reference, the function modifies the original variables directly.  This results in an unexpected output.

## Solution

To correctly swap the values, create a new tuple containing the swapped values and return the tuple. This way, the original variables remain unchanged.