# Word-Machine-System
A machine challenge on Codility done in python



A word machine is a system that performs a sequence of simple operations on a stack of integers. Initially the stack is empty. The sequence of operations is given as a string. Operations are separated by single spaces. 
The following operations may be specified: 
•	an integer X (from 0 to 220 - 1): the machine pushes X onto the stack; 
•	 "POP": the machine removes the topmost number from the stack; 
•	 "DUP": the machine pushes a duplicate of the topmost number onto the stack; 
•	 "+": the machine pops the two topmost elements from the stack, adds them together and pushes the sum onto the stack;
•	 "-": the machine pops the two topmost elements from the stack, subtracts the second one from the first (topmost) one and pushes the difference onto the stack. After processing all the operations, the machine returns the topmost value from the stack. 
The machine processes 20-bit unsigned integers (numbers from 0 to 220 - 1). An overflow in addition or underflow in subtraction causes an error. The machine also reports an error when it tries to perform an operation that expects more numbers on the stack than the stack actually contains. Also, if, after performing all the operations, the stack is empty, the machine reports an error. 
For example, given a string "13 DUP 4 POP 5 DUP + DUP + -", the machine performs the following operations:
 Operation        	                 comment 
| stack - - - - - - - - -------- [empty] 
"13"			 push 13 12
 "DUP"			 duplicate 13
 "4" 			push 4 
"POP"			 pop 4 
"5"				 push 5 
"DUP"			 duplicate 5 
"+" 				pop 5 and 5 then adding sum of the two to stack
"DUP" 			duplicate 10
        “+”				pop 10 and 10 adding sum of the two to stack
       “-“				pop 13 from 20 adding difference of the two to stack
       Finally, the machine will return 7.
 Given a string "5 6 + -", the machine reports an error, since, after the addition, there is only one number on the stack, but the subtraction operation expects two. 
Given a string "3 DUP 5 - -", the machine reports an error, since the second subtraction yields a negative result. Write a function: def solution (S) Chat, given a string S containing a sequence of operations for the word machine, returns the result the machine would return after processing the Operations. The function should return -1 if the machine would report an error.
 For example, given string S = "13 DUP 4 POP 5 DUP + DUP + - "the function should return 7, as explained in the example above.
 Given string S = "5 6 + -" or S = "3 DUP 5 - -" the function should return -1. 
Assume that: 
•	the length of S is within the range (0..2,000); 
•	Sis a valid sequence of word machine operations.

