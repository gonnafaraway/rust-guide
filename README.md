# 🦀 Rust Style Guide
Community collected styleguide to write Rust code efficiently.

Just Rust.

<img width="100" height="100" alt="image" src="https://github.com/user-attachments/assets/275fde8e-a9e2-44e9-8c9a-4c45b39a568b" />

## 📖 Introduction

> **Important**: This style guide is based on official Rust recommendations and is designed for ease of use.

### 🎯 Purpose of Formatting
- **Time Saving** — automation through `rustfmt`
- **Consistency** — reduced cognitive load when reading code
- **Standardization** — minimized style debates in teams

## 🛠 Using rustfmt
```bash
# Check formatting
rustfmt --check src/main.rs

# Auto-format
rustfmt src/main.rs
```
### 🌐 Online (Rust Playground)

### 💬 Comments
* Single-line Comments
```rust
// ✅ Correct (with space after //)
fn main() {}

//❌ Incorrect (without space)
fn main() {}
```
* Block Comments
```rust
/* ✅ Correct single-line block */
/*❌ No spaces*/

/*
 * ✅ Multi-line comment
 * with line breaks
 */
```
* Comment Rules

🔤 Complete sentences — start with capital letter, end with period

📏 Length — max 80 characters or line width (whichever is smaller)

🚫 No trailing spaces — // comment not // comment_

### 🔡 Indentation Style

### 📦 Block Indent (Recommended)
```rust
// ✅ Block indent
a_function_call(
    foo,
    bar,
);

// ❌ Visual indent (avoid)
a_function_call(foo,
                bar);
```

Advantages:
- Fewer edits during refactoring
- Less rightward drift

### ✅ Trailing Commas
```rust
// ✅ With trailing comma
let array = [
    element,
    another_element,
    yet_another_element,
];

// ❌ Without trailing comma
let array = [
    element,
    another_element  // Adding new element requires changing this line
];
```
Why This Matters:
- Easier copy/paste
- Smaller diff when changing
- Consistent style

### ⏸ Empty Lines
```rust
fn foo() {
    let x = ...;
    
    // ✅ 1-2 empty lines between logical blocks
    let y = ...;
}

// ✅ No unnecessary empty lines
fn bar() {}
fn baz() {}
```
### 🎨 Visual Cheat Sheet

🏗 File Structure
```rust
// 1. Modules and imports
use std::collections::HashMap;

// 2. Constants
const MAX_SIZE: usize = 100;

// 3. Types
struct Point {
    x: i32,
    y: i32,
}

// 4. Implementations
impl Point {
    fn new(x: i32, y: i32) -> Self {
        Self { x, y }
    }
}

// 5. Functions
fn main() {
    // Logical blocks separated
    let point = Point::new(10, 20);
    
    // ... by one empty line
    println!("Point: {:?}", point);
}
```
### 📚 Sources
## 📚 Sources
🔗 Primary Materials
* [Official Rust Style Guide](https://github.com/rust-lang/rfcs/blob/master/style-guide/README.md)
* [rustfmt Documentation](https://github.com/rust-lang/rustfmt)
* [Rust Style Guide (Russian Translation)](https://github.com/rust-lang-ru/style-guide)

## 📖 Additional Resources
* [Rust Book](https://doc.rust-lang.org/book/)
* [Rust by Example](https://doc.rust-lang.org/rust-by-example/)
* [Clippy](https://github.com/rust-lang/rust-clippy)
