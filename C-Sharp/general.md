### General Notes###

- C# is strongly typed, but implicit types can be used if you explicitly use 'var = "this is a string"', it's able to reason that it's a string. 
- must use double quotes for strings

-there are many numeric types:
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

Static properties and methods are those that are available on the class. For example, the integer class or math or string class.

After instantiating a variable... there are more methods available on that variable. (Just type the variable name then a period)

It's possible to use uppercase variable names (it's a crossover from Java).











