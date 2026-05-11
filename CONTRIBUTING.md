# Contributing to Shipwright

Thanks for helping improve Ship of Harkinian. This repository combines C++ code, generated asset data, documentation, and platform build scripts, so small focused pull requests are easiest to review.

## Setup

1. Fork the repository and create a branch from `develop`.
2. Clone with submodules, or initialize them after cloning:

```bash
git submodule update --init
```

3. Follow the platform-specific build steps in [docs/BUILDING.md](docs/BUILDING.md).
4. Keep a legally acquired game dump outside the repository. Do not commit ROMs, extracted copyrighted assets, generated `.o2r` or `.otr` files, local saves, build outputs, or personal configuration files.

## Pull Request Guidelines

- Keep each pull request focused on one bug fix, feature, platform change, or documentation update.
- Describe what changed, why it changed, and which platform or workflow it affects.
- Link related issues or discussions when available.
- Include screenshots, logs, or reproduction steps for user-visible changes.
- Update documentation when behavior, setup steps, controls, or packaging workflows change.
- Avoid unrelated formatting churn and generated files unless the change specifically requires regenerating them.

## Code Style

- Match the style of the surrounding C++ and CMake code.
- Run the formatter before opening a pull request when touching C or C++ files:

```bash
./run-clang-format.sh
```

On Windows, use `run-clang-format.ps1`.

- Prefer clear names and small functions over broad rewrites.
- Keep platform-specific logic isolated to the existing platform or build-system boundaries.
- Do not silence warnings unless the pull request explains why the warning is not actionable.

## Validation

Run the checks that match your change:

- Documentation-only changes: review links and Markdown rendering.
- C++ or build-system changes: run the relevant CMake configure and build commands from [docs/BUILDING.md](docs/BUILDING.md).
- Packaging changes: run the relevant `cpack` target or platform packaging workflow when possible.

Mention any checks you could not run in the pull request description.
