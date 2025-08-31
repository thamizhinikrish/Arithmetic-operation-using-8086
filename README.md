# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|1200 12                  |1204 24                   |
 1201 34                   1205 68
 1202 12                   1206 00
 1203 34                   1207 C4
#### Manual Calculations
![WhatsApp Image 2025-08-31 at 22 31 06_a8346ce0](https://github.com/user-attachments/assets/88564205-151d-44aa-8363-195ae8e77b65)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-08-31 at 22 21 46_043e9091](https://github.com/user-attachments/assets/0d7d4840-60f4-4ba1-a98f-736935be2cdb)
![WhatsApp Image 2025-08-31 at 22 21 54_6ce04641](https://github.com/user-attachments/assets/a466694d-672d-4f94-a435-4f5e3066a53b)

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|1200 12                         |1204 00                         |
 1201 34                          1205 00
 1202 12                          1206 00
 1203 34                          1207 C4
#### Manual Calculations
![WhatsApp Image 2025-08-31 at 22 31 07_bdbb8c2c](https://github.com/user-attachments/assets/e098b4ae-8072-47c6-8515-d36a0336aa2c)

(Add your calculation here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-08-31 at 22 22 14_37bb185e](https://github.com/user-attachments/assets/1abcedbc-2fd0-45ab-bbc5-dccd83dc8793)
![WhatsApp Image 2025-08-31 at 22 22 15_0645b4f7](https://github.com/user-attachments/assets/0adc1ed4-bf82-4052-87cf-c0bf4c0e00bf)

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|1200 12                         |1204 44                          |
 1201 34                          1205 51
 1202 12                          1206 97
 1203 34                          1207 0A
#### Manual Calculations
![WhatsApp Image 2025-08-31 at 22 31 07_f92fd3d8](https://github.com/user-attachments/assets/4860485e-ac14-4b65-a9db-0f2216c3e98b)

(Add your calculation here)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-08-31 at 22 22 15_126492c3](https://github.com/user-attachments/assets/025b1b11-65e3-4a69-bde8-8572f8781cac)
![WhatsApp Image 2025-08-31 at 22 22 16_49cb9443](https://github.com/user-attachments/assets/214f74b7-0cdc-4d9e-a9d1-14c761c79e6c)

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|1200 12                        |1204 01                         |
 1201 34                         1205 00
 1202 12                         1206 00
 1203 34                         1207 00
#### Manual Calculations
![WhatsApp Image 2025-08-31 at 22 31 08_f53eeda4](https://github.com/user-attachments/assets/1ad3bae2-817d-4a89-a2d8-b47bde1cb0c2)

(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-08-31 at 22 22 17_7c19d058](https://github.com/user-attachments/assets/75e40739-7b0b-4bfc-9b6f-d2afa2564549)
![WhatsApp Image 2025-08-31 at 22 22 16_fc88566d](https://github.com/user-attachments/assets/dd68e84a-cab9-419a-a5be-e4cd6cb3bcac)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
