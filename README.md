# PHP Foreach Loop Pass-by-Reference Bug

This repository demonstrates a common, yet subtle, bug in PHP related to pass-by-reference in `foreach` loops.  Incrementing a value inside a `foreach` loop, when using pass-by-reference, modifies the original array element directly, potentially leading to unexpected behavior.

## The Bug

The `bug.php` file contains a function that attempts to increment each element of an array.  However, due to the use of pass-by-reference (`&$value`), the original array is modified directly.

## The Solution

The `bugSolution.php` file provides a corrected version that avoids unintended side effects.  It creates a copy of the value before incrementing, preventing changes to the original array.