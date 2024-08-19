# IntroductionToOOP

# Procedural vs OOP Approach - Real-Life Example

## Procedural Style:

```csharp
class Program
{
    static void DisplayPersonDetails(string name, int age)
    {
        Console.WriteLine($"{name} is {age} years old.");
    }

    static void Main()
    {
        // Display details for brother
        DisplayPersonDetails("John", 25);
        // Output: John is 25 years old.

        // Display details for sister
        DisplayPersonDetails("Emily", 22);
        // Output: Emily is 22 years old.
    }
}
```

### Explanation:
In the procedural approach, we use a standalone function `DisplayPersonDetails` that takes a name and age as arguments. The focus here is on procedures or methods that manipulate the data, but the data (name and age) is not associated with any object. This style works for simple cases but can become harder to manage and scale as the system grows, especially when additional behaviors or attributes need to be added to the person.

## OOP Style:

```csharp
class Person
{
    private string name;
    private int age;

    public Person(string name, int age)
    {
        this.name = name;
        this.age = age;
    }

    public void DisplayDetails()
    {
        Console.WriteLine($"{name} is {age} years old.");
    }
}

class Program
{
    static void Main()
    {
        // Create a brother object
        Person brother = new Person("John", 25);
        brother.DisplayDetails();  // Output: John is 25 years old.

        // Create a sister object
        Person sister = new Person("Emily", 22);
        sister.DisplayDetails();  // Output: Emily is 22 years old.
    }
}
```

### Explanation:
In the OOP approach, the person is modeled as a class with attributes like name and age. The method `DisplayDetails` is encapsulated within the class, and the data (name and age) is tied to the `Person` object. This makes the code more modular and reusable, as the `Person` object holds both the data and behavior, aligning with real-world modeling. By grouping related data and functionality together, the OOP style makes it easier to manage and extend the system as it grows.
