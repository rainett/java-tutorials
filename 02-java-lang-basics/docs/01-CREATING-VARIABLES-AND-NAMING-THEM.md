# Variables
Sometimes variables may be called fields and vice versa.
Java introduces four types of variables:
## Instance variables
These exist within an object that belongs to some class. As in example with a `Bicycle`, 
you can create a field `speed`. Every bicycle has it's individual speed - that's a state of 
a single bicycle, not all of them at once - this makes the `speed` an **instance** variable.

## Class variables
These exist within a class. Technically it is shared with the objects with the class, but 
it is specific to the class in general. For example, you want to specify that the max gear
of a bicycle is 6. You can create a final class field (final makes it constant):
```java
class Bicycle {
  static final int MAX_GEAR = 6;
  
  int gear = 1;
}
```
There are more tricks to it. For example, if you don't want to make it final, it can be modified
by any objects of that class, or from calling the class itself.

## Local variables
Method can have its own variables too. These are not coming from outside and not going to outside.
Their scope is only the method.
```java
int calculateExpression(int a, int b) {
  int sum = a + b; // local variable
  int product = a * b; // local variable
  return sum + product;
}
```

## Method parameters
Method has some input parameters. These are variables too. In the example above, `a` and `b` 
are method parameters.

# Naming variables
Honestly this is dumb, you will never name your variable with a special character or something like
that. These kinds of questions always pissed me off, as they don't represent any real use case. 
Anyway, here's what we can and cannot do in Java:
- Variables are case-sensitive. 
- Variables can start with a letter, $, or the underscore _.
- Subsequent characters may be letters, digits, dollar signs, underscores.
- Capitilize every following word, e.g.: `getSpeed`, `findById`.
- Constants are all uppercase, separated with underscore: `MAX_GEAR`.