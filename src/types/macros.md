# Macros

Compile-time code generation tools.
Used for metaprogramming, to generate code based on patterns, reducing boilerplate and increasing flexibility.

```rust
macro_rules! custom_println {
    () => {
        println!("No parameters given.");
    };
    ($msg:expr) => {
        println!("One parameter: {}", $msg);
    };
    ($msg:expr, $param:expr) => {
        println!("Two parameters: {} and {}", $msg, $param);
    };
}

fn main() {
    custom_println!();  // Outputs: No parameters given.
    custom_println!("Hello, World");  // Outputs: One parameter: Hello, World
    custom_println!("Hello", "World");  // Outputs: Two parameters: Hello and World
}
```
