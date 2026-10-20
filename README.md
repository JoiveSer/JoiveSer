<div align="center">

# JoiveSer

### Software Architect, Game Modder & Systems Developer
**C# / .NET | Game Modding & Minecraft | High-Performance Systems | Binary Analysis**

<br/>

[![C# / .NET](https://img.shields.io/badge/C%23-Modern%20.NET-161b22?style=flat-square&logo=csharp&logoColor=white)](https://dotnet.microsoft.com/)
[![Minecraft Modding](https://img.shields.io/badge/Minecraft-NeoForge%20Modding-161b22?style=flat-square&logo=curseforge&logoColor=white)](https://github.com/JoiveSer)
[![C++20 Systems](https://img.shields.io/badge/C%2B%2B-20%2F23%20Win32-161b22?style=flat-square&logo=c%2B%2B&logoColor=white)](https://en.cppreference.com/)
[![Rust Tooling](https://img.shields.io/badge/Rust-Systems%20%7C%20Analysis-161b22?style=flat-square&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Web & Guides](https://img.shields.io/badge/Web-Guides%20%26%20Docs-161b22?style=flat-square&logo=markdown&logoColor=white)](https://github.com/JoiveSer)
[![Support Ko-fi](https://img.shields.io/badge/Support-Ko--fi-161b22?style=flat-square&logo=ko-fi&logoColor=FF5E5B)](https://ko-fi.com/joive)

</div>

---

## 🏛️ About & Engineering Focus

Multi-disciplinary software developer and creator. Primary engineering language and core background is **C# / .NET**, spanning application development, game modding ecosystems, high-performance native Windows software, and specialized binary analysis tools.

My work covers a broad spectrum of software engineering:
* **Game Modding & Mechanics:** Minecraft mod development on modern NeoForge, custom trial mechanics, loot pipelines, and game loop integrations.
* **Community Platforms & Web:** Building and curating structured game guides, documentation sites, and web resources.
* **High-Performance Systems:** Windows storage optimization, unbuffered asynchronous I/O completion ports, and direct NTAPI execution engines.
* **Binary Analysis & RE:** Automated decompilation tooling in Rust for stripped binaries, protobuf schema recovery, coroutine linearizers, and bytecode devirtualizers.

---

## 🔬 Skills & Technology Matrix

| Domain | Core Stack & Technologies | Focus & Primitives |
| :--- | :--- | :--- |
| **Core Software Architecture** | C# (.NET 8/9), LINQ, Async/Await, P/Invoke | Object-oriented architecture, native interop, desktop utilities, backend APIs |
| **Game Modding & Mechanics** | Java, Minecraft NeoForge, Game Internals | Custom modifiers, trial mechanisms, event-driven game hooks, dynamic loot registries |
| **Web & Community Resources** | HTML5, CSS3, Markdown, Web Guides | Structured knowledge bases, responsive game documentation, community resource curation |
| **High-Performance Systems** | Modern C++20, Win32 API, NTAPI (`ntdll.dll`) | Direct system calls, NUMA topology binding, unbuffered QD32 hardware benchmarks |
| **Binary Analysis & RE Tooling** | Rust, x86_64, iced-x86, LLVM IR | Zero-knowledge Protobuf extraction, Tokio async desugaring, GBNF struct solving, MBA simplifiers |

---

## 🚀 Projects & Production Artifacts

### 🎮 Game Modding & Community Resources

* **[scavenger-extra-trials](https://github.com/JoiveSer/scavenger-extra-trials)** — *Minecraft NeoForge add-on expanding the Scavenger mod with high-tier modifiers and challenging trial mechanics.*
  * Extends gameplay with custom modifier events, dynamic difficulty scaling, and trial reward mechanics.
  * Built for modern Minecraft modloaders using clean, event-driven NeoForge registries.

* **[CSC-Guides-Fork](https://github.com/JoiveSer/CSC-Guides-Fork)** — *Community game guides and comprehensive documentation portal.*
  * Structured references, walkthroughs, and mechanic breakdowns for community players and modders.
  * Clean, fast web styling designed for quick lookup and navigation.

---

### ⚡ High-Performance Systems & Native Tools

* **[ClusterShift](https://github.com/JoiveSer/ClusterShift)** — *Universal high-performance Win32 storage optimizer, unbuffered QD32 hardware benchmark & multi-core space analyzer for Windows 10/11.*
  * Implements direct execution control through undocumented NTAPI routines, bypassing standard Win32 file abstraction overhead.
  * Utilizes unbuffered asynchronous I/O completion ports (`FILE_FLAG_NO_BUFFERING | FILE_FLAG_OVERLAPPED`) for deterministic throughput.
  * Engineered in modern C++20 with custom memory-mapped indexing and NUMA-aware multi-core dispatch.

---

### 🛡️ Reverse Engineering & Binary Analysis Suite

* **[DeReflect-IR](https://github.com/JoiveSer/DeReflect-IR)** — *SMT-Driven Symbolic Execution Deobfuscator & CFG Reconstruction Engine for Modern .NET (6 / 8 / 9 / 10).*
  * Operates on raw CIL bytecode via AsmResolver 6.0, constructing basic block CFGs and dominance trees (Cooper-Harvey-Kennedy idom).
  * Features an in-memory symbolic SMT execution engine for mathematical control flow deflattening (CFF) and opaque predicate elimination.
  * Reconstructs clean method bodies, repairs MaxStack / exception handling, and inlines encrypted strings and proxy delegates.

* **[ProtoSieve](https://github.com/JoiveSer/ProtoSieve)** — *Zero-knowledge static schema recovery engine for table-driven Protobuf (`TcParseTable` & `upb_MiniTable`) from stripped PE/ELF binaries.*
  * Recovers message field boundaries, wire types, tag identifiers, and packed struct offsets from read-only data without reflection tables.
  * Emits compilable `.proto` schema definitions and structured JSON AST models with zero heap allocation overhead.

* **[DeTokio](https://github.com/JoiveSer/DeTokio)** — *Automated coroutine & async state machine desugaring engine for Rust binaries (`Future::poll` linearizer).*
  * Resolves compiler-generated asynchronous state machines created by Tokio and async runtimes directly from stripped binaries.
  * Demangles optimized async futures by tracing discriminant lifecycle stores to `[self + offset]` and jump tables.
  * Reconstructs C-compatible environment frame layouts and exports linear procedural C pseudocode and Mermaid CFG flowcharts.

* **[LocalRev](https://github.com/JoiveSer/LocalRev)** — *Zero-Hallucination Struct Layout Recovery Engine via Grammar-Constrained (GBNF) Neural Decompilation & Deterministic Memory Synthesis.*
  * Enforces a hard architectural boundary: memory geometry (offsets, member sizes, alignment, and padding) is computed 100% deterministically by the Rust `LayoutSolver`.
  * Couples deterministic layout synthesis with local LLMs (via `llama.cpp` / Ollama) strictly bounded by dynamic GBNF grammars to prevent structural hallucination.
  * Emits compilable C99 / C++20 headers with static assertions (`static_assert`) verifying exact byte offsets.

* **[TraceDiff](https://github.com/JoiveSer/TraceDiff)** — *Execution trace differential analysis platform designed for behavioral divergence mapping & anti-analysis detection.*
  * Ingests deterministic instruction streams (WinDbg TTD, Frida Stalker, Unicorn/QEMU logs) bypassing noisy hardware ring buffers.
  * Synchronizes multi-thousand instruction streams, flags exact Point of Divergence (PoD), and decomposes root-cause branch mutations.
  * Emits interactive ANSI split-screen diffs, Mermaid graphs, and structured JSON reports.

* **[VMSmith](https://github.com/JoiveSer/VMSmith)** — *Constraint-guided bytecode devirtualizer & Mixed Boolean-Arithmetic (MBA) micro-synthesizer for VMProtect 3.x / Tigress virtualized routines.*
  * Simulates virtual stack machines (`VSP`/`VIP`/`VREGS`) symbolically, lifting raw virtual bytecode into normalized expression trees.
  * Employs term-rewriting algebraic patterns for instant simplification of complex linear MBA expressions without SMT timeouts.
  * Eliminates VM dispatcher loops, reconstructing clean control-flow graphs, compilable C99 pseudocode, and LLVM IR SSA format.

---

## ☕ Support & Sponsorship

Developing open-source software, game mods, community resources, and specialized systems tools:

[![Support via Ko-fi](https://img.shields.io/badge/Support-Ko--fi-FF5E5B?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/joive)

---

<div align="center">
<sub>Crafted with passion for C#, game modding, systems architecture, and open-source software.</sub>
</div>
