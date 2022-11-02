# rustls-example

A tweaked version of the `tlscient-mio` and `tlsserver-mio` examples from `rustls` that supports `serde` serialization
and sending of data.

## Setup

Certificate generation



## Building

```shell
cargo build
```

## Running

Run the server

```shell
cargo run --bin tlsserver-mio -- --verbose --certs certs/end.fullchain --key certs/end.rsa -p 8443 echo
```

Run the client

```shell
echo hello world | cargo run --bin tlsclient-mio -- --verbose --cafile certs/ca.cert -p 8443 localhost
```
