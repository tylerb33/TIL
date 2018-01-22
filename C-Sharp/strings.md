### Strings

var testString = " abCDefg  ";
testString.Trim() // would return "abCDefg". There's also TrimStart and TrimEnd

testString.ToUpper()
testString.ToLower()

var dickens = "It was the best of times, it was the worst of times.";

dickens.Substring(4, 8); // returns "as the b"

dickens.Length(); // returns 46


var challenge = "  Text processing in C# is really great!  ";

challenge.Trim().Substring(24, challenge.Trim().Length - 25).ToUpper().Trim() // returns "REALLY GREAT"

String concatenation is the same as Javascript with:
var stringOne = "Hello ";
var stringTwo = "I love you ";
var stringThree = "Won't you tell me your name?";

stringOne + stringTwo + stringThree;

But there is also ```StringBuilder``` to use in C#.

var sb = newStringBuilder();
sb.AppendLine("It was the best of times, it was the worst of times");
sb.AppendLine("it was the age of wisdom");
sb.AppendLine("it was the age of foolishness");
sb.ToString()

ToString() is on virtually every object in C#. It is a  way to get some meaningful string from an object.




## String Formatter in C# ##

var city = "Dallas";
var temperature = 103.4f;
var currentDt = DateTime.Now;

string.Format("Welcome to {0}. The time is {1}. The temperature is {2}.", city, currentDt, temperature)


would return  // "Welcome to Dallas. The time is 10/18/2017 12:55:11 PM. The temperature is 103.4."

string.Format("Welcome to {0}. The time is {1:t}. The temperature is {2:0.00}.", city, currentDt, temperature)

temperature = 1000.25f;


string.Format("Welcome to {0}. The time is {1:T}. The temperature is {2:0,0.00}.", city, currentDt, temperature)

would return  // "Welcome to Dallas. The time is 12:55:11 PM. The temperature is 1,000.25"

*Parse string to integer*

int.Parse("15") // will return the integer 15

int.Parse("15,234") // this will not work because you need to remove the comma... see below:
var number = "15,234";
int.Parse(test.Replace(",", "")) // returns integer 15234

*TryParse*
int result;
int.TryParse("15,234", out ```result```) // returns ```false``` because there's a comma in the string

int.TryParse("15234", out ```result```) // returns true, and now ```result``` is set to the integer 15234.































