# Java_Assignment_6

Exam interface:

public void Percent_cal(): An interface method that is meant to be implemented by classes that implement the `Exam` interface. The method calculates the percentage, and any class implementing this interface needs to provide its own implementation for this method.

`Fixed_stk` class:

- `private int stack[]`: Private array representing the stack.
- `private int top`: Private variable representing the top of the stack.

- `public Fixed_stk(int[] stack, int top)`: Constructor that initializes the `stack` and `top` with the provided values.
- `@Override public void push(int element)`: Overrides the `push` method from the `Interface_STK` interface. It pushes an element onto the stack if there is no overflow.
- `@Override public int pop()`: Overrides the `pop` method from the `Interface_STK` interface. It pops an element from the stack if there is no underflow and returns the popped element.
- `@Override public void displayStack()`: Overrides the `displayStack` method from the `Interface_STK` interface. It displays the elements of the stack.
- `@Override public boolean overflow()`: Overrides the `overflow` method from the `Interface_STK` interface. It checks if the stack is full and returns `true` if it is, `false` otherwise.
- `@Override public boolean underflow()`: Overrides the `underflow` method from the `Interface_STK` interface. It checks if the stack is empty and returns `true` if it is, `false` otherwise.
