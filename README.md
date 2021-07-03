# exec-target

the simple invoke command for test

This invokes external a command and manipulates standard in out.
You can use `std::process::Command` more easily.

* minimum support rustc 1.43.0

## Example:

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
