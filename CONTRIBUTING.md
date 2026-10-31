# Contributing to P-Code VM

Thanks for helping improve the P-Code VM IntelliJ plugin.

## Report issues and suggest features

Use the GitHub issue templates for bugs and feature requests. For bugs, include the IntelliJ IDEA and plugin versions, reproduction steps, and a minimal P-Code example when possible. Do not share private data or credentials.

## Propose a change

1. Open an issue first for substantial changes so the scope can be discussed.
2. Create a focused branch and make the smallest change that solves the problem.
3. Add or update tests and user documentation when relevant.
4. Open a pull request describing the change and how you verified it.
5. Wait for review before merging.

## Project scope

This repository contains the public IntelliJ plugin integration. The P-Code virtual machine implementation is maintained separately and is not part of this repository. Do not add private VM source, unobfuscated binaries, or credentials to pull requests.

Some local builds require an authorized VM binary supplied separately. If you cannot build because that dependency is unavailable, explain this in your pull request rather than committing the binary.

## License

Contributions to this repository are submitted under its MIT license unless explicitly agreed otherwise. The separately maintained VM is not covered by this repository's MIT license.
