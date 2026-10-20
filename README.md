<div align="center">

# JoiveSer

### Senior Low-Level Systems & Reverse Engineering Architect
**Windows Internals | Memory Topology | Native Runtimes | Binary Deobfuscation**

<br/>

[![C++20/23](https://img.shields.io/badge/C%2B%2B-20%2F23-161b22?style=flat-square&logo=c%2B%2B&logoColor=white)](https://en.cppreference.com/)
[![Rust Systems](https://img.shields.io/badge/Rust-Systems%20%7C%20No__Std-161b22?style=flat-square&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![x86_64 / AArch64](https://img.shields.io/badge/ASM-x86__64%20%7C%20AArch64-161b22?style=flat-square&logo=assemblyscript&logoColor=white)](https://software.intel.com/content/www/us/en/develop/download/intel-64-and-ia-32-architectures-sdm-combined-volumes-1-2a-2b-2c-2d-3a-3b-3c-3d-and-4.html)
[![Windows NTAPI](https://img.shields.io/badge/Windows-NTAPI%20%7C%20Win32-161b22?style=flat-square&logo=windows&logoColor=white)](https://learn.microsoft.com/en-us/windows/win32/)
[![Binary Analysis](https://img.shields.io/badge/Analysis-IDA%20%7C%20Ghidra%20%7C%20x64dbg-161b22?style=flat-square&logo=target&logoColor=white)](https://github.com/JoiveSer)
[![Support Ko-fi](https://img.shields.io/badge/Support-Ko--fi-161b22?style=flat-square&logo=ko-fi&logoColor=FF5E5B)](https://ko-fi.com/joive)

</div>

---

## 🏛️ Architectural Profile

Systems programming and binary analysis engineer focused on the intersection of operating system internals, compiler transformation logic, and executable security analysis. Technical scope encompasses low-overhead runtime scheduling via undocumented NTAPI interfaces, automated static lifting of virtualized bytecode to intermediate representations, and dynamic inspection of stripped, asynchronous binaries.

Primary research vectors target Windows memory virtualization, NUMA-aware multi-core execution scheduling, formal semantics extraction through SMT solvers, and reconstruction of high-level state machines from machine code.

---

## 🔬 Systems Engineering Matrix

| Engineering Domain | Core Technologies & Interfaces | Methodological Focus & Primitives |
| :--- | :--- | :--- |
| **Operating Systems Internals** | C++20/23, Win32 API, NTAPI (`ntdll.dll`) | Direct system calls, APC dispatch, NUMA node binding, heap virtualization, unbuffered I/O |
| **Binary Analysis & RE** | x86_64, AArch64, PE/COFF, iced-x86, Capstone | Disassembly graph slicing, control flow flattening defeat, anti-debug bypassing, vtable recovery |
| **Formal Analysis & Lifting** | Rust (`no_std`), LLVM IR, Symbolic Execution | Semantic synthesis, automated dead-code elimination, bytecode devirtualization, MBA reduction |
| **Serialization & Wire Protocols**| Rust, Zero-copy memory mapping, Protobuf ABI | Protocol reverse engineering, `TcParseTable` / `upb_MiniTable` table reconstruction, schema inference |
| **Differential Execution & Tracing**| WinDbg TTD, Frida Stalker, Unicorn / QEMU | Synchronized lock-step trace alignment, Point of Divergence (PoD) detection, flag delta resolving |

---

## 🚀 Production & Research Artifacts

### 👑 Flagship Systems Core

* **[ClusterShift](https://github.com/JoiveSer/ClusterShift)** — *Universal high-performance Win32 storage optimizer, unbuffered QD32 hardware benchmark & multi-core space analyzer for Windows 10/11.*
  * Implements direct execution control through undocumented NTAPI routines, bypassing standard Win32 file abstraction overhead.
  * Utilizes unbuffered asynchronous I/O completion ports (`FILE_FLAG_NO_BUFFERING | FILE_FLAG_OVERLAPPED`) for deterministic throughput.
  * Engineered in modern C++20 with custom memory-mapped indexing and NUMA-aware multi-core dispatch.

---

### 🛡️ The Reverse Engineering & Systems Suite

* **[ProtoSieve](https://github.com/JoiveSer/ProtoSieve)** — *Zero-knowledge static schema recovery engine for table-driven Protobuf (`TcParseTable` & `upb_MiniTable`) from stripped PE/ELF binaries.*
  * Recovers message field boundaries, wire types, tag identifiers, and packed struct offsets from read-only data without reflection tables.
  * Emits compilable `.proto` schema definitions and structured JSON AST models with zero heap allocation overhead.
  * Engineered in pure Safe Rust with zero-copy memory-mapped PE/ELF ingestion pipelines.

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
  * Analyzes register deltas and flags (`ZF`, `CF`, `SF`), emitting interactive ANSI split-screen diffs, Mermaid graphs, and JSON reports.

* **[VMSmith](https://github.com/JoiveSer/VMSmith)** — *Constraint-guided bytecode devirtualizer & Mixed Boolean-Arithmetic (MBA) micro-synthesizer for VMProtect 3.x / Tigress virtualized routines.*
  * Simulates virtual stack machines (`VSP`/`VIP`/`VREGS`) symbolically, lifting raw virtual bytecode into normalized expression trees.
  * Employs term-rewriting algebraic patterns for instant simplification of complex linear MBA expressions without SMT timeouts.
  * Eliminates VM dispatcher loops, reconstructing clean control-flow graphs, compilable C99 pseudocode, and LLVM IR SSA format.

---

## ☕ Research Funding & Sponsorship

Developing specialized binary analysis toolsets, maintaining disassembler integrations, and conducting low-level systems research requires continuous testing infrastructure and physical hardware platforms. Independent engineering efforts can be sponsored directly via:

[![Support via Ko-fi](https://img.shields.io/badge/Support%20Research-Ko--fi-FF5E5B?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/joive)

---

## 🔬 Technical References & Influences

The architecture and methodologies incorporated across these projects draw foundation from peer research within the low-level security and systems domain:

* **[Axel Souchet (0vercl0k)](https://github.com/0vercl0k)** — Snapshot-based fuzzing architectures (`wtf`), minidump parsing, and rigorous bug triage.
* **[Duncan Ogilvie (mrexodia)](https://github.com/mrexodia)** — Windows debugging internals (`x64dbg`), emulation harnesses, and analysis tooling.
* **[Jonathan Salwan](https://github.com/JonathanSalwan)** — Symbolic execution frameworks (`Triton`), binary lifting methodologies, and instruction synthesis.
* **[hasherezade](https://github.com/hasherezade)** — In-memory PE file inspection (`pe-sieve`), payload extraction, and memory anomaly detection.

---

<div align="center">
<sub>All research and production artifacts are distributed under permissive open-source licenses for security research and systems verification.</sub>
</div>
