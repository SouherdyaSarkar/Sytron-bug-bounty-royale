# Bug Bounty Royale – Final (C)

Below are 5 codeblocks. Each contains hidden bugs.  
Your task:  
1. Identify and fix the bug(s).  
2. Run the corrected code.  
3. Submit the **final correct output**.  

---

## Q1.  
The following program mixes pre/post increment operations.  
What will be the final values of `a` and `b` when fixed?

```c
#include <stdio.h>

int main() {
    int a = 5;
    int b = a++ + ++a * 2 - --a;
    printf("%d %d\n", a, b);
    return 0;
}
```

## Q2.
This recursive Fibonacci function is intended to also count how many times it was called.
Fix the logic so both Fibonacci result and call count display correctly, answer what the calls count will be.

```c
#include <stdio.h>

int fib(int n) {
    static int calls = 0;
    calls++;
    if (n <= 1)
        return n;
    return fib(n-1) + fib(n-2);
    printf("Function called %d times\n", calls);
}

int main() {
    int result = fib(5);
    printf("Fibonacci(5): %d\n", result);
    return 0;
}
```

## Q3.  
The following program intends to print the squares of numbers in an array.  
Fix the logic so that the correct squares are printed.

```c
#include <stdio.h>

int main() {
    int arr[3] = {0, 1, 2};
    int *p = arr;
    for(int i=0; i<=3; i++) {
        printf("%d ", *(p+i) * *(p+i));
    }
    return 0;
}

```
