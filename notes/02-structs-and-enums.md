# Structs and Enums

## Structs

Structs are custom data types that group related values together,
similar to objects in other languages but without inheritance.

## Enums

Enums define a type that can be one of several variants. Rust's
enums are more powerful than in most languages because each variant
can carry data.

## The Option Enum

Rust has no null values. Instead it uses the built-in `Option` enum:
```rust
enum Option<T> {
    Some(T),
    None,
}
```

This forces you to explicitly handle the case where a value might
not exist, eliminating null pointer errors at compile time.

## The Result Enum

Used for error handling:
```rust
enum Result<T, E> {
    Ok(T),
    Err(E),
}
```

## Why This Matters for Security

- No null pointers means no null pointer dereference vulnerabilities
- Explicit error handling via Result means errors cannot be silently 
  ignored the way they can in languages that use exceptions or return 
  codes informally

## What Tripped Me Up

---

*Will add notes here as I work through structs and enums.*

---

*Last updated: 2026-03-11*
