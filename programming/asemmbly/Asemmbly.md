# 🧠 x86 / x86-64 Assembly — **Complete Practical Instruction Set**

---

## 1️⃣ Data Transfer

| Instruction             | Operands   | Description         |
| ----------------------- | ---------- | ------------------- |
| MOV                     | dst, src   | Copy value          |
| MOVZX                   | dst, src   | Zero-extend         |
| MOVSX                   | dst, src   | Sign-extend         |
| MOVSXD                  | r64, r/m32 | Sign-extend 32→64   |
| LEA                     | dst, mem   | Address calculation |
| XCHG                    | a, b       | Swap                |
| PUSH                    | src        | Push to stack       |
| POP                     | dst        | Pop from stack      |
| PUSHF / PUSHFD / PUSHFQ | —          | Push FLAGS          |
| POPF / POPFD / POPFQ    | —          | Pop FLAGS           |

---

## 2️⃣ Integer Arithmetic

| Instruction | Description          |
| ----------- | -------------------- |
| ADD         | Add                  |
| SUB         | Subtract             |
| INC         | Increment            |
| DEC         | Decrement            |
| MUL         | Unsigned multiply    |
| IMUL        | Signed multiply      |
| DIV         | Unsigned divide      |
| IDIV        | Signed divide        |
| NEG         | Two’s complement     |
| ADC         | Add with carry       |
| SBB         | Subtract with borrow |

---

## 3️⃣ Floating-Point Arithmetic (SSE)

| Instruction     | Description     |
| --------------- | --------------- |
| ADDSS / ADDSD   | Scalar add      |
| SUBSS / SUBSD   | Scalar subtract |
| MULSS / MULSD   | Scalar multiply |
| DIVSS / DIVSD   | Scalar divide   |
| SQRTSS / SQRTSD | Square root     |
| MAXSS / MAXSD   | Maximum         |
| MINSS / MINSD   | Minimum         |

---

## 4️⃣ Logical / Bitwise

| Instruction          | Description   |
| -------------------- | ------------- |
| AND                  | Bitwise AND   |
| OR                   | Bitwise OR    |
| XOR                  | Bitwise XOR   |
| NOT                  | Bitwise NOT   |
| TEST                 | AND for flags |
| BT / BTS / BTR / BTC | Bit test      |

---

## 5️⃣ Shift & Rotate

| Instruction | Description            |
| ----------- | ---------------------- |
| SHL / SAL   | Shift left             |
| SHR         | Logical shift right    |
| SAR         | Arithmetic shift right |
| ROL         | Rotate left            |
| ROR         | Rotate right           |
| RCL         | Rotate through carry   |
| RCR         | Rotate through carry   |

---

## 6️⃣ Comparison & Conditional

| Instruction | Description           |
| ----------- | --------------------- |
| CMP         | Compare               |
| SETcc       | Set byte if condition |
| CMOVcc      | Conditional move      |

---

## 7️⃣ Control Flow

| Instruction | Description        |
| ----------- | ------------------ |
| JMP         | Unconditional jump |
| JE / JZ     | Equal              |
| JNE / JNZ   | Not equal          |
| JG / JL     | Signed             |
| JA / JB     | Unsigned           |
| CALL        | Call               |
| RET         | Return             |
| LOOP        | Decrement RCX loop |

---

## 8️⃣ Stack Frame

| Instruction    | Description         |
| -------------- | ------------------- |
| ENTER          | Create stack frame  |
| LEAVE          | Destroy stack frame |
| PUSHA / PUSHAD | Push all regs       |
| POPA / POPAD   | Pop all regs        |

---

## 9️⃣ String Instructions

| Instruction        | Description |
| ------------------ | ----------- |
| MOVSB/W/D/Q        | Copy        |
| LODSB/W/D/Q        | Load        |
| STOSB/W/D/Q        | Store       |
| CMPSB/W/D/Q        | Compare     |
| SCASB/W/D/Q        | Scan        |
| REP / REPE / REPNE | Repeat      |

---

## 🔟 Sign Extension & Size Conversion

| Instruction | Effect        |
| ----------- | ------------- |
| CBW         | AL → AX       |
| CWDE        | AX → EAX      |
| CDQE        | EAX → RAX     |
| CWD         | AX → DX:AX    |
| CDQ         | EAX → EDX:EAX |
| CQO         | RAX → RDX:RAX |

---

## 1️⃣1️⃣ x87 Floating Point

| Instruction | Description   |
| ----------- | ------------- |
| FLD         | Load float    |
| FSTP        | Store float   |
| FADD        | Add           |
| FSUB        | Subtract      |
| FMUL        | Multiply      |
| FDIV        | Divide        |
| FSIN / FCOS | Trig          |
| FILD        | Load integer  |
| FISTP       | Store integer |

---

## 1️⃣2️⃣ SIMD Packed (SSE)

| Instruction     | Description     |
| --------------- | --------------- |
| MOVSS / MOVSD   | Scalar move     |
| MOVAPS / MOVUPS | Packed move     |
| ADDPS / ADDPD   | Packed add      |
| SUBPS / SUBPD   | Packed subtract |
| MULPS / MULPD   | Packed multiply |
| DIVPS / DIVPD   | Packed divide   |

---

## 1️⃣3️⃣ Bit Scan & Count

| Instruction | Description      |
| ----------- | ---------------- |
| BSF         | Bit scan forward |
| BSR         | Bit scan reverse |
| POPCNT      | Count bits       |
| TZCNT       | Trailing zeros   |
| LZCNT       | Leading zeros    |

---

## 1️⃣4️⃣ System / CPU Control

| Instruction | Description         |
| ----------- | ------------------- |
| NOP         | No operation        |
| PAUSE       | Spin-wait           |
| HLT         | Halt CPU            |
| INT imm     | Software interrupt  |
| SYSCALL     | System call         |
| SYSRET      | Return from syscall |
| MFENCE      | Memory fence        |
| LFENCE      | Load fence          |
| SFENCE      | Store fence         |
| LOCK        | Atomic prefix       |

---

## 1️⃣5️⃣ Registers (x86-64)

| Type  | Registers                       |
| ----- | ------------------------------- |
| GPR   | RAX RBX RCX RDX RSI RDI RBP RSP |
| IP    | RIP                             |
| FLAGS | RFLAGS                          |
| SIMD  | XMM0–XMM15                      |
| x87   | ST0–ST7                         |
