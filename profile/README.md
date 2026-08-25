<p align="center">
  <a href="https://github.com/Tetrodotoxin-Dev/Tetrodotoxin">
    <img src="https://raw.githubusercontent.com/Tetrodotoxin-Dev/Tetrodotoxin/main/extension/media/logo.png" alt="Tetrodotoxin Toolchain" width="100%">
  </a>
</p>

> **The common layer is meaning, not representation.**

Tetrodotoxin is an extensible language and toolchain platform for projects that
speak more than one language. It lets purpose-built languages keep the meaning
that makes them useful while sharing one Package graph, one editor experience,
one linked understanding of the program, and one path to finished products.

Software already contains languages for composition, behavior, scenes, shaders,
assets, and deployment. Those languages often remain data files whose rules are
reimplemented by every tool, or they grow into isolated compilers with their own
private model of the project. Tetrodotoxin gives them a place to meet without
flattening them into one universal language first.

## One project, several languages

Imagine adding a scene language without also inventing another type system,
package manager, editor protocol, build driver, and shader bridge. The scene can
own lifecycle and signals, reuse ordinary Library code for behavior, and meet
Render and Shader around graphics. The editor follows those relationships
through the same identities used by the build.

Tetrodotoxin calls each focused language a **Dialect**. A Dialect owns the
grammar and complete meaning of its domain. TTX provides a compact shared
vocabulary for the semantic questions that genuinely cross domains, including
identity, resolution, Types, Packs, Layouts, Addressables, Callables,
documentation, and Interfaces.

This is **raising by participation**. The original objects created by each
language take part in a linked semantic Workspace instead of being copied into a
universal declaration tree or compiler IR.

> **Pull upward every fact that is target neutral and genuinely shared, while
> leaving richer meaning with its concrete owner.**

## One understanding, many products

The same semantic graph supports navigation, completion, Packages, compilation,
and durable reconstruction. Each tool asks the real semantic owners for the
context it needs rather than maintaining another account of the program.

Once that meaning is complete, independent **Terminals** carry it into products
for other consumers. LLVM IR, SPIR-V, Package Archives, formatted source, native
programs, and application bundles can all begin from the same Workspace.
Lowering remains in the representation domains built for it, while the authored
languages keep their original meaning.

Dialects compose what a Tetrodotoxin toolchain understands. Terminals compose
what it can produce. Together they make a specialized language part of a
complete SDK rather than another parser attached to the edge of a project.

## Explore Tetrodotoxin

* [Tetrodotoxin](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin) is the main
  language and toolchain repository.
* [Project philosophy](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin/blob/main/PHILOSOPHY.md)
  explains why the architecture takes this unusual shape.
* [Contributing](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin/blob/main/CONTRIBUTING.md)
  offers practical guidance for extending and reviewing the project.
* [TTX](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin/tree/main/ttx) defines
  the semantic graph vocabulary shared across languages.
* [Visual Studio Code extension](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin/tree/main/extension)
  provides the editor and native debugging experience.

## Join the project

Tetrodotoxin is developed in public, and concrete use cases are especially
valuable. Each new domain helps reveal which meaning belongs in a Dialect and
which ideas have become genuinely common.

Share an idea, report a problem, or follow the work through
[GitHub Issues](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin/issues).
Project correspondence can be sent to
[github@tetrodotoxin.dev](mailto:github@tetrodotoxin.dev).

Tetrodotoxin is available under the
[MIT License](https://github.com/Tetrodotoxin-Dev/Tetrodotoxin/blob/main/LICENSE).
