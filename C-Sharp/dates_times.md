### Dates and Times

DateTime.Now // returns the current date and time
var birthday = new DateTime(1998, 5, 12);
The date/time object will be built for my birthday.

var difference = DateTime.Now - birthday; // This returns a timespan object.

difference.Days // will return the # of days I've been alive

The below values are (Year, Month, Day, Hour, Minute, Second)
var someTime = new DateTime(2017, 10, 18, 9, 51, 32)

someTime.AddMinutes(134)
This returns what time it will be 134 minutes in the future. Passing in a negative value to AddMinutes will show time in the past.

DateTime Object has its own formatting included. They include ToLocalTime, ToFileTime, ToLongDateString() and more.

