# Javascript Basics - 3

## [Comparison Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators)

* JavaScript has both strict and type–converting comparisons. A strict comparison (e.g., ===) is only true if the operands are of the same type and the contents match. 

* The more commonly-used abstract comparison (e.g. ==) converts the operands to the same type before making the comparison. 

* Features of comparisons:
    - Two strings are strictly equal when they have the same sequence of characters, same length, and same characters in corresponding positions.
    - Two numbers are strictly equal when they are numerically equal (have the same number value). NaN is not equal to anything, including NaN. Positive and negative zeros are equal to one another.
    - Two Boolean operands are strictly equal if both are true or both are false.
    - Two distinct objects are never equal for either strict or abstract comparisons.
    - An expression comparing Objects is only true if the operands reference the same Object.
    - Null and Undefined Types are strictly equal to themselves and abstractly equal to each other.

## Equality operators

1) **Equality (==)**
    - The equality operator converts the operands if they are not of the same type, then applies strict comparison.
    - If **both operands are objects**, then JavaScript compares internal references which are equal when operands refer to the same object in memory.

    ```javascript
        1    ==  1         // true
        '1'  ==  1         // true
        1    == '1'        // true
        0    == false      // true
        0    == null       // false
        var object1 = {'key': 'value'}, object2 = {'key': 'value'}; 
        object1.key == object2.key //true
        0    == undefined  // false
        null == undefined  // true
    ```

2) **Inequality (!=)**
    - The inequality operator returns true if the operands are not equal. If the two operands are not of the same type, JavaScript attempts to convert the operands to an appropriate type for the comparison.
    - If **both operands are objects**,  then JavaScript compares internal references which are not equal when operands refer to different objects in memory.

    ```javascript
        1 !=   2     // true
        1 !=  '1'    // false
        1 !=  "1"    // false
        1 !=  true   // false
        0 !=  false  // false
    ```

3) **Identity / strict equality (===)**
    - The identity operator returns true if the operands are strictly equal **with no type conversion.**

    ```javascript
        3 === 3   // true
        3 === '3' // false
        var object1 = {'key': 'value'}, object2 = {'key': 'value'};
        object1 === object2 //false
    ```

4) **Non-identity / strict inequality (!==)**
    - The non-identity operator returns true if the operands **are not equal and/or not of the same type.**

    ```javascript
        3 !== '3' // true
        4 !== 3   // true
    ```

## Relational operators
* Each of these operators will [coerce](https://developer.mozilla.org/en-US/docs/Glossary/Type_coercion) its operands to primitives before a comparison is made. If both end up as strings, they are compared using lexicographic order, otherwise they are cast to numbers to be compared. A comparison against NaN will always yield false.

1) **Greater than operator (>)**
    - The greater than operator returns true if the left operand is greater than the right operand.

    ```javascript
        4 > 3 // true
    ```
2) **Greater than or equal operator (>=)**
    - The greater than or equal operator returns true if the left operand is greater than or equal to the right operand.
   
    ```javascript
        4 >= 3 // true
        3 >= 3 // true
    ```

3) **Less than operator (<)**
    - The less than operator returns true if the left operand is less than the right operand.

    ```javascript
        3 < 4 // true
    ```

4) **Less than or equal operator (<=)**
    - The less than or equal operator returns true if the left operand is less than or equal to the right operand.

    ```javascript
        3 <= 4 // true
        3 <= 3 // true
    ```

## Extra

* The standard equality operators (== and !=) use the [Abstract Equality Comparison Algorithm](http://www.ecma-international.org/ecma-262/5.1/#sec-11.9.3) to compare two operands. If the operands are of different types, it will attempt to convert them to the same type before making the comparison, e.g., in the expression 5 == '5', the string on the right is converted to Number before the comparison is made.

* The strict equality operators (=== and !==) use the [Strict Equality Comparison Algorithm](http://www.ecma-international.org/ecma-262/5.1/#sec-11.9.6) and are intended for performing equality comparisons on operands of the same type. If the operands are of different types, like 5 and '5', an identity comparison 5 !== '5' will evaluate to true and a check 5 === '5' will evaluate to false.
