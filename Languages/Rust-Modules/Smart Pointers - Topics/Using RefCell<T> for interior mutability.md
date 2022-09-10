# Using [RefCell\<T>](https://doc.rust-lang.org/std/cell/struct.RefCell.html#) for interior mutability

Interior mutability is a design patterin in Rust that allows one to mutate data, even when there are immutable references to that data. Normally this is disallowed due to borrowing rules, however RefCell exists for this purpose. It utilises unsafe code to bend the rules.

Bending rules at compile time, means that the errors will be caught and not run. RefCell allows these checks to be done at runtime, therefore if you break these rules, your program will Panic and then exit. 

This essentially allows the programmer themselves to check if the code adheres to the borrowing rules, it is useful if you understand your code follows the rules but the compiler does not know that.

Example usage of [RefCell\<T>](https://doc.rust-lang.org/std/cell/struct.RefCell.html#).

```rust
#[derive(Debug)]
enum List {
    Cons(Rc<RefCell<i32>>, Rc<List>),
    Nil,
}

use crate::List::{Cons, Nil};
use std::cell::RefCell;
use std::rc::Rc;

fn main() {
    let value = Rc::new(RefCell::new(5));

    let a = Rc::new(Cons(Rc::clone(&value), Rc::new(Nil)));

    let b = Cons(Rc::new(RefCell::new(3)), Rc::clone(&a));
    let c = Cons(Rc::new(RefCell::new(4)), Rc::clone(&a));

    *value.borrow_mut() += 10;

    println!("a after = {:?}", a);
    println!("b after = {:?}", b);
    println!("c after = {:?}", c);
}
```

