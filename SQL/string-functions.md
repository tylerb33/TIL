## String Functions


### LENGTH
* SELECT LENGTH('string'); returns 6


* SELECT Name, LENGTH(Name) FROM City; returns city names and length of their names


### SUBSTR
* SELECT SUBSTR('this string', 6); returns name 'string'. This starts at the 6th position and goes till the end.

	- SELECT released,
			SUBSTR(released, 1, 4) AS year,
			SUBSTR(released, 6, 2) AS month,
			SUBSTR(released, 9, 2) AS day
		FROM album
		ORDER BY released
	;

	The above is looking at the album table, the released column. It is extracting out the year, month and day from this column and and breaking them out into 3 columns separately.

### TRIM
* SELECT '    string    '; returns just 'string', trimming off extra spaces

	- There is also an LTRIM and RTRIM to trim just one side

* SELECT TRIM ('...string...', '.'); returns 'string', filtering out '.'

### UPPER / LOWER
* SELECT UPPER(NAME) FROM City; returns upper case of all city names

