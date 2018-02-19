### Regex

**Metacharacters in Regex**

*Single Characters*
\d -> 0-9
\D -> one character that is not a digit
\w -> A-Z a-z 0-9
\W -> anything NOT A-Z a-z 0-9
\s -> whitespace
\S -> anything NOT whitespace
. -> any character whatsoever

*Quantifiers*
Metacharacters that modify the previous character.
* -> 0 or more
+ -> 1 or more
? -> 0 or 1 (optional)
{min, max} -> range
{n} -> exactly n number of times

Example ```\w{5}``` all five letter combinations
Example ```colou?rs?``` c followed by o, l, o, u(optionally), r, s(optionally)

*Position*
^ -> start of string or start of line
$ -> end of string or line
\b -> word boundary
\z -> very end of string

*Character Classes*
[ ... ] -> one of the characters in the brackets
- -> range indicator

*More characters*
\. -> a period (special character needs to be escaped)
\ -> escapes a special character