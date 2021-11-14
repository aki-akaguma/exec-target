TBD
===
Unreleased changes. Release notes have not yet been written.

0.2.4 (2021-11-14)
=====

* add more documents

0.2.3 (2021-07-03)
=====

* to github.com

0.2.2 (2021-07-03)
=====

* rewite TARGET_EXE_PATH with `env!("CARGO_BIN_EXE_exe-stab-cat")`
* rewite TARGET_EXE_PATH with `env!("CARGO_BIN_EXE_exe-stab-env")`
* rewite TARGET_EXE_PATH with `env!("CARGO_BIN_EXE_exe-stab-grep")`
* minimum support rustc 1.43.0
* add documents
* remove build.rs

0.2.1 (2021-06-23)
=====

* update depend: rustc_version(0.4)

0.2.0 (2021-04-02)
=====

* update depend: rustc_version(0.3)

0.1.6 (2020-11-17)
=====

* add README.md, COPYING, LICENSE-APACHE, LICENSE-MIT
* bug fix: not match https in help text on test-unix

0.1.5 (2020-11-12)
=====

* add support rustc 1.41
* downgrade rustc_version

0.1.4 (2020-05-10)
=====

* change edition 2015 to 2018

0.1.3 (2019-06-09)
=====

* bug fix: fn fotmat_diff_add_rem()
* add support of workspace and cargo make
* add doc comments
* remove cfg-if

0.1.2 (2019-05-30)
=====

* add test with exe-stab and cargo make support
* switch to cargo workspace
* modify env: AsRef<OsStr>

0.1.1 (2018-03-22)
=====

* add exec_target_with_env_in
* rename exec_target to exec-target
a lot of things...

0.1.0 (2017-11-06)
=====
first commit
