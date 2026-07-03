---
title: "Rust-Opas osa2"
author: "Samuel Kriikkula"
tags: rust
redirect_from:
  - /rust/osa7
---

## Structit

Structit koostuvat monesta muuttujasta.
Muista lisätä `pub` sana structin alkuun ja muuttujiin jos haluat julkistaa ne.
```rust
struct Person {
    name: String,
    age: usize,
    email: String,
}

fn main() {
    let bob = Person {
        name: String::from("Bob Smith"),
        age: 32,
        email: String::from("bsmith@example.com")
    };
    println!("{}", bob.name);
}
```

Voit myös hajoittaa structin osiinsa.
```rust
let Person { name, age, email } = bob; 
```
