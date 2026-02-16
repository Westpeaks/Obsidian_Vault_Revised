05-07-2025 23:07

Tags: [[C Sharp]] [[Programming Fundamentals]]

## Purpose of Void Return Type

The `void` return type in C# is used to indicate that a method does not return any value to its caller. When you declare a method with `void`, you are telling the compiler and anyone reading your code that the method performs an action (like printing to the console, modifying an object, or triggering an event) but does not produce a result that can be used or stored.

**Ex.**

```csharp
public void PrintMessage(string message)
{
    Console.WriteLine(message);
}
```

- Use void when you want to perform an operation in a method, but not return a value. 
- Output (like writing to the console) is not the same as a return value-`void` methods can still perform visible actions, but nothing is returned to the caller.
- If a method needs to provide information back to the caller, use an appropriate return type instead (like `int`, `string`, etc).
## References


