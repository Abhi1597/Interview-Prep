# Javascript Basics - 2

## [Arithematic Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators)

* Arithmetic operators take numerical values (either literals or variables) as their operands and return a single numerical value. 

* The standard arithmetic operators are addition (+), subtraction (-), multiplication (*), and division (/).

1) **Addition (+)**
    - The addition operator produces the sum of numeric operands or string concatenation.

    ```javascript
        // Number + Number -> addition
        1 + 2 // 3

        // Boolean + Number -> addition
        true + 1 // 2

        // Boolean + Boolean -> addition
        false + false // 0

        // Number + String -> concatenation
        5 + 'foo' // "5foo"

        // String + Boolean -> concatenation
        'foo' + false // "foofalse"

        // String + String -> concatenation
        'foo' + 'bar' // "foobar"
    ```

2) **Subtraction (-)**
    - The subtraction operator subtracts the two operands, producing their difference.

    ```javascript
        5 - 3 // 2
        3 - 5 // -2
        'foo' - 3 // NaN
    ```

3) **Division (/)**
    - The division operator produces the quotient of its operands where the left operand is the dividend and the right operand is the divisor.

    ```javascript
        1 / 2      // returns 0.5 in JavaScript
        1 / 2      // returns 0 in Java 
        // (neither number is explicitly a floating point number)

        1.0 / 2.0  // returns 0.5 in both JavaScript and Java

        2.0 / 0    // returns Infinity in JavaScript
        2.0 / 0.0  // returns Infinity too
        2.0 / -0.0 // returns -Infinity in JavaScript
    ```

4) **Multiplication (*)**
    - The multiplication operator produces the product of the operands.

    ```javascript
        2 * 2 // 4
        -2 * 2 // -4
        Infinity * 0 // NaN
        Infinity * Infinity // Infinity
        'foo' * 2 // NaN
    ```

5) **Remainder (%)**
    - The remainder operator returns the remainder left over when one operand is divided by a second operand. It always takes the sign of the dividend.

    ```javascript
        12 % 5 // 2
        -1 % 2 // -1
        1 % -2 // 1
        NaN % 2 // NaN
        1 % 2 // 1
        2 % 3 // 2
        -4 % 2 // -0
        5.5 % 2 // 1.5
    ```

6) **Exponentiation**(**)
    - The exponentiation operator returns the result of raising first operand to the power second operand.      Exponentiation operator is right associative. a ** b ** c is equal to a ** (b ** c).

    ```javascript
         2 ** 2; 
        // 4 in Bash, -4 in other languages. 
        // This is invalid in JavaScript, as the operation is ambiguous. 
        -(2 ** 2); 
        // -4 in JavaScript and the author's intention is unambiguous. 

        2 ** 3 // 8
        3 ** 2 // 9
        3 ** 2.5 // 15.588457268119896
        10 ** -1 // 0.1
        NaN ** 2 // NaN

        2 ** 3 ** 2 // 512
        2 ** (3 ** 2) // 512
        (2 ** 3) ** 2 // 64
    ```


7) **Increment (++)**
    - The increment operator increments (adds one to) its operand and returns a value.
    - If used postfix, with operator after operand (for example, x++), then it increments and **returns the value before incrementing**.
    - If used prefix, with operator before operand (for example, ++x), then it increments and **returns the value after incrementing.**

    ```javascript
        // Postfix 
        var x = 3;
        y = x++; // y = 3, x = 4

        // Prefix
        var a = 2;
        b = ++a; // a = 3, b = 3
    ```


8) **Decrement (--)**
    - The decrement operator decrements (subtracts one from) its operand and returns a value.
    - If used postfix, with operator after operand (for example, x--), then it decrements and **returns the value before decrementing.**
    - If used prefix, with operator before operand (for example, --x), then it decrements and **returns the value after decrementing.**

    ```javascript
        // Postfix 
        var x = 3;
        y = x--; // y = 3, x = 2

        // Prefix
        var a = 2;
        b = --a; // a = 1, b = 1
    ```


9) **Unary negation (-)**
    - The unary negation operator precedes its operand and negates it.

    ```javascript
       var x = 3;
        y = -x; // y = -3, x = 3

        // Unary negation operator can convert non-numbers into a number
        var x = "4";
        y = -x; // y = -4
    ```


10) **Unary plus (+)**
    - The unary plus operator precedes its operand and evaluates to its operand but attempts to convert it into a number, if it isn't already.
    - unary plus is the fastest and preferred way of converting something into a number, because it does not perform any other operations on the number. 

    ```javascript
        +3     // 3
        +'3'   // 3
        +true  // 1
        +false // 0
        +null  // 0
        +function(val){ return val } // NaN
    ```