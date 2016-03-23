# Reduce

`reduce()` is an array operation that applies a callback function to each value in the array ( from left to right ) and accumulates the result as defined by the function into an accmulator.

It's a powerful functional programming paradigm, allowing for simple operations such as sum of arrays, as well as complex functions that take other functions as arguments and accumulate their results into a final desired result.

## Arguments

the callback function within `reduce()` takes 4 arguments:

- previousValue
- currentValue
- index
- array

NOTE: if a default value is not provided ( to be the first argument of the reduce function ), it will default to using the value at the 0 index.

## Examples

1. Product of all numbers in an array

    var numbers = [ 1, 2, 3, 4, 5 ];

    product = numbers.reduce(function( prev, curr ) {
        return prev * curr;
    }, 1);
