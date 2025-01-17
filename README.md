# JavaScript Type Coercion Bug

This repository demonstrates a common subtle bug in JavaScript related to type coercion within conditional checks. The `foo` function is designed to return `null` only when one or both of its arguments are explicitly `null`. However, due to JavaScript's loose comparison (`==`), it incorrectly returns `null` when 'falsy' values such as `0` or `""` are passed as arguments.

## Bug Description:
The problem lies in the use of `===`  in the `if` condition.  While `===` performs strict equality comparison, avoiding type coercion, the use of `==` leads to unexpected results when 'falsy' values are passed, causing incorrect null returns.  This could lead to unexpected application behavior or errors if not carefully considered.

## Solution:
The provided solution demonstrates a safer alternative.  It continues using `===` for strict comparisons, ensuring that the function only returns `null` when either input is strictly equal to `null`.