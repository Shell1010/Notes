# Working with multiple concurrent futures

Tokio also allows you to execute multiple futures concurrently at the same time. This is through the [tokio::join](https://docs.rs/tokio/latest/tokio/macro.join.html#) macro. This macro is designed to execute multiple futures at the same time. Example usage.

```rust
use futures::join;

async fn get_book_and_music() -> (Book, Music) {
    let book_fut = get_book();
    let music_fut = get_music();
    join!(book_fut, music_fut)
}
```

This is convenient in the event, you don't have a lot of futures in which you are working with. If you are working with 100's or 1000's of futures, this is deeply inconvenient in which we will look at our next method.

Within the [futures](https://docs.rs/futures/latest/futures/index.html) there is a very useful Struct that enables us to start 100's of futures concurrently. This is the [futures::stream::futures_unordered::FuturesUnordered](https://docs.rs/futures/latest/futures/stream/futures_unordered/struct.FuturesUnordered.html#) struct. This struct is essentially a list which allows one to store multiple futures inside, and then concurrently execute them all at once.

```rust
pub async fn spam_gen(&self, chan_id: &str, tokens: &Vec<String>, msg: &str) {

	let mut futs = FuturesUnordered::new();
	
	for token in tokens {
		futs.push(self.send_msg(chan_id, token, msg))
	}
	
	while let Some(_) = futs.next().await {}
}
```
