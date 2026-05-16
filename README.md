# Brainfuck Interpreter in Rust

A simple Brainfuck interpreter written in Rust.

It supports:

- Pointer movement (`>`, `<`)
- Cell increment/decrement (`+`, `-`)
- Output (`.`)
- Loops (`[` and `]`)
- Bracket matching using a precomputed map

---

## Features

- 30,000-byte memory tape
- Loop handling with bracket jump table
- Wrapping arithmetic using `wrapping_add` and `wrapping_sub`
- Simple and lightweight implementation

---

## How It Works

1. Builds a bracket map for fast loop jumps
2. Uses:
   - `dp` → data pointer
   - `pc` → program counter
3. Executes Brainfuck instructions one byte at a time
4. Handles loops efficiently using precomputed bracket positions

---

## Supported Instructions

| Instruction | Description |
|-------------|-------------|
| `>` | Move pointer right |
| `<` | Move pointer left |
| `+` | Increment current cell |
| `-` | Decrement current cell |
| `.` | Output current cell |
| `,` | Input (not implemented) |
| `[` | Jump forward if cell is zero |
| `]` | Jump backward if cell is non-zero |

---

## Example Program

```rust
let program = "-.";
```

Output:

```text
ÿ
```

---

## Run

```bash
cargo run
```

---

## Example Output

```text
Hello World!
```

(when using a valid Brainfuck Hello World program)

---

## Build Release Binary

```bash
cargo build --release
```

Run binary:

```bash
./target/release/brainfuck-interpreter
```

---

## Future Improvements

- Add input support (` , `)
- Load `.bf` files
- Better error handling
- Dynamic tape resizing
- Debug mode
