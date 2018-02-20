**C# 7 Additions**

*Tuples*
-Allows returning multiple values from methods.

var car = getCar();
Console.WriteLine($"Model: {car.Model}")
Console.WriteLine($"Price: {car.Price}")
Console.WriteLine($"Currency: {car.Currency}")

```
private static (string Model, double Price, string Currency) getCar()
{
	return ("Tesla Model S", 75000, "USD");
}
```

-Deconstruction
(string model, double price, string currency) = getCar();

*Pattern Matching*
- A pattern shows the type of variable.
'Type value'

If the variable in question matches 'Type' it will be converted to a variable 'value' of type Type.

-Patterns and switch statements
Able to use switch statements to see the type of variables. So it could be a switch statement saying "if ExampleA 'is a' Person.Athlete do this. If ExampleA 'is a' Person.Chef do this. If ExampleA 'is a' Person, do this."