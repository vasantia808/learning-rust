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

- Learned about how you can create a new instance of a struct, using
  some of the values of another instance. This can be done via struct
  update syntax. It's important to note that some types that live on
  the stack, like booleans, integers, and chars, are copied by Rust via
  the `Copy` trait. Types like a String, which have data on the heap,
  have to either be moved or explicitly cloned. Also, when you move
  the data from one field in a struct instance to another instance,
  that field becomes invalid, but the other fields are not affected
  and are still useable.

---

*Last updated: 2026-03-17*
