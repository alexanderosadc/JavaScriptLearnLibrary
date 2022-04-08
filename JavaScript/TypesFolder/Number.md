- is a double precision 64-bit binary format IEEE 754 value (numbers between -(2^53 - 1) and 2^53 - 1)
- Has 3 symbolic values: **+Infinity**, **-Infinity**, **NaN**
* To detect larger amount in **+Infinity** is **Number.MAX_VALUE**
* To detect smallest avialiable value in **-Infinity** write **Number.MIN_VALUE**
* To check if number is in the double precision floating-point number range we will use **Number.isSafeInteger()** as well as **Number.MAX_SAFE_INTEGER** and **Number.MIN_SAFE_INTEGER**
	* Beyond this range numbers will be not safe anymore and will be a double-precision floating point approximation of the value.
* Has only one integer with 2 representations: **+0** and **-0**
[[ParsingNumber]]
