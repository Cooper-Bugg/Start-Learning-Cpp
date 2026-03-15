```markdown
# mini-disasm

Educational disassembler for a tiny instruction subset. The project focuses on binary parsing, opcode decoding, and human-friendly output formats for teaching purposes.

Features:
- Parse binary instruction streams for a small custom or reduced ISA subset.
- Pretty-print mnemonics, operands, and addresses with annotation hints.
- Test cases that map known byte patterns to expected assembly output.

Learning outcomes:
- Understand opcode decoding and the relationship between binary encodings and assembly mnemonics.
- Build clear, testable parsing code and mapping tables.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o mini-disasm main.cpp
./mini-disasm sample.bin
```

Notes:
- Keep the ISA small and documented; this is an educational tool rather than a production disassembler.
```
