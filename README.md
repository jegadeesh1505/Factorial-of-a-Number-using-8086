# Factorial-of-a-Number-using-8086
8086 assembly language projects developed and debugged using DOSBox

# Aim:
To write and execute Assembly Language Programs to perform factorial  of given number for the 8086 microprocessor.

# Software required:
* Personal Computer with MASM Software

# Algorithm:

1. **Start** the program and initialize the data segment.
2. **Load** the input number from memory into a register.
3. **Set** the accumulator to 1 to store the factorial result.
4. **Repeat multiplication** of the accumulator by the number, decrementing the number each time until it becomes 1.
5. **Store and display** the final factorial result, then **end** the program.

# Program:

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV SI, 2000H
MOV AL, [SI]
MOV BL, AL
MOV AX, 0001H
CMP BL, 01H
JE STORE
MUL BL
DEC BL
JMP FACTL
MOV [SI+02H], AX
MOV DX, 0000H
MOV [SI+04H], DX
MOV AH, 4CH
INT 21H
CODE ENDS

```


# Manual calculation:

* 4! = 4*3*2*1 = 120
 * 120 in hec = 18

# Output:

<img width="735" height="396" alt="Screenshot 2025-10-24 184403" src="https://github.com/user-attachments/assets/337d17c3-46a8-4287-92c5-d1124acf99be" />


# Result:
Thus, the Assembly Language Programs for 8086 to perform addition of 5 numbers was successfully written and executed using MASM.
