# JavaScript Closure Issue in setTimeout Loop
This example demonstrates a common closure issue in JavaScript when using setTimeout within a loop.  The variable `i` is not captured correctly within the setTimeout callback, leading to unexpected behavior.

## Bug Description
The code intends to print numbers 0 through 9 to the console with a one-second delay between each number. However, due to the way closures work in JavaScript, the loop completes before the setTimeout callbacks execute, resulting in the value of `i` being 10 when the callbacks finally fire.  The output will be ten instances of '10'.

## Solution
The solution involves using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, ensuring each callback captures its own unique value of `i`.
