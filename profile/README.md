<p align="center">
  <a href="https://github.com/Tetrodotoxin-Dev/Tetrodotoxin">
    <img src="https://raw.githubusercontent.com/Tetrodotoxin-Dev/Tetrodotoxin/main/extension/media/logo.png" alt="Tetrodotoxin Toolchain" width="100%">
  </a>
</p>

> **The common layer should be meaning, not representation.**

Tetrodotoxin raises several owned language models into one linked semantic
Workspace, using TTX as their shared graph vocabulary, then derives independent
Terminal products from that completed meaning.

Large systems rarely speak only one language. Package manifests, reusable
libraries, application policy, scene state, render contracts, and shaders each
ask different questions. Tetrodotoxin lets each domain keep a language shaped
for its work while participating in one program, editor session, Package graph,
and build.

## One platform, several languages

Each Tetrodotoxin language is a Dialect that owns its grammar and complete domain
meaning. TTX owns only the semantic questions genuinely shared across domains:
identity, resolution, Types, Packs, Layouts, Addressables, Callables, source
locations, and documentation.

Workspace owns lifetime, cross-Dialect linking, completion, and publication. A
Terminal producer then derives only the target facts needed for its product.
LLVM IR, SPIR-V, Archives, editor data, and executables remain outputs rather
than sources of semantic truth.

Raising means participation rather than translation. Concrete language objects
expose TTX contracts on their original identities instead of being copied into
a universal declaration tree.

> **Pull upward every fact that is target neutral and genuinely shared, while
> leaving richer meaning with its concrete owner.**

## Explore Tetrodotoxin

- [Tetrodotoxin](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin) is the main
  language and toolchain repository.
- [Platform overview](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin/tree/main/tetrodotoxin)
  introduces Dialects, Workspaces, Packages, and Terminal products.
- [TTX](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin/tree/main/ttx) defines
  the lexical and semantic vocabulary shared across languages.
- [Language integration](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin/tree/main/tetrodotoxin/language)
  explains how a new Dialect joins the platform.
- [Visual Studio Code extension](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin/tree/main/extension)
  provides the editor and native debugging experience.

## Join the project

Tetrodotoxin is under active research and development. Explore the design,
follow the implementation, or share a concrete use case through
[GitHub Issues](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin/issues).
Project correspondence can be sent to
[contact@tetrodotoxin.dev](mailto:contact@tetrodotoxin.dev).

Tetrodotoxin is available under the
[MIT License](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin/blob/main/LICENSE).
