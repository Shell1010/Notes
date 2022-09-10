# Using [Box\<T>](https://doc.rust-lang.org/std/boxed/struct.Box.html#) to Point to Data stored on the Heap

The most straightfowards smart pointer is box, it allows you to store data on the heap rather than the stack. What remains on the stack is the pointer to the heap data. 

Boxes alone don't have performance overhead, other than storing their data (this may take longer), but they don't have many extra capabilities. They are used in these specific situations:

- When you have a type whose size can't be known at compile time, and you want to use a value of that type in a context that requires an exact size.
- When you have a large amount of data and you want to transfer ownership, but ensure the data won't be copied when you do so.
- When you want to own a value, but you only care that it implements a trait rather than the specific type.

Example of storing data on the heap using [Box\<T>](https://doc.rust-lang.org/std/boxed/struct.Box.html#). 

```rust
fn main() { 
	let b = Box::new(5);
	println!("b = {}", b);
}
```
