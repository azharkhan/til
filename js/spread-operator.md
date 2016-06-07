# Spread Operator ( ES6 / ES2015 )

The spread operator `...` is a handy syntax introduced in ES6 / ES2015 which allows an expression to be expanded into individual arguments (for function calls) or individual elements (for arrays etc.)

### Examples

    // concat an array
    const greeting = ['This', 'is', 'a', 'test'];

    console.log(...greeting);

    > "This is a test"

    // it can help convert an array to individual params for a function

    // eg: finding lowest number in array
    let numbers = [1, 5, 10];

    // we can use the `Math.min` function, but it doesn't accept an array
    // we can use the spread operator, to send this to the function
    Math.min(...numbers);

    // it can also be helpful for destructuring

    [a, b, ...iterableObj] = [1,2,3,4,5];

    // helps with `apply` or `push`

    var arr1 = [0,1,2];
    var arr2 = [3,4,5];

    // append all items from arr2 to arr1
    Array.prototype.push.apply(arr1, arr2);

    // with ... operator
    arr1.push(...arr2);

