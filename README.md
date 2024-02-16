# Java_Assignment_6

`Exam` interface:

- `public void Percent_cal()`: An interface method that is meant to be implemented by classes that implement the `Exam` interface. The method calculates the percentage, and any class implementing this interface needs to provide its own implementation for this method.

`Fixed_stk` class:

- `private int stack[]`: Private array representing the stack.
- `private int top`: Private variable representing the top of the stack.

- `public Fixed_stk(int[] stack, int top)`: Constructor that initializes the `stack` and `top` with the provided values.
- `@Override public void push(int element)`: Overrides the `push` method from the `Interface_STK` interface. It pushes an element onto the stack if there is no overflow.
- `@Override public int pop()`: Overrides the `pop` method from the `Interface_STK` interface. It pops an element from the stack if there is no underflow and returns the popped element.
- `@Override public void displayStack()`: Overrides the `displayStack` method from the `Interface_STK` interface. It displays the elements of the stack.
- `@Override public boolean overflow()`: Overrides the `overflow` method from the `Interface_STK` interface. It checks if the stack is full and returns `true` if it is, `false` otherwise.
- `@Override public boolean underflow()`: Overrides the `underflow` method from the `Interface_STK` interface. It checks if the stack is empty and returns `true` if it is, `false` otherwise.

`Growable_stk` class:

- `ArrayList<Integer> stack`: ArrayList representing the stack.
- `int top`: Variable representing the top of the stack.

- `public Growable_stk()`: Constructor that initializes the stack as an `ArrayList` with an initial capacity of 5 and sets the top to -1.
- `@Override public void push(int element)`: Overrides the `push` method from the `Interface_STK` interface. It adds an element to the stack and increments the top.
- `@Override public int pop()`: Overrides the `pop` method from the `Interface_STK` interface. It removes and returns the element at the top of the stack if there is no underflow.
- `@Override public void displayStack()`: Overrides the `displayStack` method from the `Interface_STK` interface. It displays the elements of the stack.
- `@Override public boolean overflow()`: Overrides the `overflow` method from the `Interface_STK` interface. It prints a message indicating that overflow is not applicable for a growable stack and returns `false`.
- `@Override public boolean underflow()`: Overrides the `underflow` method from the `Interface_STK` interface. It checks if the stack is empty and returns `true` if it is, `false` otherwise.

`Input` class:

- `takeInput()`: Takes user input for the number of students and their details (PRN, name, DoB, marks), creating `Result` objects and adding them to the list.

- (assuming `Result` class has a suitable `toString()` method) `displayResults()`: Prints the details of all students in the list using the `toString()` method.

`Interface_STK` interface:

- `public void push(int element)`: Interface method to push an element onto the stack.
- `public int pop()`: Interface method to pop an element from the stack.
- `public void displayStack()`: Interface method to display the elements of the stack.
- `public boolean overflow()`: Interface method to check if the stack is in overflow condition.
- `public boolean underflow()`: Interface method to check if the stack is in underflow condition.

`MainResult` class:

- Creates an instance of the `Result` class with the name "Aayush", PRN 003, marks 98, and marks 96.
- Calls the `display()` method of the `Result` class to print the details of the result.

`MainSTK` class:

- Creates an array-based stack and an `ArrayList`-based stack.
- Creates an instance of the `Growable_stk` class.
- Pushes elements (1 to 6) onto the growable stack.
- Displays the elements of the growable stack using the `displayStack()` method.

`Result` class:

- Extends the `Student` class and implements the `Exam` interface.
- Additional field: `double percentage` to store the calculated percentage.
- `public Result(String name, int roll_no, double mark1, double mark2)`: Constructor that initializes the `Result` object with the provided name, roll number, and marks.
- `@Override public void Percent_cal()`: Overrides the `Percent_cal` method from the `Exam` interface. Calculates the percentage based on the marks.
- `public String display()`: Calls the `Percent_cal` method and returns the string representation of the result.
- `@Override public String toString()`: Overrides the `toString` method to provide a string representation of the result, including the percentage, name, roll number, and marks.

`Student` class:

- Fields: `String name`, `int roll_no`, `double mark1`, `double mark2`.
- Constructor: `public Student(String name, int roll_no, double mark1, double mark2)`: Initializes the `Student` object with the provided name, roll number, and marks.
- Getter and setter methods for each field.
- `@Override public String toString()`: Overrides the `toString` method to provide a string representation of the student, including the name, roll number, and marks.
