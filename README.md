# PHP Array Key Type Coercion Bug

This repository demonstrates a common, subtle bug in PHP related to how it handles array keys.  When you use non-integer values as array keys, PHP will implicitly cast them to strings, leading to unexpected behavior if you're not careful about the type of your keys.

The `bug.php` file shows the problematic code. The `bugSolution.php` offers a fix.

## Bug Description

The bug stems from PHP's loose typing system. Different keys (integer, boolean, float) get converted to strings, resulting in key collisions and unexpected data overwrites.

## Solution

The solution involves careful consideration of key types or using a more robust data structure such as an associative array where keys are consistently strings to avoid implicit type conversions.