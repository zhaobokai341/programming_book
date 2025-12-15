# x86 / x86-64 Assembly Instructions (Common Set)

> **Note**: There is no such thing as *literally all* instructions in a short list (x86 has 1000+ variants including SIMD).
> This table covers the **core, commonly-used x86/x86-64 instructions** grouped by purpose.

---

## Data Transfer Instructions

| Instruction | Operands (Value) | Description               | Return / Effect         |
| ----------- | ---------------- | ------------------------- | ----------------------- |
| `MOV`       | `dst, src`       | Copy data from src to dst | `dst = src`             |
| `MOVZX`     | `dst, src`       | Move with zero extension  | Zero-extended value     |
| `MOVSX`     | `dst, src`       | Move with sign extension  | Sign-extended value     |
| `XCHG`      | `op1, op2`       | Swap values               | Values exchanged        |
| `LEA`       | `dst, mem`       | Load effective address    | Address, no memory read |
| `PUSH`      | `src`            | Push onto stack           | `RSP -= size`           |
| `POP`       | `dst`            | Pop from stack            | `RSP += size`           |

---

## Arithmetic Instructions

| Instruction | Operands   | Description       | Return / Effect                 |
| ----------- | ---------- | ----------------- | ------------------------------- |
| `ADD`       | `dst, src` | Addition          | `dst = dst + src`               |
| `SUB`       | `dst, src` | Subtraction       | `dst = dst - src`               |
| `INC`       | `dst`      | Increment         | `dst++`                         |
| `DEC`       | `dst`      | Decrement         | `dst--`                         |
| `MUL`       | `src`      | Unsigned multiply | Result in `RDX:RAX`             |
| `IMUL`      | `dst, src` | Signed multiply   | Result in dst                   |
| `DIV`       | `src`      | Unsigned divide   | Quotient `RAX`, remainder `RDX` |
| `IDIV`      | `src`      | Signed divide     | Quotient `RAX`, remainder `RDX` |
| `NEG`       | `dst`      | Two's complement  | `dst = -dst`                    |

---

## Logical Instructions

| Instruction | Operands   | Description        | Return / Effect |
| ----------- | ---------- | ------------------ | --------------- |
| `AND`       | `dst, src` | Bitwise AND        | Result in dst   |
| `OR`        | `dst, src` | Bitwise OR         | Result in dst   |
| `XOR`       | `dst, src` | Bitwise XOR        | Result in dst   |
| `NOT`       | `dst`      | Bitwise NOT        | Inverted bits   |
| `TEST`      | `op1, op2` | AND for flags only | No data change  |

---

## Shift and Rotate

| Instruction   | Operands   | Description            | Return / Effect |
| ------------- | ---------- | ---------------------- | --------------- |
| `SHL` / `SAL` | `dst, imm` | Shift left             | Multiply by 2^n |
| `SHR`         | `dst, imm` | Logical shift right    | Zero-fill       |
| `SAR`         | `dst, imm` | Arithmetic shift right | Sign-fill       |
| `ROL`         | `dst, imm` | Rotate left            | Bit rotation    |
| `ROR`         | `dst, imm` | Rotate right           | Bit rotation    |

---

## Comparison & Flags

| Instruction | Operands   | Description           | Return / Effect |
| ----------- | ---------- | --------------------- | --------------- |
| `CMP`       | `op1, op2` | Compare values        | Flags set       |
| `SETcc`     | `dst`      | Set byte on condition | 0 or 1          |
| `CLC`       | none       | Clear carry flag      | CF = 0          |
| `STC`       | none       | Set carry flag        | CF = 1          |
| `CLD`       | none       | Clear direction flag  | DF = 0          |
| `STD`       | none       | Set direction flag    | DF = 1          |

---

## Control Flow (Jumps)

| Instruction | Operands | Description          | Return / Effect |
| ----------- | -------- | -------------------- | --------------- |
| `JMP`       | `label`  | Unconditional jump   | RIP = label     |
| `JE / JZ`   | `label`  | Jump if equal / zero | Conditional     |
| `JNE / JNZ` | `label`  | Jump if not equal    | Conditional     |
| `JG`        | `label`  | Jump if greater      | Signed          |
| `JL`        | `label`  | Jump if less         | Signed          |
| `JA`        | `label`  | Jump if above        | Unsigned        |
| `JB`        | `label`  | Jump if below        | Unsigned        |

---

## Function Call Instructions

| Instruction | Operands      | Description          | Return / Effect |
| ----------- | ------------- | -------------------- | --------------- |
| `CALL`      | `label`       | Call function        | Push RIP, jump  |
| `RET`       | none          | Return from function | Pop RIP         |
| `ENTER`     | `size, level` | Setup stack frame    | RBP-based frame |
| `LEAVE`     | none          | Destroy stack frame  | Restore RBP     |

---

## String Instructions

| Instruction | Operands | Description     | Return / Effect      |
| ----------- | -------- | --------------- | -------------------- |
| `MOVS`      | none     | Move string     | Memory copy          |
| `LODS`      | none     | Load string     | Load to AL/AX/EAX    |
| `STOS`      | none     | Store string    | Store from AL/AX/EAX |
| `CMPS`      | none     | Compare strings | Flags updated        |
| `SCAS`      | none     | Scan string     | Flags updated        |

---

## System & CPU Control

| Instruction | Operands | Description         | Return / Effect      |
| ----------- | -------- | ------------------- | -------------------- |
| `NOP`       | none     | No operation        | No effect            |
| `HLT`       | none     | Halt CPU            | Stop until interrupt |
| `INT`       | `imm`    | Software interrupt  | Kernel call          |
| `SYSCALL`   | none     | System call (x64)   | OS transition        |
| `SYSRET`    | none     | Return from syscall | User mode            |

---

## Floating Point (x87)

| Instruction | Operands | Description       | Return / Effect  |
| ----------- | -------- | ----------------- | ---------------- |
| `FLD`       | `src`    | Load float        | Push to FP stack |
| `FSTP`      | `dst`    | Store & pop       | Save float       |
| `FADD`      | `src`    | Floating add      | FP result        |
| `FSUB`      | `src`    | Floating subtract | FP result        |
| `FMUL`      | `src`    | Floating multiply | FP result        |
| `FDIV`      | `src`    | Floating divide   | FP result        |

---

## SIMD (SSE / AVX – Common)

| Instruction | Operands   | Description           | Return / Effect |
| ----------- | ---------- | --------------------- | --------------- |
| `MOVDQA`    | `dst, src` | Aligned move          | XMM copy        |
| `ADDPS`     | `dst, src` | Packed float add      | Vector result   |
| `SUBPS`     | `dst, src` | Packed float subtract | Vector result   |
| `MULPS`     | `dst, src` | Packed float multiply | Vector result   |
| `DIVPS`     | `dst, src` | Packed float divide   | Vector result   |

---

## Key Registers (x86-64)

| Register | Purpose                    |
| -------- | -------------------------- |
| `RAX`    | Accumulator / return value |
| `RBX`    | Base register              |
| `RCX`    | Counter / argument         |
| `RDX`    | Data / remainder           |
| `RSI`    | Source index               |
| `RDI`    | Destination index          |
| `RSP`    | Stack pointer              |
| `RBP`    | Base pointer               |
| `RIP`    | Instruction pointer        |

---

If you want:

* **Full instruction reference per Intel manual**
* **ARM / RISC-V version**
* **Only control-flow or syscall-focused instructions**
* **Cheat sheet PDF**

Tell me 👍
