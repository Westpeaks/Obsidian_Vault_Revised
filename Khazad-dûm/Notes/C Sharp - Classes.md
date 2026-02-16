05-02-2025 12:39

Tags: [[C Sharp]] [[Programming Fundamentals]]

## Classes

- Classes are a blueprint for creating objects It defines the data that will be contained within the class. Fields and properties will represent data and methods (functions) will represent behavior. 
- Classes help to organize code by creating a hierarchy for data and methods. Related data an methods will exist within the same class. 
- Declare a class when creating a model to represent a real world entity (**Ex.** car, user).
- Use a class when you want encapsulate related data and operate on that data with a method or methods. 

#### An example of a class

``` csharp
public class Car
{
    public string color;
    public void Drive() { /* ... */ }
}
```

### Public vs. Internal vs. Private

- Classes by default (meaning not declared as public) are given internal access. This means that they can be accessed within the same assembly. 
- Public classes are accessible from any other code. Use `public` when you want other classes or code to be able to create instances of the class or access its members.
- `private` is only used by members (data or methods) of a class. This means the member is only accessible within the same class. Use `private` to hide implementation details and protect data from being accessed or modified directly from outside the class.

#### Summary Table

| Access Modifier | Where to Use           | Visibility                          | Typical Use Case            |
| --------------- | ---------------------- | ----------------------------------- | --------------------------- |
| public          | Class, member          | Anywhere (all classes)              | Expose functionality/data   |
| private         | Member (field, method) | Only within the same class          | Hide implementation details |
| (none)          | Class                  | Internal (same assembly by default) | Library/internal code       |

## References

[C# Access Modifiers](https://www.w3schools.com/cs/cs_access_modifiers.php)

