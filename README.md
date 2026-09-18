# C Programming - Week 1

## Goal
Build enough C and memory understanding to eventually understand GDB and binary exploitation from the core level.

---

## Day 1 - C Fundamentals + Pointer Introduction ✅

- [x] Review variables and basic data types
- [x] Review if/else and logical operators
- [x] Review loops
- [x] Review functions and return values
- [x] Review arrays and indexing
- [x] Review strings and `\0`
- [x] Understand integer division and `%`
- [x] Understand declaration vs initialization
- [x] Understand basic buffer overflow concept
- [x] Begin pointers
- [x] Understand `&x` as the address of `x`
- [x] Understand `p` as a pointer containing an address
- [x] Understand `*p` as the value at that address
- [x] Understand changing a value through `*p`

### Day 1 takeaway
`x` → value  
`&x` → address of x  
`p` → pointer containing an address  
`*p` → value at that address

### C Mistakes to Remember
1. **Integer division:** `10 / 3` with two `int`s gives `3`, not `3.333`.
2. **Array bounds:** `numbers[5]` is not `null`; it is an out-of-bounds access if the array has indices `0–4`.
3. **Strings:** `"Rudy"` is stored as `R u d y \0`, so the `\0` terminator also needs space.
4. **Uninitialized variables:** `int a;` declares a variable but does not give it a defined value.
5. **Pointers:** `p` is the pointer, while `*p` means the value stored at the address inside `p`.
6. **`&x`:** `&x` gives the address of `x`.
7. **`*p = 20`:** This changes the value at the address `p` points to. It does not change the address itself.
8. **Pointer declaration:** `int *p;` means `p` is a pointer capable of storing the address of an `int`.
9. **Array + pointer:** `int *p = numbers;` points to `numbers[0]`, not `numbers[3]`.
10. **Pointer arithmetic:** If `p` points to `numbers[0]`, then `p + 1` points to `numbers[1]`, and `p + 2` points to `numbers[2]`.


---

## Day 2 - Pointers

- [ ] Learn pointer declarations
- [ ] Learn addresses and memory locations
- [ ] Practice `&` and `*`
- [ ] Understand pointer assignment
- [ ] Understand dereferencing
- [ ] Understand changing variables through pointers
- [ ] Practice pointers with functions
- [ ] Practice pointers with arrays
- [ ] Understand pointer arithmetic
- [ ] Understand `p`, `p + 1`, `*p`, `*(p + 1)`
- [ ] Write small pointer programs without AI

### Goal
Be able to look at pointer code and explain exactly what each pointer contains and what memory it accesses.

---

## Day 3 - Arrays, Strings & Pointers

- [ ] Understand the relationship between arrays and pointers
- [ ] Practice `numbers[i]` vs `*(numbers + i)`
- [ ] Understand array memory layout
- [ ] Practice character arrays
- [ ] Understand C strings and `\0`
- [ ] Practice strings using pointers
- [ ] Understand common string-related mistakes
- [ ] Practice out-of-bounds access conceptually
- [ ] Write small programs using arrays + pointers

### Goal
Stop thinking of arrays as isolated boxes and start understanding them as data occupying contiguous memory.

---

## Day 4 - Structs, Pointers & Dynamic Memory

- [ ] Review structs
- [ ] Create and access structs
- [ ] Understand pointers to structs
- [ ] Learn `->`
- [ ] Understand stack vs heap at a basic level
- [ ] Learn `malloc`
- [ ] Learn `free`
- [ ] Understand why dynamically allocated memory exists
- [ ] Practice allocating and freeing memory
- [ ] Understand what happens when memory is used incorrectly

### Goal
Understand how programs create, access, and release memory.

---

## Day 5 - Memory Bugs

- [ ] Review buffer overflow
- [ ] Understand out-of-bounds reads
- [ ] Understand out-of-bounds writes
- [ ] Understand dangling pointers
- [ ] Understand use-after-free conceptually
- [ ] Understand NULL pointers
- [ ] Understand uninitialized pointers
- [ ] Read small vulnerable C programs
- [ ] Identify what memory operation is unsafe
- [ ] Explain why the bug happens

### Goal
Given a small C program, identify where memory assumptions can fail.

---

## Day 6 - C Code Reading + Debugging

- [ ] Read unfamiliar C programs
- [ ] Trace variables manually
- [ ] Trace function calls
- [ ] Trace pointer changes
- [ ] Trace array access
- [ ] Predict program output before running it
- [ ] Intentionally introduce bugs
- [ ] Compile and fix them
- [ ] Start basic GDB
- [ ] Learn `break`
- [ ] Learn `run`
- [ ] Learn `next`
- [ ] Learn `print`
- [ ] Learn `info`

### Goal
Start observing what the program is actually doing instead of relying only on source code.

---

## Day 7 - Consolidation

- [ ] Write a small C program from scratch
- [ ] Use variables, functions, arrays and pointers
- [ ] Use at least one struct
- [ ] Allocate memory with `malloc`
- [ ] Free allocated memory
- [ ] Debug a bug without immediately asking AI
- [ ] Read a ~100-line C program
- [ ] Identify inputs
- [ ] Trace important variables
- [ ] Identify pointers and memory operations
- [ ] Explain the program in your own words
- [ ] Review all mistakes from the week

### End-of-Week Test

I should be able to:

- [ ] Explain what a pointer is
- [ ] Explain `&x`
- [ ] Explain `*p`
- [ ] Explain the difference between `p` and `*p`
- [ ] Explain pointer arithmetic
- [ ] Explain arrays vs pointers
- [ ] Explain `\0`
- [ ] Explain stack vs heap at a basic level
- [ ] Explain `malloc` and `free`
- [ ] Identify basic memory-safety bugs
- [ ] Read basic C code without needing line-by-line AI explanations
- [ ] Use basic GDB commands

---

## Rule for the Week

Do not optimize the learning process instead of learning.

Use AI for:
- [ ] Explaining a concept after trying it yourself
- [ ] Debugging after attempting to find the problem
- [ ] Clarifying terminology

Do NOT use AI to:
- [ ] Write the exercise before attempting it
- [ ] Give the answer immediately
- [ ] Replace struggling with a concept

### Main objective

C → Memory → GDB → Exploitation

The goal is not to "finish C."

The goal is to understand what a program is doing at the memory level well enough that exploitation eventually makes sense.
