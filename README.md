Unofficial snapshots of a subset of crates in [Sapling](https://github.com/facebook/sapling).

## Usage

The crates are prefixed with `esl01-` to avoid conflicts with official publication in the future. So you'll need to use the `esl01-` prefix when specifying dependencies:

```
# Cargo.toml
[dependencies]
esl01-drawdag = "0.3"
```

You can use the non-prefixed names in Rust code. This works because `lib.name` is set in `Cargo.toml` to not have the prefix:

```
// lib.rs
let parsed = drawdag::parse("A..E");
```

## Issues

Bug reports and discussions should go [upstream](https://github.com/facebook/sapling).

## Versions

- 0.3: [Snapshot](https://github.com/facebook/sapling/commit/b805766dd5edef4cee15cb694ae21f85b9bfc2d4) taken on Jan 26, 2023.
