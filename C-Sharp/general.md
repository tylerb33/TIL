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

*Constants*

- These are immutable, the advantage is that it doesn't take up any memory like a variable does
const float pi=3.14f;

enum weekDays { Monday, Tuesday, Wednesday, Thursday, Friday};
var someDay = weekDays.Monday;
- Enums are similar to arrays but they allow you to use the actual values to reference values instead of numbers (like array positions)

You could also assign the number values
enum weekDays { Monday = 1, Tuesday, Wednesday, Thursday, Friday};
// Now Monday is 1, Tuesday is 2, etc.

- Typing ```ctor``` then ```tab``` ```tab``` will make a constructor function for you in Visual Studio


*Function Bodied Expression*
New feature as of last release of C#.

public float AverageThreeScores(float a, float b, float c) => (a + b + c) / 3; // only use this in very simple methods.

*Static Methods*

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

















