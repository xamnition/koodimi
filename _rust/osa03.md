---
title: "Rust-Opas osa3"
author: "Samuel Kriikkula"
tags: rust
redirect_from:
  - /rust/osa3
---

# Merkkijonot, "stringit"
Rustissa on kahdenlaisia merkkijonoja (molemmat tosin utf-8).

## &str
Merkkijonoreferenssi. Tätä on hyvä käyttää, kun haluaa lukea merkkijonon muuttamatta sitä.

```rust
fn main() {
    let my_string: &str = "hello rust";
    print_str(my_string);
}

fn print_str(s: &str) {
    println!("{s}");
}
```

## String
Omistettu merkkijono. Hyvä valinta, jos merkkijonoa tulee muuttamaan jollain tavalla.
`String`in saa `&str` muotoon `.as_str()` metodin avulla.
`&str` referenssin saa `String` muotoon funktiolla `String::from`.
```rust
fn main() {
    let mut my_string: String = String::from("hello, ");
    my_string.push_str("Rust!");
    print_str(my_string.as_str());
}

fn print_str(s: &str) {
    println!("{s}");
}
```

### Metodit
Tärkeimmät metodit ovat varmaankin `push_str`, jolla pusketaan stringiin merkkijonoreferenssi `&str` tai `push` jolla pusketaan merkki. Merkkijonot tarjoavat vaikka mitä funktionaalisuutta, joita tällä kurssilla ei käsitellä. Netti on apuri näissä!


## char
`char` vastaa unicode-merkkiä.
```rust
let my_char: char = 'ä';
```
