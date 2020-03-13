Unofficial snapshots of a subset of crates in [facebookexperimental/eden/scm/libs](https://github.com/facebookexperimental/eden/tree/master/eden/scm/lib).

## Motivation

It might take some time for the upstream to publish crates on `crates.io`. For example, they might want 2-fac support which is currently not present in `crates.io`.

Before the upstream publishes the crates officially, this repository forks and renames the crates, then publishes them to `crates.io` with the new names that won't conflict with the upstream. Therefore those crates can actually be used in other projects that want to be published to `crates.io`, since `crates.io` does not allow dependencies in git sources.

## Crates

The crates are published to `crates.io` with prefix `esl01-`:
- `esl01-dag`
- `esl01-drawdag`
- `esl01-indexedlog`
- `esl01-mincode`
- `esl01-minibytes`
- `esl01-vlqencoding`

## Usage

When using the crates, consider using the [renaming feature](https://doc.rust-lang.org/cargo/reference/specifying-dependencies.html#renaming-dependencies-in-cargotoml) of `Cargo.toml` so future migration is easier:

```
[package]
mincode = { package = "esl01-mincode", version = "0.1" }
```

## Tests

The docstrings are not updated to use prefixed crate name. So `--doc` tests will fail. However, `--lib` tests should succeed. Bug reports should go [upstream](https://github.com/facebookexperimental/eden).

## Upstream

Consider switching to officially published crates once they are available.