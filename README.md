# CORE — Virtual 8-bit CPU

A custom bytecode processor and two-pass assembler with register display, memory inspection, output port and single-step execution.

Open `index.html` in a browser.

## Architecture
256 bytes unified RAM, 8-bit accumulator and program counter, zero and carry/borrow flags, instruction register. Opcodes NOP=0, LDI=1, LDA=2, STA=3, ADD=4, SUB=5, JMP=6, JZ=7, JNZ=8, OUT=9, HLT=255. Instructions 1–8 have one operand byte. Arithmetic wraps modulo 256. Labels are resolved in a second pass.

## Limitations
Instruction-level emulator, not a gate-level or cycle-accurate HDL design. No interrupts, stack or operating system.
