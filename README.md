# Learning Rust

Notes and projects from my Rust learning journey, with a focus 
on systems programming and security tooling.

**Status:** In progress — currently working through ownership, 
borrowing, and types  
**Resources:** The Rust Book, Rustlings exercises

---

## Why Rust for Security?

Rust's ownership model eliminates entire classes of memory safety 
vulnerabilities at compile time — use-after-free, double-free, 
buffer overflows — bugs that account for a significant percentage 
of real-world CVEs in C and C++ codebases. Learning Rust builds 
both development skill and a deeper understanding of the 
vulnerability classes that security engineers defend against.

---

## Concept Notes

| # | Topic | Status |
|---|-------|--------|
| 01 | [Ownership and Borrowing](notes/01-ownership-and-borrowing.md) | In progress |
| 02 | [Structs and Enums](notes/02-structs-and-enums.md) | In progress |

---

## Rustlings Insights

- [Exercise Insights](exercises/README.md)

---

## Projects

| Project | Description | Status |
|---------|-------------|--------|
| [See projects folder](projects/README.md) | Security-focused Rust tools | Planned |

---

## Connections to Security Work

- Ownership prevents use-after-free and double-free vulnerabilities
- No null pointers eliminates null pointer dereference bugs
- Explicit error handling via Result prevents silent failure
- Growing adoption in security tooling and systems programming

---

*Updated regularly as I progress through Rust.*
