04-01-2025 16:05

Tags: [[C Sharp]] [[Programming Fundamentals]]

## Scope

- Scope is determined by indent and curly brackets in C Sharp. The deepest level of scope is the deepest indent. So, variables can be used in further indention levels. However, you cannot use a variable from inward indentions outward.  
- Variables that need to be accessed by multiple methods will need to be declared on the class level (outside the methods). Also, the static property can cause issue. Static methods can only access static variables from outside the method. Non static methods can access static and non static attributes. 
- Variables can be overridden in further indentations (inside a method). However, this can become confusing when deciphering code. In any case, where possible, separate naming conventions should be adhered to.
- Variables declared at the class level should follow the pascal case naming convention. Variables declared at the method level should follow camel case.

### Variable Scope

- When you declare a variable inside a code block, its visibility is local to that code block and that variable cannot be accessed outside of the code block.
- To ensure that a variable is visible both inside and outside of a code block, you must declare the variable prior to the code block (outside and above the code block).
- Ensure that variables are initialized before your code attempts to access them (for all potential code execution paths).

**Example of scope in code**

```c sharp
# vars are declared outside of methods as they will be iterated on by multiple methods

int[] numbers = { 4, 8, 15, 16, 23, 42 };
int total = 0;
bool found = false;
  
foreach (int number in numbers)
{
	total += number;
	
	if (number == 42)
	{
		found = true;
	}
}

if (found)
{
	Console.WriteLine("Set contains 42");
}

Console.WriteLine($"Total: {total}");
```

## References

[Exercise - Code blocks and variable scope](https://learn.microsoft.com/en-us/training/modules/csharp-code-blocks/2-exercise-variable-scope)

[Pascal Case vs. Camel Case](https://builtin.com/articles/pascal-case-vs-camel-case)

