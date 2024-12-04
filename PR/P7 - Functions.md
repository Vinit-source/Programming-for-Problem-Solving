
## Write C programs to demonstrate the use of functions in C.

### Aim
To write C programs to demonstrate the use of functions in C.

### Example Problem
**Problem Statement:** Write functions for addition, subtraction, multiplication, division, and a user-defined function to print the results in a specific format. Use these functions to solve the expression `((a + b) * (c - d)) / e`, where `a`, `b`, `c`, `d`, and `e` are provided by the user. Display each intermediate step in a specific format using the user-defined print function.

### Algorithm
1. Start the program.
2. Declare functions for addition, subtraction, multiplication, and division.
3. In the main function, take input for `a`, `b`, `c`, `d`, and `e` from the user.
4. Call the functions to solve `a + b`, `c - d`, and `(a + b) * (c - d)`.
5. Use the division function to calculate the final result by dividing the intermediate product by `e`.
6. Print each intermediate result and the final result in a formatted manner.
7. End the program.

### Flowchart
```mermaid
graph TD;

subgraph "add(x, y)" 
	addStart([Start]);
	B1([Return x + y]);
	addStart --> B1;
end
subgraph "subtract(x, y)"
	subStart([Start]);
	B2([Return x - y]);
	subStart --> B2;
end
subgraph "multiply(x, y)"
	mulStart([Start]);
	B3([Return x * y]);
	mulStart --> B3;
end
subgraph "divide(x, y)"
	divStart([Start]);
	J{Is y != 0?};
    J -- Yes --> K([Return x / y]);
    J -- No --> M[/Print 'Division by zero error'/];
    divStart --> J;
    M --> MR([Return 0]);
end
subgraph "printResult(operation, result)"
	printStart([Start]);
	P[/Print formatted 'operation = result'/];
	R([Return]);
	printStart --> P;
	P --> R;
end

CS2((C1));
CE2((C2));
CAS1((C1));
CSS1((C1));
CMS1((C1));
CDS1((C1));
CAE1((C2));
CSE1((C2));
CME1((C2));
CDE1((C2));
CS2 --> printStart;
R --> CE2;

subgraph main
    A([Start]) --> B[Declare functions for addition, subtraction, multiplication, division];
    B --> BB[Declare a, b, c, d, e, sum, diff, product, finalResult];
    BB --> C[/Input values for a, b, c, d, e from user/];
	C --> CB[["sum = add(a, b)"]];
	CB --> addStart;
	B1 --> E[["printResult('a + b', sum)"]];
    E --> CAS1;
    CAS1 -.-> CAE1;
    CAE1 --> F[["diff = subtract(c, d)"]];
    F --> subStart;
    B2 --> G[["printResult('c - d', diff)"]];
    G --> CSS1;
    CSS1 -.-> CSE1;
    CSE1 --> H[["product = multiply(sum, diff)"]];
    H --> mulStart;
    B3 --> I[["printResult('(a + b) * (c - d)', product)"]];
    I --> CMS1;
    CMS1 -.-> CME1;
    CME1 --> DB0{Is e != 0?};
    DB0 -- Yes --> I1[["finalResult = divide(product, e)"]];
    I1 --> divStart;
    K --> L[["printResult('(a + b) * (c - d) / e', finalResult)"]];
    L --> CDS1;
    CDS1 -.-> CDE1;
    CDE1 --> N([Stop]);
    DB0 -- No --> N0[/"Print 'Division by zero Error'"/];
    N0 --> N
   end
```
- **Details:** The flowchart illustrates the steps of calculating intermediate results using individual arithmetic functions and printing the final result.


### Suggested Programs (2 of 5)
1. Create a function in C to calculate the factorial of a given number and display the result. (Mandatory)
2. Write a program to create functions for calculating the power of a number using a loop.
3. Write a function to find the maximum and minimum of three given numbers.
5. Write a function to calculate the sum of an array of numbers and display the average.

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQ0MDk1MTY2Ml19
-->