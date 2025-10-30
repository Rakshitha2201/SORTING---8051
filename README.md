
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

<img width="1917" height="1079" alt="Screenshot 2025-10-30 183915" src="https://github.com/user-attachments/assets/0d7dfc44-7f3d-4f9f-861b-0aa0410879c9" />


After execution: D:0x40H:

<img width="1919" height="1079" alt="Screenshot 2025-10-30 183955" src="https://github.com/user-attachments/assets/8c61cae7-bd47-4e16-bbc3-0b4f8119745c" />






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

<img width="1919" height="1079" alt="Screenshot 2025-10-03 093252" src="https://github.com/user-attachments/assets/c122135d-816f-4cb9-89ff-2ad27256e3cd" />  

After execution:
D:0x40H:  

<img width="1919" height="1079" alt="Screenshot 2025-10-03 093136" src="https://github.com/user-attachments/assets/1e8cc2c5-9a05-447c-9943-c0b06a25af71" />

**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

