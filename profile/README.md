<p align="center">
  <a href="https://tetrodotoxin.dev">
    <img src="https://raw.githubusercontent.com/tetrodotoxin-dev/Tetrodotoxin/main/extension/media/logo.png" alt="Tetrodotoxin Toolchain" width="100%">
  </a>
</p>

Tetrodotoxin is a systems and tooling project about making independently built
components useful to each other. A renderer, compiler service or language runtime
should be able to offer its capabilities without requiring every consumer to
adopt its storage, implementation language or private object model.

TTX provides the foundation for that exchange. The participants agree on what a
contract means and check the concrete data and callable representations they
will use. Each provider keeps control of how it does the work. This lets a
consumer use an implementation it was not built alongside, while checking the
interface before calling through it.

## See it in Godot

The [Godot example](https://tetrodotoxin.dev/lab/) brings GDScript, native C++
and CUDA image providers into the same scene. They offer the same operations
through TTX contracts while keeping their algorithms and storage separate.
Changing an overlay updates the composition without recomputing an unrelated
filter. Independent C and C++ modules also expose classes through a reusable
Godot extension.

You can try the CPU and GDScript providers directly in the browser. CUDA requires
the native setup with a compatible GPU and toolkit; the browser reports that
capability as unavailable. The [Godot repository](https://github.com/tetrodotoxin-dev/Godot)
contains the scene, providers and instructions for running or extending it.

## How the pieces fit together

TTX separates the agreements needed to connect those systems into three layers:

* **Data** describes concrete data and callable forms, compiles their canonical
  representations, and provides protocols for accessing values.
* **Semantic** identifies contracts by UUID and negotiates their interfaces and
  data access. Recognizing a contract and agreeing on a usable interface are
  separate questions.
* **Concept** exposes Abstracts that consumers can navigate and query for
  policies. An implementation can answer the questions a consumer understands
  without exposing its private classes.

The [TTX overview](https://tetrodotoxin.dev/ttx/) explains those layers in more
detail. The implementation is being separated into repositories around these
responsibilities:

| Project | Responsibility |
| --- | --- |
| [Perimortem](https://github.com/tetrodotoxin-dev/Perimortem) | Memory, containers, serialization, image storage and system services. |
| [Toolchain](https://github.com/tetrodotoxin-dev/Toolchain) | Shared Bazel rules, compiler and SDK acquisition, validation and release packaging. |
| TTX | The Data, Semantic and Concept foundation, independent of the source toolchain. |
| [Tetrodotoxin](https://github.com/tetrodotoxin-dev/Tetrodotoxin) | Source dialects, semantic models and the compiler and toolchain work built on TTX. |
| Photophore | Vulkan rendering, windowing and platform input. |
| [CUDA](https://github.com/tetrodotoxin-dev/CUDA) | CUDA compilation and execution services exposed through TTX contracts. |
| [Godot](https://github.com/tetrodotoxin-dev/Godot) | The reusable Godot bridge and the demonstration that exercises these interfaces. |

TTX and Photophore repository publication is still in progress.

## Where the work is going

The source toolchain applies the same approach to language and compiler services.
The goal is for each language to contribute its own semantics while editor tools,
build systems and execution backends follow the relationships between them.
Cross-language navigation, reusable build tools and reconstructable Packages are
part of that work. The source and Package systems are still being reworked;
there is no published Puffer SDK to install yet. The [Puffer page](https://tetrodotoxin.dev/puffer/)
describes that direction.

The [research](https://tetrodotoxin.dev/research/) follows the practical question
behind these examples: how much integration knowledge can a good interface carry
for the next person or tool using it? Performance measurements, provider
substitution and work by independent coding agents help expose where the design
still relies on context that its interfaces do not express. The
[background](https://tetrodotoxin.dev/docs/design/) explains how the project grew
out of runtime and tooling work.

## Join the work

Concrete integration problems are especially useful because they reveal where
an interface makes reuse easier and where it still leaves too much work to the
consumer. Share an idea or report a problem through
[GitHub Issues](https://github.com/tetrodotoxin-dev/Tetrodotoxin/issues), or contact
[github@tetrodotoxin.dev](mailto:github@tetrodotoxin.dev).

Tetrodotoxin is available under the
[MIT License](https://github.com/tetrodotoxin-dev/Tetrodotoxin/blob/main/LICENSE).
