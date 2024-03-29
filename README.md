# exec-target

[![crate][crate-image]][crate-link]
[![Docs][docs-image]][docs-link]
![Rust Version][rustc-image]
![Apache2/MIT licensed][license-image]
[![Test ubu][test-ubuntu-image]][test-ubuntu-link]
[![Test mac][test-windows-image]][test-windows-link]
[![Test win][test-macos-image]][test-macos-link]

the simple invoke command for test

This invokes external a command and manipulates standard in out.
You can use `std::process::Command` more easily.

## Features

- minimum support rustc 1.56.1 (59eed8a2a 2021-11-01)

## Example

```rust
use exec_target::exec_target_with_env_in;

let command = "target/debug/exe-stab-grep";
let args = &["--color=always", "-e", "c"];
let envs = vec![("GREP_COLORS", "ms=01;32")];
let inp = b"abcdefg\n" as &[u8];

let oup = exec_target_with_env_in(command, args, envs, inp);

assert_eq!(oup.stderr, "");
assert_eq!(oup.stdout, "ab\u{1b}[01;32m\u{1b}[Kc\u{1b}[m\u{1b}[Kdefg\n");
assert_eq!(oup.status.success(), true);
```

# Changelogs

[This crate's changelog here.](https://github.com/aki-akaguma/exec-target/blob/main/CHANGELOG.md)

# License

This project is licensed under either of

 * Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or
   https://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or
   https://opensource.org/licenses/MIT)

at your option.

[//]: # (badges)

[crate-image]: https://img.shields.io/crates/v/exec-target.svg
[crate-link]: https://crates.io/crates/exec-target
[docs-image]: https://docs.rs/exec-target/badge.svg
[docs-link]: https://docs.rs/exec-target/
[rustc-image]: https://img.shields.io/badge/rustc-1.56+-blue.svg
[license-image]: https://img.shields.io/badge/license-Apache2.0/MIT-blue.svg
[test-ubuntu-image]: https://github.com/aki-akaguma/exec-target/actions/workflows/test-ubuntu.yml/badge.svg
[test-ubuntu-link]: https://github.com/aki-akaguma/exec-target/actions/workflows/test-ubuntu.yml
[test-macos-image]: https://github.com/aki-akaguma/exec-target/actions/workflows/test-macos.yml/badge.svg
[test-macos-link]: https://github.com/aki-akaguma/exec-target/actions/workflows/test-macos.yml
[test-windows-image]: https://github.com/aki-akaguma/exec-target/actions/workflows/test-windows.yml/badge.svg
[test-windows-link]: https://github.com/aki-akaguma/exec-target/actions/workflows/test-windows.yml
