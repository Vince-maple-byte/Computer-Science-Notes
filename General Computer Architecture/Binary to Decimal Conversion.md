**Binary to decimal conversion:**
To do this we simply start from the right hand side and if the first number is equal to a 1 we do 2<sup>0</sup> and save the value, and if the next number is a 0 we simply save the value 0. We continue doing this for each of the numbers with the 2<sup>n</sup> for n being the positing of the number - 1
*Example:* 
1001 -> 2<sup>3</sup> 0 0 2<sup>0</sup> 
			 8 0 0 1

Finally we just add up all of the numbers from what we saved, and the decimal representation of that binary number would appear.

1001 -> 2^3 0 0 2^0 
			 8 0 0 1
			 8 + 0 + 0 + 1
			 9
So the binary 1001 is equal to 9 
#bit #binary #computerorganization #computersciencemath 