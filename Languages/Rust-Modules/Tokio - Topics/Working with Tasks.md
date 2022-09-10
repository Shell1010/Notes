# Working with Tasks

Asynchronous programs in Rust are based around lightweight, non-blocking units of execution named tasks. The [tokio::task](https://docs.rs/tokio/latest/tokio/task/index.html) module provides tools for working with them.

Here is an example for [tokio::spawn](https://docs.rs/tokio/latest/tokio/fn.spawn.html#). This spawns a task, a unit of execution that is non-blocking. This runs in the background as the main thread executes.

```rust
use tokio::net::{TcpListener, TcpStream};

use std::io;

async fn process(socket: TcpStream) {
    // ...
}

#[tokio::main]
async fn main() -> io::Result<()> {
    let listener = TcpListener::bind("127.0.0.1:8080").await?;

    loop {
        let (socket, _) = listener.accept().await?;

        tokio::spawn(async move {
            // Process each socket concurrently.
            process(socket).await
        });
    }
}
```
