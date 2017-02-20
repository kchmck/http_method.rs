# uhttp\_method -- HTTP request method parser/formatter

[Documentation](https://docs.rs/uhttp_method)

This crate provides an HTTP request method parser/formatter, split out from
[hyper.rs](https://hyper.rs).

## Example

```rust
use uhttp_method::Method;

assert_eq!("GET".parse(), Ok(Method::Get));
assert!(Method::Get.idempotent());
assert_eq!(format!("{}", Method::Patch), "PATCH");
```

## Usage

This [crate](https://crates.io/crates/uhttp_method) can be used through cargo by
adding it as a dependency in `Cargo.toml`:

```toml
[dependencies]
uhttp_method = "0.10.0"
```
and importing it in the crate root:

```rust
extern crate uhttp_method;
```
