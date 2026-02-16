03-26-2025 22:29

Tags: [[Tags/C Sharp]] [[Programming Fundamentals]] [[C Sharp Methods]]

### Take a look at the following code:

```csharp
using System;
using System.Collections.Generic;

namespace Coding.Exercise
{
    public class Exercise
    {
        public void RunExercise()
        {
            List<int> myNumberList = new List<int>()
            {
                2, 3, 5, 6, 7, 9, 10, 123, 324, 54
            };
            
            foreach (int number in myNumberList)
            {
                PrintIfOdd(number);
            }
        }

        public void PrintIfOdd(int number) // Corrected method signature
        {
            if (number % 2 != 0) // Check if the number is odd
            {
                Console.WriteLine(number); // Print the odd number
            }
        }
    }
}
```

- Both methods must declare public and void. 
- The second method must also pass in an integer to make sure the the passed values from the first method are consistent. 
- When dealing with methods in C Sharp, values and method assignments are not assumed as in other languages. They must be declared with each new method in order that data types are maintained and the code will compile. 
- Not maintaining these will result in errors when the code attempts to run.

## References

[[C Sharp Basic Commands, Vars, and Operators]]