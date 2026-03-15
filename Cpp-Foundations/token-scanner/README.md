# token-scanner

A reusable TokenScanner class that breaks an input string into a stream of tokens: numbers, words, operators, and punctuation. Designed as a drop-in upgrade for Mini-CLI-Calc and as a foundation for any future parser work.

## Features

- Scan a string or input stream into typed tokens: NUMBER, WORD, OPERATOR, PUNCTUATION, END.
- Configurable delimiters and whitespace handling.
- Peek at the next token without consuming it.
- Save and restore scanner position for backtracking.
- Clear error reporting for unexpected characters.

## Learning outcomes

- Design a class with a well-defined public interface and hidden internal state.
- Understand the difference between interface design and implementation — callers should not care how tokens are stored internally.
- Practice writing a class that other classes depend on, which forces you to think about stability and contracts.
- See how a scanner layer separates concerns from the evaluator layer in Mini-CLI-Calc.

## Build & run

g++ -std=c++17 -O2 -o token-scanner main.cpp scanner.cpp
./token-scanner

- Input "3 + 4 * 2" — tokens: 3, +, 4, *, 2, END
- Input "sin(x)" — tokens: sin, (, x, ), END

## Build it when

- You can describe the public interface of the class completely — what methods exist, what they return, what they guarantee — before writing the .h file.

## Notes

- Write this before upgrading Mini-CLI-Calc. Then swap in the scanner and observe how much simpler the calculator's parsing logic becomes.
- Unit tests should cover: empty input, whitespace-only input, multi-digit numbers, consecutive operators, and an unknown character.
