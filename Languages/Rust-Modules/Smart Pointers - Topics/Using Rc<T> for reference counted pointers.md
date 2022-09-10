# Using [Rc\<T>](https://doc.rust-lang.org/stable/std/rc/struct.Rc.html#) for reference counted pointers

In majority of cases, ownership is very clear, you know exactly which variable owns a given value. However, in situations where a single value may have multiple owners, e.g a reference is passed around to multiple values, the variable is essentially owned by everything that points to it. Therefore, a variable shouldn't be dropped unless all references pointing to it have been deleted. 

To enable multiple ownership explicitly, you have to use the rust type [Rc\<T>](https://doc.rust-lang.org/stable/std/rc/struct.Rc.html#) which is an abbreviation for reference counting. This type of pointer keeps track of the number of references to it, if the number of values is > 0, the value stays in scope. If there are 0 references to this value, the value is dropped without any consequences.

Example of usage of [Rc\<T>](https://doc.rust-lang.org/stable/std/rc/struct.Rc.html#).

```rust
enum List {
    Cons(i32, Rc<List>),
    Nil,
}

use crate::List::{Cons, Nil};
use std::rc::Rc;

fn main() {
    let a = Rc::new(Cons(5, Rc::new(Cons(10, Rc::new(Nil)))));
    let b = Cons(3, Rc::clone(&a));
    let c = Cons(4, Rc::clone(&a));
}

```

In the event one wants to write multi-threaded, asynchronous or concurrent code, one can use [Arc\<T>](https://doc.rust-lang.org/std/sync/struct.Arc.html#).
