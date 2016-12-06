# Now for some TDD on a funky calculation!

Let's assign a price for each symbol
	 
   
     Symbol 		I 		V 		X 		L
     Price 			1 	4.4 	8.4		39

Convert the number of days to its Roman Numerals-related price and add them together, except when there is subtractive notation (e.g. IV or IX), in which case we subtract the value. 
Replace NbDays by RomanPrice(NbDays) in calculation.

Examples
	  nBdays			(Numeral)			roman Price
	  1						I							1
	  3						III						3*1
	  4						IV						(4.4 - 1)
	  5						V							4.4
	  7						VII						4.4 + 2*1
	  9						IX						(8.4 - 1)
	  14					XIV						8.4 + (4.4 -1)
	  39					XXXIX					3*8.4 + (8.4 -1)
	  41					XLI						(39 - 8.4) +1
	  77 					LXXVII				39 + 2*8.4 + 4.4 + 2*1

**Enjoy your TDD!**
