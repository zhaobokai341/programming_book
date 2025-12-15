# x86 / x86-64 Assembly – Ultimate Cheat Sheet

---

## **1. Data Transfer**

| Instruction               | Operands | Description              | Effect                  |
| ------------------------- | -------- | ------------------------ | ----------------------- |
| `MOV`                     | dst, src | Move data                | dst = src               |
| `MOVZX`                   | dst, src | Move with zero extension | dst = zero-extended src |
| `MOVSX`                   | dst, src | Move with sign extension | dst = sign-extended src |
| `XCHG`                    | op1, op2 | Swap values              | Values exchanged        |
| `LEA`                     | dst, mem | Load effective address   | dst = address           |
| `PUSH`                    | src      | Push onto stack          | RSP -= size             |
| `POP`                     | dst      | Pop from stack           | RSP += size             |
| `MOVSB/MOVSW/MOVSD/MOVSQ` | —        | String move              | Memory copy             |

---

## **2. Arithmetic**

| Instruction | Operands        | Description          | Effect                              |
| ----------- | --------------- | -------------------- | ----------------------------------- |
| `ADD`       | dst, src        | Add                  | dst += src                          |
| `SUB`       | dst, src        | Subtract             | dst -= src                          |
| `INC`       | dst             | Increment            | dst++                               |
| `DEC`       | dst             | Decrement            | dst--                               |
| `MUL`       | src             | Unsigned multiply    | RDX:RAX = RAX * src                 |
| `IMUL`      | dst, src[, imm] | Signed multiply      | dst = dst * src                     |
| `DIV`       | src             | Unsigned divide      | Quotient = RAX/src, RDX = remainder |
| `IDIV`      | src             | Signed divide        | Quotient = RAX/src, RDX = remainder |
| `NEG`       | dst             | Two’s complement     | dst = -dst                          |
| `ADC`       | dst, src        | Add with carry       | dst += src + CF                     |
| `SBB`       | dst, src        | Subtract with borrow | dst -= src + !CF                    |

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

| Instruction | Operands | Description           | Effect                      |
| ----------- | -------- | --------------------- | --------------------------- |
| `CMP`       | op1, op2 | Compare               | Sets flags (ZF, SF, CF, OF) |
| `TEST`      | op1, op2 | AND for flags         | Flags set, no data change   |
| `SETcc`     | dst      | Set byte if condition | dst = 0 or 1                |
| `CLC`       | —        | Clear carry           | CF = 0                      |
| `STC`       | —        | Set carry             | CF = 1                      |
| `CLD`       | —        | Clear direction       | DF = 0                      |
| `STD`       | —        | Set direction         | DF = 1                      |
| `LAHF`      | —        | Load flags to AH      | AH = FLAGS                  |
| `SAHF`      | —        | Store AH to flags     | FLAGS = AH                  |

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


Do you want me to generate that too?
