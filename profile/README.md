<p align="center">
  <a href="https://tetrodotoxin.dev">
    <img src="https://raw.githubusercontent.com/tetrodotoxin-dev/Tetrodotoxin/main/extension/media/logo.png" alt="Tetrodotoxin Toolchain" width="100%">
  </a>
</p>

Tetrodotoxin is a systems and tooling project about making independently built
components useful to each other. A renderer, compiler service or language runtime
should be able to offer its capabilities without requiring every consumer to
adopt its storage, implementation language or private object model.

With TTX, a tool exposes its capabilities through driver-style interfaces that
other languages and runtimes can use without adopting its implementation.
Binding checks both the contract being requested and the layouts of its data
and callable interface, so separately built components can establish how to
work together before making a call.

## See it in Godot

Check out the [live Godot lab running in WebAssembly](https://tetrodotoxin.dev/lab/)
or [build it locally](https://github.com/tetrodotoxin-dev/Godot#run-locally).
The lab brings GDScript, native C++ and CUDA image providers into the same scene.
They offer the same operations
through TTX contracts while keeping their algorithms and storage separate.
Changing an overlay updates the composition without recomputing an unrelated
filter. Independent C and C++ modules also expose classes through a reusable
Godot extension.

You can try the CPU and GDScript providers directly in the browser. CUDA requires
the [native setup](https://github.com/tetrodotoxin-dev/Godot) with a compatible GPU and toolkit.

## Build and wrap toolchains with TTX

TTX separates APIs needed to connect systems into three layers:

* **Data** describes concrete data and callable forms, compiles their canonical
  representations, and provides protocols for accessing values.
* **Semantic** identifies contracts by UUID and negotiates their interfaces and
  data access. Recognizing a contract and agreeing on a usable interface are
  separate questions.
* **Concept** exposes Abstracts that consumers can navigate and query for
  policies. An implementation can answer the questions a consumer understands
  without exposing its private classes.

## Project Split

| Project | Responsibility |
| --- | --- |
| [Perimortem](https://github.com/tetrodotoxin-dev/Perimortem) | Memory, containers, serialization, image storage and system services. |
| [Toolchain](https://github.com/tetrodotoxin-dev/Toolchain) | Shared Bazel rules, compiler and SDK acquisition, validation and release packaging. |
| TTX | The Data, Semantic and Concept foundation, independent of the source toolchain. |
| [Tetrodotoxin](https://github.com/tetrodotoxin-dev/Tetrodotoxin) | Source dialects, semantic models and the compiler and toolchain work built on TTX. |
| Photophore | Vulkan rendering, windowing and platform input. |
| [CUDA](https://github.com/tetrodotoxin-dev/CUDA) | CUDA compilation and execution services exposed through TTX contracts. |
| [Godot](https://github.com/tetrodotoxin-dev/Godot) | The reusable Godot bridge and the demonstration that exercises these interfaces. |

## Join the work

Concrete integration problems are welcome along with any contributions. Share an idea or report a problem through
[GitHub Issues](https://github.com/tetrodotoxin-dev/Tetrodotoxin/issues), or contact
[github@tetrodotoxin.dev](mailto:github@tetrodotoxin.dev).

Tetrodotoxin Projects are available under the
[MIT License](https://github.com/tetrodotoxin-dev/Tetrodotoxin/blob/main/LICENSE).
