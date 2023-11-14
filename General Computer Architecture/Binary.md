Binary is a 2 base numerical system.

Binary is represented with the two numbers of 0 and 1.

The way these numbers would be shown are 1001

However if we want to see how binary relates to decimal we need to do some math to convert a binary number such as 1001 to a decimal number.

**Binary to decimal conversion:**
To do this we simply start from the right hand side and if the first number is equal to a 1 we do 2<sup>0</sup> and save the value, and if the next number is a 0 we simply save the value 0. We continue doing this for each of the numbers with the 2<sup>n</sup> for n being the positing of the number - 1
*Example:* 
1001 -> 2<sup>3</sup> 0 0 2<sup>0</sup> 
			 8 0 0 1

Finally we just add up all of the numbers from what we saved, and the demical representation of that binary number would appear.

1001 -> 2<sup>3</sup> 0 0 2<sup>0</sup> 
			 8 0 0 1
			 8 + 0 + 0 + 1
			 9
So the binary 1001 is equal to 9 

Here is a chart of binary, decimal, and hex values
![[Pasted image 20231113153520.png]]

**Decimal to binary conversion:** 
This can be down by simply dividing the decimal number by 2 and saving the remainder. We then take the result and divide it again and save the remainder. We keep on doing this until we reach 0.
*Example:* 
14 -> 14 / 2 = 7 remainder = 0
			7/2 = 3 remainder = 1
			3/2 = 1 remainder = 1
			1/2 = 0 remainder = 1
			0 We stop here
After this the top to bottom remainders would be represented as right to left in binary. 
That's how we get the binary from a decimal.

#bit #computersciencemath #binary #computerorganization 
