05-07-2025 22:56

Tags: [[C Sharp]] [[Programming Fundamentals]]

## Methods

A method in C# is a block of code declared inside of a class. It should perform a specific task. Methods help organize code, promote reuse, and encapsulate functionality.

### Basic Structure

``` csharp
<access_modifier> <return_type> <method_name>(<parameter_list>) {// method body }
```

- **Access Modifier**: Controls visibility (e.g., `public`, `private`)
    
- **Return Type**: The type of value the method returns (e.g., `int`, `string`, `void`)
  
	- Use a specific type (e.g., `int`, `string`) if you want to return a value.
	- Use `void` if the method does not return a value.
    
- **Method Name**: The name you use to call the method
    
- **Parameter List**: (Optional) Data passed into the method
    
- **Method Body**: The code to execute

**Ex.**
```csharp
public int Add(int a, int b) { return a + b; }
```

#### Summary

| Element         | Purpose                                 | Example                 |
| --------------- | --------------------------------------- | ----------------------- |
| Access Modifier | Controls visibility                     | `public`, `private`     |
| Return Type     | Type of value returned (`void` if none) | `int`, `string`, `void` |
| Method Name     | Identifier for the method               | `Add`, `PrintMessage`   |
| Parameters      | Data passed to the method               | `(int a, int b)`        |
## References



