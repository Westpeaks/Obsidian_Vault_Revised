03-11-2025 16:33

Tags: [[Programming Fundamentals]] [[Tags/C Sharp]]

## Breakdown of Variables - C Sharp

- Variable is a named storage location in memory within an executable program in C#. It is broken down into 3 parts. 
	- Name
	- Data type (e.g. System identifier or alias: **int, string, bool**)
	- Value
- Values that are not assigned will have a default. 
#### Ex.
```csharp
int number; // Default: 0
bool isActive; // Default: false
string text; // Default: null
```

- Variables within C# are static, meaning the variable datatype cannot be changed. 
- Values of variables can be changed, unless designated as **readonly** or **const**. 
### Declaration

- Variables are declared in the following order:
	```dataType variableName = value;```

## Variable Scope

A variables scope determines where it can be accessed. 

| Scope              | Description                                                                       |
| ------------------ | --------------------------------------------------------------------------------- |
| **Local**          | Declared inside a method (function) or block; accessible only within that block.  |
| **Instance/Field** | Declared at the class level; accessible to all methods in the class (non-static). |
| **Static**         | Declared with the `static` keyword; shared across all instances of the class.     |

#### Ex. 
```csharp
class Example {
    int instanceVariable = 10; // Instance variable
    static int staticVariable = 20; // Static variable

    void Method() {
        int localVariable = 30; // Local variable
    }
}
```

## References
