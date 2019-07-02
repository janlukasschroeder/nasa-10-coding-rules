# NASA's 10 Coding Rules

### 1 - Simple Control Flow
Keep it simple; don't use indirect recursion

### 2 - Fixed Upper Bound for Loops
All loops must have a fixed upper-bound. It should be possible for a verification tool to prove statically that a preset upper-bound on the number of iteration of a loop can’t be exceeded.
The rule is considered violated if the loop-bound can’t be proven statically.

### 3 – No Dynamic Memory Allocation
Do not use dynamic memory allocation after initialization.

### 4 – No Large Functions
No function should be longer than what could be printed on a single sheet of paper in a standard reference format with one line per declaration and one line per statement. This means a function shouldn’t have more than 60 lines of code.

### 5 - Low Assertion Density
The assertion density of the program should average to a minimum of two assertions per function. Assertions are used to check for abnormal conditions that should never happen in real-life executions. They should be defined as Boolean tests. When an assertion fails, an explicit recovery action should be taken.
If a static checking tool proves that assertion can never fail or never hold, the rule is considered violated.

### 6 – Declare Data Objects at Smallest Level of Scope
All data objects must be declared at the smallest possible level of scope.

### 7 – Check Parameters and Return Value
The return value(s) of a non-void functions should be checked by each calling function, and the validity of parameters should be checked inside each function.
In its strictest form, the rule means even the return value of printf statements and file close statements should be checked.

### 8 – Limited Use of Preprocessor
The use of the preprocessor should be limited to the inclusion of header files and macro definitions. Recursive macro calls, token pasting, and variable argument lists are not allowed. There should be justification for more than one or two conditional compilation directives even in large application development efforts, beyond the standard boilerplate, which avoids multiple inclusion of the same header file. Each such use must be flagged by a tool based checker and justified in the code.

### 9 – Limited Use of Pointers
The use of pointers must be restricted. No more than one level of dereferencing is permitted. Pointer dereference operations should not be hidden inside typedef declaration or macro definitions. Also, function pointers are not allowed.

### 10 – Compile all Code
All code must be compiled from the first day of development. The compiler warning must be enabled at the compiler’s most punctilious setting. The code must compile with these settings without any warning.
All code should be checked daily with at least one (preferably more than one) state-of-the-art static source code analyzer and should pass the analyses process with zero warning. 
