Before we start with bitwise operators we need to understand a bit.

A bit is the single 1 and 0 value in [[Binary]]
Bits are used in computers to understand data in the smallest level. Meaning that everything from a String to a number is going to be transformed into a bit in order for the computer to understand the information.

Here is a chart of all of the bitwise operators
![[Pasted image 20231113161026.png]]
*bitwise AND:* 
AND is returns a 1 if both the of bits that we give to it are equal to 1 else it will return a 0
example 1001
	  AND 1110
   result 1000

*bitwise OR:* 
OR is returns a 1 if both or either of them are 1 else a 0
example 1001
	  AND 1110
    result 1111

*bitwise XOR:* 
XOR is returns a 1 if only one of the bits is a 1 else returns a 0
example 1001
	  AND 1110
    result 0111

*bitwise NOT:* 
NOT give the opposite values for the bits passed on
example 
	  NOT 1110
   result 0001

*bitwise shift left:* 
Shift left would take the bits that we already have and move them to the left by n and would add 0s following it. Example 1001 << 2 = 100100
Shift left can be thought of as multiplying by 2
So x << n would be the same as x $\times$ 2<sup>n</sup> 
Example of doing x $\times$ 18 = (x << 4) + (x << 1)

*bitwise shift right:*
Shift right is similar to shift left but instead of moving the bits to the left we are moving them to the right. Example 1001 >> 2 = 10
So x >> n would be the same as x $\div$ 18 = (x >> 4) + (x >> 1)
*Be aware in most programming languages the >> would keep in track of the sign bit so -9 >> 2 = -3 while >>> would not keep track of the sign bit so -9 >>> 2 = 1073741821*

#bit #computersciencemath #computerorganization 