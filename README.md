# go-notation
Description of the notation for entities in the GoLang code.

***Note:***  
*This naming system is not a standard.*  
*This system is a kind of Hungarian notation and is convenient for its author, but you can also use it if you want.*  
*This notation makes the code more readable, which means it simplifies application development.*  
*The use of this notation is solely your choice.*  

***Warning:***  
*Using this notation in the early stages requires self-discipline from the developer.*  

## Application



## Basic data types

|Private|Public|Description|
|:-|:-|:-|
|b|B|byte|
|r|R|rune|
|s|S|string
|fl|Fl|float, float32, float64|
|i|I|int, int8, int16, int32, int64|
|u|U|uint, uint8, uint16, uint32, uint64|
|c|C|complex64, complex128|
|bi|Bi|BigInt|
|is|Is|bool|
|dt|Dt|Date and time|
|p|P|pointer|
|r|R|reference|

## Aggregate and other complex data types

|Private|Public|Description|
|:-|:-|:-|
|st|St|struct|
|in|In|interface|
|sl|Sl|slice|
|ar|Ar|array|
|m|M|map|

## Naming types

|Private|Public|Description|
|:-|:-|:-|
|t|T|for custom type|

## Code entities with a special purpose

|Private|Public|Description|
|:-|:-|:-|
|g|G|Global variables|
|cl|Cl|Closure variables|
|fn|Fn|Variables for storing functions and other higher-order operations|
|d|D|The difference between the values (delta)|

## Entities with a frequently used purpose

|Private|Public|Description|
|:-|:-|:-|
|f|F|for file descriptors|
|mx|Mx|mutex and other blocking|
|j|J|Encoded JSON in string|
|bs|Bs|Encoded base64 in string|

## A combination of prefixes

|Private|Public|Description|
|:-|:-|:-|
|slS|SlS|slice of string|
|slU|SlU|slice of uint|
|slB|SlB|slice of byte|
| | | |
|tSl|TSl|custom slice|
|tSt|TSt|custom struct|

## About the author

The author of the project is Constantine Zavezeon (Kwynto).  
You can contact the author by e-mail: kwynto@mail.ru  
The author accepts proposals for participation in open source projects,  
as well as willing to accept job offers.
If you want to offer me a job, then first I ask you to read [this](https://github.com/Kwynto/Kwynto/blob/main/offer.md).
