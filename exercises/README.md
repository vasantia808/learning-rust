# Rustlings Exercise Insights

This file captures conceptual insights and "aha moments" from 
working through Rustlings exercises. Individual exercises are 
not documented here — only insights worth remembering.

---

## Insights

### Mutable Bindings
**Date:** 2026-03-13  
**Exercise:** move_semantics3   
**Insight:** The `mut` keyword belongs to the variable, not the type.

```
mut vec: Vec<i32>  // "vec" is a mutable binding
vec: mut Vec<i32>  // invalid — mut can't go here
```

**Why it matters for security:** Immutability by default reduces 
the risk of unintended state changes, which is a common source of 
bugs and vulnerabilities in other languages.

---

*Last updated: 2026-03-13*
