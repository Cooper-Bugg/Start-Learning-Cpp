```markdown
# File-Stat-Tool

Command-line C++ utility that analyzes files and reports basic statistics useful for quick inspection and text-analysis exercises.

Features:
- Report file size in bytes and human-friendly units.
- Line count and word count with configurable word delimiters.
- Byte frequency distribution (histogram) to spot binary vs text content.
- Optional streaming mode to process very large files without loading into memory.

Learning outcomes:
- Practice efficient file I/O using C++ standard streams or low-level POSIX APIs.
- Implement streaming algorithms and memory-constant processing.
- Build small test fixtures to verify counts on sample inputs.

Build & run (example):
```sh
g++ -std=c++17 -O2 -o filestat main.cpp
./filestat path/to/file.txt
```

Usage examples:
- `./filestat README.md` — prints size, lines, words, and a byte-frequency summary.
- `./filestat --stream huge.log` — run in streaming mode with low memory overhead.

Notes:
- Provide unit tests that compare results to known `wc` outputs for correctness.
- Consider portable newline handling and binary/text mode differences on Windows.
```
