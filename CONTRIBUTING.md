# Contributing to Oxide

Thanks for helping build Oxide! This guide applies to every repository in the
[oxide-hq](https://github.com/oxide-hq) organization unless a repository has its own.

## Before you start

- **Bugs:** search existing issues first, then open one with the bug report template and a minimal
  reproduction.
- **Features and API changes:** open an issue or a [discussion](https://github.com/oxide-hq/oxide-framework/discussions)
  before writing code, so we can agree on the design. Oxide's goal is Laravel-style ergonomics with
  compile-time guarantees; proposals should keep both.
- **Security issues:** do not open a public issue. Follow the [security policy](SECURITY.md).

## Development setup

You need stable Rust (each repository pins it in `rust-toolchain.toml`) and
[`just`](https://github.com/casey/just). Each repository's README lists its exact commands; for
`oxide-framework`:

```bash
just ci     # fmt check + clippy -D warnings + tests
```

## Pull requests

1. Fork the repository and branch from `main`.
2. Keep each pull request focused on one change. Add tests for new behaviour and update rustdoc
   and the README when public APIs change.
3. Make sure `just ci` passes. CI runs the same checks plus an MSRV build and `cargo deny`.
4. Fill in the pull request template. Call out breaking changes explicitly.
5. Pull requests are squash-merged; the PR title becomes the commit title, so make it a clear
   imperative sentence (for example "Add JSON:API error renderer").

## Coding conventions

- `unsafe` code is forbidden workspace-wide.
- Clippy runs with `pedantic` enabled; fix warnings rather than silencing them, and justify any
  `#[allow]` with a comment.
- Prefer compile-time guarantees (types, traits, derives) over runtime checks.
- Public items need rustdoc.

## License

By contributing, you agree that your contributions are dual-licensed under MIT OR Apache-2.0, as
described in each repository's README, without any additional terms or conditions.

Everyone participating is expected to follow the [code of conduct](CODE_OF_CONDUCT.md).
