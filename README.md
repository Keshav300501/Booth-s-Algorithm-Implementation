# Booth-s-Algorithm-Implementation
Implementation of booth's algorithm in python


ALGORITHM
*********
The first number is called as multiplicand and the second number is called as multiplier
Take the input of the numbers as integers and convert them to binary
If any(or both) number is negative find the 2's complement of the number
make the bits equal in the number
Initialize a bit with 0 (Qn)
Initialize accumulator with number of bits equal to maximum bits
If the last bit of multiplier is 0 and that of Qn is 1: add the multiplicand to accumulator and do a right shift
If the last bit of multiplier is 1 and that of Qn is 0: add the 2's complement of the multiplicand to accumulator and do the right shift
If the last bit of multiplier and Qn is either 0,0 or 1,1: do a right shift
Decrease the counter by 1
Continue till the counter is 0
Combine the result of Accumulator and multiplier and print the result
convert the result to decimal (if needed)

CODE
****
The code implements the above algorithm sequentially. The code is implemented in python

INPUT
*****
The 2 number of which we need to find the product

OUTPUT
******
The product of 2 numbers in binary(signed bit representation) and decimal representation

CODE DOCUMENTATION
******************

DATA VARIABLES:

1. multiplicant : Data type-List	stores the binary of multiplicant
2. multiplier	: Data type-List	stores the binary of multiplier
3. Acc 			: Data type-List	stores the accumulator contents
4. cycleCount 	: Data type-Int		stores the number of cycles that need to be performed


FUNCTIONS/METHODS (in order of appearance in code)

1. setCycleCount() : sets the cycleCount to maximum bits

2. setAccumalator() : sets the accumulator content to 0

3. addBin(a,b) : adds 2 binary bits a and b

4. add3Bin(a,b,c) : adds 3 binary bits a, b and c

5. get2Complement(list) : return the 2's complement of list of binary bits

6. getBinary(num) : return the binary of a number num as a list

7. addTwoBinaryList(list1,list2) : adds 2 binary lists list1 and list2

8. getNumber() : function to take input and convert to binary. It also calls the function get2Complement(list) to find the 2's complement of the negative 					 numbers if necessary.  

9. arithmeticShiftRight() : function to perform arithmetic shift right on the list Accumulator, multiplier and integer Qn

10. getNumberFromBinaryList(list) : function to get an integral number from a list containing binary bits

11. convertToStr(list) : function to convert a string to list

12. BoothAlgorithm() : main function which is called to find the product of 2 numbers using booth's algorithm. The function implements the above algorithm and 						  displays the result. Also, it stores the result in a file named result.txt
