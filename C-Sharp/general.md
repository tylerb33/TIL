### General Notes###

- C# is strongly typed, but implicit types can be used if you explicitly use 'var = "this is a string"', it's able to reason that it's a string. 
- must use double quotes for strings

- there are many numeric types:
	INTEGER 
		- if you use ```int```, it can hold smaller numbers but can also handle negatives. 
		- if you use ```uint``` then it can hold larger numbers but no negatives.
		- ```short``` - short SmallerNumber = 5; (this is a 16 bit integer)
		- ```long``` - long LargerNumber = 34345455455455; (this holds a longer integer)
	
	FLOAT
		- assign by saying 'float pi = 3.14f'
			-  The extra 'f' at the end explicitly calls it a float.
			- The other option is ```double``` by using ```double pi2 = 3.14```
				- The double is able to handle larger floats.
	BOOLEAN
		- bool personalTruth = true;
		- var thisIsFalse = false;

***There are many more types including currency, etc.***


- If you type a period after a datatype, you'll see a list of possible methods to use. i.e. 'int.'

- Static properties and methods are those that are available on the class. For example, the integer class or math or string class.

- After instantiating a variable... there are more methods available on that variable. (Just type the variable name then a period)

**Constants**

- These are immutable, the advantage is that it doesn't take up any memory like a variable does
const float pi=3.14f;

enum weekDays { Monday, Tuesday, Wednesday, Thursday, Friday};
var someDay = weekDays.Monday;
- Enums are similar to arrays but they allow you to use the actual values to reference values instead of numbers (like array positions)

You could also assign the number values
enum weekDays { Monday = 1, Tuesday, Wednesday, Thursday, Friday};
// Now Monday is 1, Tuesday is 2, etc.

- Typing ```ctor``` then ```tab``` ```tab``` will make a constructor function for you in Visual Studio


**Function Bodied Expression**
New feature as of last release of C#.

public float AverageThreeScores(float a, float b, float c) => (a + b + c) / 3; // only use this in very simple methods.

**Static Methods**

- Add ```static``` to beginning of method. Makes it visible from other classes, and can be used without instantiation.

public static float AverageThreeScores (float a, float b, float c) {
	...code...
}



- Abstract class, required to be over written. For instance an abstract class could be 'people', and 'teacher' and 'student' could extend that abstract class.

- Extension methods - can extend the methods of an existing base class. Such as adding in a method to calculate word count



- A namespace is a collection of classes

- The Main method is the entry point for all C# programs. The Main method states what the class does when executed.

- All statements and expression must end with a semicolon (;)

- Console.ReadKey() - Obtains the next character or function key pressed by the user. The pressed key is displayed in the console window.

- Console.ReadLine() - gets input from user in console. Same as gets.chomp in Ruby


-string hello = @"Hello World";

The above '@' marks the string as a verbatim string literal - anything in the string that would normally be interpreted as an escape sequence is ignored.

**To initialize a class in C# with some parameters:**

Class:

``` using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Test
{
    public class Posicion
    {
        public int X { get; set; }
        public int Y { get; set; }
    }
} ```

The below would initialize a new instance with values for X & Y

button1.Tag = new Posicion() { X = 1, Y = 1 };


**Ternary operations are possible in C#**
```Exp1 ? Exp2 : Exp3;```
In the above, if Exp1 is true then Exp2 runs. If false, then Exp3 runs.


**Public Access Specifier**
Public access specifier allows a class to expose its member variables and member functions to other functions and objects. Any public member can be accessed from outside the class.

``` namespace RectangleApplication {
   class Rectangle {
      //member variables
      public double length;
      public double width;
      
      public double GetArea() {
         return length * width;
      }
      public void Display() {
         Console.WriteLine("Length: {0}", length);
         Console.WriteLine("Width: {0}", width);
         Console.WriteLine("Area: {0}", GetArea());
      }
   } ```



**Defining a method in C#**
``` <Access Specifier> <Return Type> <Method Name>(Parameter List) {
   Method Body
} ```


*Access Specifier* − This determines the visibility of a variable or a method from another class.

*Return type* − A method may return a value. The return type is the data type of the value the method returns. If the method is not returning any values, then the return type is void.

*Method name* − Method name is a unique identifier and it is case sensitive. It cannot be same as any other identifier declared in the class.

*Parameter list* − Enclosed between parentheses, the parameters are used to pass and receive data from a method. The parameter list refers to the type, order, and number of the parameters of a method. Parameters are optional; that is, a method may contain no parameters.

*Method body* − This contains the set of instructions needed to complete the required activity.

``` class NumberManipulator {

   public int FindMax(int num1, int num2) {
      /* local variable declaration */
      int result;

      if (num1 > num2)
         result = num1;
      else
         result = num2;

      return result;
   }
   ...
} ```


**Defining a structure**

```struct Books {
   public string title;
   public string author;
   public string subject;
   public int book_id;
};```


```public class testStructure {
   public static void Main(string[] args) {
      Books Book1;   /* Declare Book1 of type Book */
  
      /* book 1 specification */
      Book1.title = "C Programming";
      Book1.author = "Nuha Ali"; 
      Book1.subject = "C Programming Tutorial";
      Book1.book_id = 6495407;    

      /* print Book1 info */
      Console.WriteLine( "Book 1 title : {0}", Book1.title);
      Console.WriteLine("Book 1 author : {0}", Book1.author);
      Console.WriteLine("Book 1 subject : {0}", Book1.subject);
      Console.WriteLine("Book 1 book_id :{0}", Book1.book_id); 

      Console.ReadKey();
   }
}```


**Structure of a method**

```char myMethod(int a, string b, double c) 
{
  method contents...
}```

char = return type, if no return then it should be ```void```
myMethod = method name
int a... = argument list

*What is a method signature?*
It includes method name and argument list. There can never be two methods with the same signature.

*Overloading*
Mulitple methods of the same name, but with different number of arguments or arguments of different types.


- The 'out' keyword allows outputting of multiple values from a method.


**Variable and Refference Difference. A Short Story...**

For example, think of a variable as like a piece of paper. It could have the value "5" or "false" written on it, but it couldn't have my house... it would have to have directions to my house. Those directions are the equivalent of a reference. In particular, two people could have different pieces of paper containing the same directions to my house - and if one person followed those directions and painted my house red, then the second person would see that change too. If they both just had separate pictures of my house on the paper, then one person colouring their paper wouldn't change the other person's paper at all.



**Inheritance**

``` public class Student : Person ```
Student is inheriting from Person.

------------------------------------
```Virtual``` allows for the method to be overridden

```public virtual void SayHello()
{
  Console.WriteLine("Hello");
}```

Then the below would be able to override
```public override void SayHello()
{
  Console.WriteLine("Hi there");
}
```
------------------------------------

System.Object comes with many methods that can be overridden. 
```public override string ToString()
{
  return FirstName + " " + LastName + " " + Age;
}
```

**Interfaces**

Anatomy:
```public interface IMyInterface
{

}```
-Must start with 'I', these are always public.
-Methods doesn't have implementations.

**Composition vs. Inheritance**

Inheritance: "is a" relationship. So a student "is a" person. Inheritance overuse could lead to maintenance issues.

Composition: "has a relationship". Composition is made of other classes?

**Enums - Enumerations**
```
public enum MovieGenre
{
  Action,
  Comedy,
  Scifi,
  Horror
}
```


*Switch statements* are generally preferred over ifs, else ifs in C#.

**Structs**
-Somewhat similar to classes
-Values types, instead of reference types like classes
-No inheritance

**Generics**
An important and vital part of C#. They are algorithms and data structures that are created without knowing the exact data type they will be used with. They can work with any data type. Applies to methods and classes.

```< >``` is how they are defined
```System.Collections.Generic```

T represents an unknown type, if you see this in Visual Studio. It is not a keyword though. Using T is just a convention. Others may use ```type```.

static void Main(string[] args)
{
  List<string> games = new List<string>();
    games.Add("Mass Effect");
    games.Add("Bioshock");
    games.Add("Prey");

    foreach (string game in games)
    {
      Console.WriteLine(game);
    }

    List<int> randomNumbers = new List<int>();

    Random r = new Random();
    randomNumbers.Add(r.Next(1, 10));
    randomNumbers.Add(r.Next(1, 10));
    randomNumbers.Add(r.Next(1, 10));

    foreach (int n in randomNumbers)
    {
      Console.Write("{0} ", n);
    }
}

**Type Checking**
*'Is' operator* - returns a true or false
*'As' operator* - converts a variable to a certain type. If types are incompatible, 'as' returns 'null'


**Garbage Collection**
-This removes unneeded objects from memory so that you don't have to.

-As long as there's an active reference to an object, the object remains. Once that active reference goes away then the object is garbage collected.

-```System.GC.Collect()``` - forces garbage collection, but is rarely used



























