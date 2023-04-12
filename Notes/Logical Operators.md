#js #javascript #webDev #dev #docs #js/operators 

Logical Operators are used to perform logical operations on boolean values. JavaScript supports three logical operators: AND (&&), OR (||), and NOT (!).

## AND Operator (&&)

The AND operator returns true only if both operands are true. If either operand is false, it returns false. The syntax for using the AND operator is:

```
    operand1 && operand2

```

Here's an example:

```
    var x = 10;
    var y = 20;
    if (x > 5 && y < 30) {
        console.log("Both operands are true");
    }

```

In this example, the condition `x > 5 && y < 30` is true because both operands are true. Therefore, the message "Both operands are true" will be displayed in the console.

## OR Operator (||)

The OR operator returns true if either of the operands is true. If both operands are false, it returns false. The syntax for using the OR operator is:

```
    operand1 || operand2

```

Here's an example:

```
    var x = 10;
    var y = 20;
    if (x > 5 || y > 30) {
        console.log("At least one operand is true");
    }

```

In this example, the condition `x > 5 || y > 30` is true because the first operand is true. Therefore, the message "At least one operand is true" will be displayed in the console.

## NOT Operator (!)

The NOT operator returns the opposite of the boolean value of the operand. If the operand is true, it returns false. If the operand is false, it returns true. The syntax for using the NOT operator is:

```
    !operand

```

Here's an example:

```
    var x = 10;
    var y = 20;
    if (!(x > 5)) {
        console.log("The condition is false");
    }

```

In this example, the condition `!(x > 5)` is false because the operand `x > 5` is true. Therefore, the message "The condition is false" will not be displayed in the console.



### [[Operators|<- Back to JavaScript/Operators]]