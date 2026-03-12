# Ownership and Borrowing

## The Core Idea

Rust's ownership system enforces memory safety at compile time 
instead of at runtime. Every value has exactly one owner. When 
the owner goes out of scope, the value is dropped automatically.

## The Three Rules

1. Each value has exactly one owner
2. There can only be one owner at a time
3. When the owner goes out of scope, the value is dropped

## Borrowing vs Moving

- **Move:** ownership transfers, original variable no longer valid
- **Borrow (`&`):** temporary read-only reference, original owner 
  retains ownership
- **Mutable borrow (`&mut`):** only one allowed at a time, prevents 
  data races

## Code Example
```rust
fn main() {
    let s1 = String::from("hello");
    let s2 = s1; // s1 is moved, no longer valid

    // println!("{}", s1); // This would fail to compile
    println!("{}", s2);   // This works
}
```

## Why This Matters for Security

Rust's ownership model prevents entire classes of vulnerabilities 
at compile time:

- **Use-after-free** — impossible because the compiler tracks ownership
- **Double-free** — impossible for the same reason
- **Data races** — prevented by the single mutable borrow rule
- **Buffer overflows** — bounds checking is enforced by default

These bug classes account for a significant percentage of real-world 
CVEs in C and C++ codebases. Understanding ownership builds intuition 
for why these vulnerabilities exist in other languages.

## Connections to Security Work

- Heap spraying and use-after-free exploits target exactly the memory 
  safety gaps that Rust's ownership system closes
- Understanding ownership makes reading CVE technical writeups clearer
- Rust is increasingly used for security tooling precisely because of 
  these guarantees

## What Tripped Me Up

- The variable, not the value has a type.

---

*Will add notes here as I work through ownership concepts.*

---

*Last updated: 2026-03-11*
