
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H 

MOV R6,#04

LOOP: MOV A,@R0 

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT 

SJMP DOWN 

NEXT:JNC DOWN 

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END


**OUTPUT:**

**MEMORY WINDOW:**

Before execution: D:0x40H:

<img width="953" height="281" alt="Screenshot 2025-10-23 110404" src="https://github.com/user-attachments/assets/6c132e73-52bd-493f-b552-3cc7bd52251f" />

<BR>
<BR>
<BR>
After execution: D:0x40H:

<img width="959" height="298" alt="Screenshot 2025-10-23 110423" src="https://github.com/user-attachments/assets/60987756-a059-43b3-9e1b-930f17184647" />

<BR>
<BR>
<BR>


**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H

MOV R6,#04

LOOP: MOV A,@R0

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT

SJMP DOWN 

NEXT:JC DOWN

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END

**OUTPUT:**

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:

<img width="959" height="271" alt="Screenshot 2025-10-23 110018" src="https://github.com/user-attachments/assets/a584fc52-543e-4482-9433-5390ce423141" />

<BR>
<BR>
<BR>
<BR>
After execution:
D:0x40H:

<img width="961" height="274" alt="Screenshot 2025-10-23 110030" src="https://github.com/user-attachments/assets/76cf0861-82f6-47ae-9a45-057b73c863b8" />

<BR>
<BR>
<BR>
**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

