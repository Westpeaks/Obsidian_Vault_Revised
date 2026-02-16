03-17-2025 10:27

Tags: [[Tags/C Sharp]] [[Programming Fundamentals]]

## Decimal as a Data Type

Decimal is a data type used for storing floating point numbers with a high level of precision. 

- Great for financial and monetary calculations. 
- Helps to prevent error
- Contrary to integer or doubles on C#, decimal are designated by both their data type and the "m" after the decimal value is declared. 
  
```csharp
decimal salary = 500.24m;
```

- One major advantage of the decimal type in C# is that it allows for very precise arithmetic operations, particularly when working with large numbers. This is because decimals have a larger range and higher precision than float or double. This makes decimals an ideal choice for computations where precision is paramount, and even slightly off calculations may lead to significant errors.

## References

[[Variables in C Sharp]]

[[C Sharp Basic Commands, Vars, and Operators]]