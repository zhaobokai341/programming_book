# x86 / x86-64 Assembly – Ultimate Cheat Sheet

---

## **1. Data Transfer**

| Instruction               | Operands       | Description                        | Effect / Return            |
| ------------------------- | -------------- | ---------------------------------- | -------------------------- |
| `MOV`                     | `dst, src`     | Copy value                         | `dst = src`                |
| `MOVZX`                   | `dst, src`     | Move with zero extension           | Zero-extended value        |
| `MOVSX`                   | `dst, src`     | Move with sign extension           | Sign-extended value        |
| `XCHG`                    | `op1, op2`     | Swap values                        | Values exchanged           |
| `LEA`                     | `dst, mem`     | Load effective address             | Address computed only      |
| `PUSH`                    | `src`          | Push value onto stack              | `RSP -= size`              |
| `POP`                     | `dst`          | Pop value from stack               | `dst = [RSP]; RSP += size` |
| `MOVSB/MOVSW/MOVSD/MOVSQ` | none           | Move string byte/word/dword/qword  | Memory copy                |
| `MOVSS`                   | `xmm, mem/reg` | Move scalar single-precision float | Copies float to/from XMM   |
| `MOVSD`                   | `xmm, mem/reg` | Move scalar double-precision float | Copies double to/from XMM  |
| `MOVAPS`                  | `xmm, xmm/mem` | Move aligned packed float          | XMM register copy          |
| `MOVUPS`                  | `xmm, xmm/mem` | Move unaligned packed float        | XMM register copy          |

---

## **2. Arithmetic**
| Instruction | Operands       | Description                       | Effect / Return                 |
| ----------- | -------------- | --------------------------------- | ------------------------------- |
| `ADD`       | `dst, src`     | Integer addition                  | `dst = dst + src`               |
| `SUB`       | `dst, src`     | Integer subtraction               | `dst = dst - src`               |
| `INC`       | `dst`          | Increment                         | `dst++`                         |
| `DEC`       | `dst`          | Decrement                         | `dst--`                         |
| `MUL`       | `src`          | Unsigned multiply                 | Result in `RDX:RAX`             |
| `IMUL`      | `dst, src`     | Signed multiply                   | Result in dst                   |
| `DIV`       | `src`          | Unsigned divide                   | Quotient `RAX`, remainder `RDX` |
| `IDIV`      | `src`          | Signed divide                     | Quotient `RAX`, remainder `RDX` |
| `NEG`       | `dst`          | Two's complement negate           | `dst = -dst`                    |
| `ADC`       | `dst, src`     | Add with carry                    | `dst = dst + src + CF`          |
| `SBB`       | `dst, src`     | Subtract with borrow              | `dst = dst - src - CF`          |
| `ADDSD`     | `xmm, xmm/mem` | Add scalar double-precision float | XMM result                      |
| `SUBSD`     | `xmm, xmm/mem` | Subtract scalar double            | XMM result                      |
| `MULSD`     | `xmm, xmm/mem` | Multiply scalar double            | XMM result                      |
| `DIVSD`     | `xmm, xmm/mem` | Divide scalar double              | XMM result                      |
| `ADDSS`     | `xmm, xmm/mem` | Add scalar single                 | XMM result                      |
| `SUBSS`     | `xmm, xmm/mem` | Subtract scalar single            | XMM result                      |
| `MULSS`     | `xmm, xmm/mem` | Multiply scalar single            | XMM result                      |
| `DIVSS`     | `xmm, xmm/mem` | Divide scalar single              | XMM result                      |

---

## **3. Logical / Bitwise**

| Instruction      | Operands | Description         | Effect     |       |
| ---------------- | -------- | ------------------- | ---------- | ----- |
| `AND`            | dst, src | Bitwise AND         | dst &= src |       |
| `OR`             | dst, src | Bitwise OR          | dst        | = src |
| `XOR`            | dst, src | Bitwise XOR         | dst ^= src |       |
| `NOT`            | dst      | Bitwise NOT         | dst = ~dst |       |
| `TEST`           | op1, op2 | AND for flags       | No change  |       |
| `BT/BTS/BTR/BTC` | dst, bit | Bit test/manipulate | CF = bit   |       |

---

## **4. Shift & Rotate**

| Instruction | Operands | Description             | Effect                 |
| ----------- | -------- | ----------------------- | ---------------------- |
| `SHL/SAL`   | dst, imm | Logical/arithmetic left | dst <<= imm            |
| `SHR`       | dst, imm | Logical right           | dst >>= imm, zero-fill |
| `SAR`       | dst, imm | Arithmetic right        | dst >>= imm, sign-fill |
| `ROL/ROR`   | dst, imm | Rotate bits             | Rotated bits           |
| `RCL/RCR`   | dst, imm | Rotate through carry    | dst rotated + CF       |

---

## **5. Comparison & Flags**
| Instruction | Description               | Effect / Return             |
| ----------- | ------------------------- | --------------------------- |
| `PUSHF`     | Push EFLAGS/RFLAGS        | Push current flags to stack |
| `POPF`      | Pop EFLAGS/RFLAGS         | Restore flags from stack    |
| `LAHF`      | Load status flags into AH | AH = SF:ZF:AF:PF:CF         |
| `SAHF`      | Store AH to flags         | Flags updated               |
| `STC`       | Set carry flag            | CF = 1                      |
| `CLC`       | Clear carry flag          | CF = 0                      |
| `CLD`       | Clear direction flag      | DF = 0                      |
| `STD`       | Set direction flag        | DF = 1                      |

---

## **6. Control Flow**

| Instruction | Operands | Description           | Effect              |
| ----------- | -------- | --------------------- | ------------------- |
| `JMP`       | label    | Unconditional jump    | RIP = label         |
| `JE/JZ`     | label    | Jump if equal / zero  | Conditional         |
| `JNE/JNZ`   | label    | Jump if not equal     | Conditional         |
| `JG/JNLE`   | label    | Jump if greater       | Signed              |
| `JL/JNGE`   | label    | Jump if less          | Signed              |
| `JA/JNBE`   | label    | Jump if above         | Unsigned            |
| `JB/JNAE`   | label    | Jump if below         | Unsigned            |
| `CALL`      | label    | Call function         | Push RIP, jump      |
| `RET`       | —        | Return                | Pop RIP             |
| `LOOP`      | label    | Loop CX/ECX/RCX times | CX--, jump if CX!=0 |

---

## **7. Function / Stack Frame**

| Instruction    | Operands    | Description       | Effect               |
| -------------- | ----------- | ----------------- | -------------------- |
| `ENTER`        | size, level | Setup stack frame | Push RBP, adjust RSP |
| `LEAVE`        | —           | Destroy frame     | RSP = RBP, pop RBP   |
| `PUSHF`        | —           | Push FLAGS        | RSP -= 8             |
| `POPF`         | —           | Pop FLAGS         | RSP += 8             |
| `PUSHA/PUSHAD` | —           | Push all regs     | RSP -= N             |
| `POPA/POPAD`   | —           | Pop all regs      | RSP += N             |

---

## **8. Data Size Conversion / Sign Extension**

| Instruction | Description   | Effect                            |
| ----------- | ------------- | --------------------------------- |
| `CBW`       | AL → AX       | Sign-extend byte to word          |
| `CWD`       | AX → DX:AX    | Sign-extend word to doubleword    |
| `CWDE`      | AX → EAX      | Sign-extend word to dword         |
| `CDQ`       | EAX → EDX:EAX | Sign-extend dword to qword        |
| `CDQE`      | EAX → RAX     | Sign-extend dword to qword        |
| `CQO`       | RAX → RDX:RAX | Sign-extend quadword for division |

---

## **9. String Instructions**

| Instruction | Description    | Effect                            |
| ----------- | -------------- | --------------------------------- |
| `MOVS`      | Move string    | Memory copy                       |
| `LODS`      | Load string    | Load AL/AX/EAX/RAX from DS:SI     |
| `STOS`      | Store string   | Store AL/AX/EAX/RAX to ES:DI      |
| `CMPS`      | Compare string | Flags updated                     |
| `SCAS`      | Scan string    | Compare AL/AX/EAX/RAX with memory |

---

## **10. Floating Point (x87)**

| Instruction   | Operands | Description       | Effect        |
| ------------- | -------- | ----------------- | ------------- |
| `FLD`         | src      | Load float        | Push FP stack |
| `FSTP`        | dst      | Store & pop       | Save float    |
| `FADD`        | src      | Floating add      | ST0 += src    |
| `FSUB`        | src      | Floating subtract | ST0 -= src    |
| `FMUL`        | src      | Floating multiply | ST0 *= src    |
| `FDIV`        | src      | Floating divide   | ST0 /= src    |
| `FSIN`/`FCOS` | —        | Sine / Cosine     | Result ST0    |
| `FILD`        | src      | Load integer      | Push FP stack |
| `FISTP`       | dst      | Store integer     | Pop FP stack  |

---

## **11. SIMD (SSE / AVX)**

| Instruction     | Operands | Description            | Effect        |
| --------------- | -------- | ---------------------- | ------------- |
| `MOVDQA/MOVAPS` | dst, src | Move aligned           | XMM copy      |
| `MOVDQU/MOVUPS` | dst, src | Move unaligned         | XMM copy      |
| `ADDPS`         | dst, src | Packed float add       | Vector result |
| `SUBPS`         | dst, src | Packed float subtract  | Vector result |
| `MULPS`         | dst, src | Packed float multiply  | Vector result |
| `DIVPS`         | dst, src | Packed float divide    | Vector result |
| `ADDPD`         | dst, src | Packed double add      | Vector result |
| `SUBPD`         | dst, src | Packed double subtract | Vector result |

---

## **12. System / CPU Control**

| Instruction | Description         | Effect               |
| ----------- | ------------------- | -------------------- |
| `NOP`       | No operation        | None                 |
| `HLT`       | Halt CPU            | Stop until interrupt |
| `INT imm`   | Software interrupt  | Call ISR             |
| `SYSCALL`   | System call (x64)   | OS transition        |
| `SYSRET`    | Return from syscall | User mode            |

---

## **13. Key Registers (x86-64)**

| Register     | Purpose                    |
| ------------ | -------------------------- |
| `RAX`        | Accumulator / return value |
| `RBX`        | Base register              |
| `RCX`        | Counter / argument         |
| `RDX`        | Data / remainder           |
| `RSI`        | Source index               |
| `RDI`        | Destination index          |
| `RSP`        | Stack pointer              |
| `RBP`        | Base pointer               |
| `RIP`        | Instruction pointer        |
| `EFLAGS`     | Flags register             |
| `XMM0-XMM15` | SIMD registers             |
| `ST0-ST7`    | x87 floating point stack   |
