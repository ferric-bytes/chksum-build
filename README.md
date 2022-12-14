# chksum-build

![Build](https://img.shields.io/github/actions/workflow/status/ferric-bytes/chksum-build/rust.yml?branch=master&style=flat-square&logo=github "Build")
[![Coverage](https://img.shields.io/codecov/c/gh/ferric-bytes/chksum-build?style=flat-square&logo=codecov "Coverage")](https://app.codecov.io/gh/ferric-bytes/chksum-build)
[![crates.io](https://img.shields.io/crates/v/chksum-build?style=flat-square&logo=rust "crates.io")](https://crates.io/crates/chksum-build)
[![docs.rs](https://img.shields.io/docsrs/chksum-build?style=flat-square&logo=docsdotrs "docs.rs")](https://docs.rs/chksum-build)
[![MSRV](https://img.shields.io/badge/MSRV-1.58.0-informational?style=flat-square "MSRV")](https://github.com/ferric-bytes/chksum-build/blob/master/Cargo.toml)
[![unsafe forbidden](https://img.shields.io/badge/unsafe-forbidden-success.svg?style=flat-square "unsafe forbidden")](https://github.com/rust-secure-code/safety-dance)
[![LICENSE](https://img.shields.io/github/license/ferric-bytes/chksum-build?style=flat-square "LICENSE")](https://github.com/ferric-bytes/chksum-build/blob/master/LICENSE)

Tiny library for setting/getting build-time values for your crate.

## Features

* Pure Rust,
* No unsafe code,
* As small as it possible,
* Configurable via Cargo features.

## Setup

### Create `build.rs`

Create new file `build.rs` at the top level of your crate (next to `Cargo.toml`).

```rust
use chksum_build::{BuildScript, Result};

fn main() -> Result<()> {
    BuildScript::default().setup()
}
```

### Update `Cargo.toml`

#### Modify `package` section

```toml
[package]
# ...
build = "build.rs"
```

#### Modify `build-dependencies` section

You can update `Cargo.toml` on your own.

```toml
[build-dependencies]
# ...
chksum-build = "0.0.3"
```

Or use [`cargo add`](https://doc.rust-lang.org/cargo/commands/cargo-add.html) subcommand.

```sh
cargo add --build chksum-build
```

#### Modify `dependencies` section

As in the example above you can add entry manually.

```toml
[dependencies]
# ...
chksum-build = "0.0.3"
```

Or by using subcommand.

```sh
cargo add chksum-build
```

## Usage

```rust
use chksum_build::build_info;

let build_info = build_info!();
```

More usage examples are available in the documentation at [docs.rs](https://docs.rs/chksum-build).

## Alternatives

* [build-data](https://crates.io/crates/build-data)
* [build-info](https://crates.io/crates/build-info)
* [built](https://crates.io/crates/built)
* [shadow-rs](https://crates.io/crates/shadow-rs)
* [vergen](https://crates.io/crates/vergen)

## License

MIT
