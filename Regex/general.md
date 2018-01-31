### Regex

**Metacharacters in Regex**

*Single Characters*
\d -> 0-9
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
{n} -> need to read up on this one

Example ```\w{5}``` all five letter combinations
Example ```colou?rs?``` c followed by o, l, o, u(optionally), r, s(optionally)

*Position*
^ ->
$ -> end
\b -> word boundary