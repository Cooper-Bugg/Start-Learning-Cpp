# float-inspector-cpp

CLI tool that performs IEEE-754 double-precision arithmetic and prints a step-by-step breakdown: sign, exponent, mantissa, alignment, GRS bits, and rounding decision. Demonstrates precision errors and catastrophic cancellation without a GUI.

## Features

- Take two double-precision values and an operation as input.
- Print the raw bits of each value broken down into sign (1 bit), exponent (11 bits), and mantissa (52 bits).
- Show the alignment step when exponents differ, including the GRS (guard, round, sticky) bits.
- Apply the rounding decision and show the final result's bit layout.
- Highlight precision errors and catastrophic cancellation with example inputs.

## Learning outcomes

- Use memcpy(&bits, &val, 8) to safely inspect the raw bit pattern of a double without undefined behavior.
- Extract sign, exponent, and mantissa fields using bit shifts and masks.
- Understand IEEE-754 bias, denormals, and how exponent alignment works before addition.
- Recognize catastrophic cancellation: when two nearly equal values subtract, significant bits are lost.
- Compare C++ raw memory access (memcpy) to Java's Double.doubleToRawLongBits().

## Build & run

g++ -std=c++17 -O2 -o float-inspector main.cpp
./float-inspector 1.0 3.14 add

## Build it when

- Extract the sign, exponent, and mantissa of 1.0 and 3.14 by hand using the IEEE-754 spec, then verify your code matches before adding any arithmetic logic.
