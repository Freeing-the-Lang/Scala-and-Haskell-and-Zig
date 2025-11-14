# Scala-and-Haskell-and-Zig  
**Hybrid Language Experiment — Scala Semantics + Haskell Purity + Zig-level Control**

This repository explores a **triple-fusion language model** combining:

- **Scala** — Pattern matching, expression orientation, ADT-style structure  
- **Haskell** — Purity, recursion, evaluation model  
- **Zig** — Low-level control, predictability, C-free system design  

The goal is to observe how these three very different philosophies behave when merged
into a single experimental interpreter and runtime.

This is part of the **Freeing-the-Lang** ecosystem:  
A collection of experimental hybrid languages, compiler prototypes,  
meaning-level runtimes, and 3-OS reproducible builds.

---

## ✨ Concept

This mini-language aims to unify:

### ✔ Scala-like features
- Pattern matching (`match { case ... }`)
- Expression-first constructs  
- Algebraic data type-style nodes  

### ✔ Haskell-like features
- Pure evaluation  
- Function-based recursion  
- Minimal mutable state  

### ✔ Zig-like features
- No hidden control  
- Predictable low-level behavior  
- Build-anywhere (Linux / macOS / Windows)  
- C/LLVM 의존도 최소화  

The interpreter itself is intentionally very small, readable, and extendable —
so we can test language combinations quickly.

---

## 🛠 Directory Structure




src/
Lexer.hs          -- (optional) tokenization
Parser.hs         -- constructs AST nodes
Evaluator.hs      -- pure recursive evaluator
Main.hs           -- entry point
examples/
demo.szh          -- sample program
dist/
slh (binary)      -- generated after build
proof/
proofledger-OS.txt



---

## 🚀 Build (3OS Auto Build)

This repository is configured with **automatic 3-OS build pipelines**:

- Ubuntu  
- macOS  
- Windows  

Each push to `main` triggers:

1. Full rebuild on all OS  
2. Interpreter compilation  
3. Example execution (non-Windows)  
4. ProofLedger generation  
5. Artifact upload  
6. Automatic Clean Release packaging  

No manual steps required.

---

## 📜 ProofLedger System

Each build generates a reproducible ledger:




proof/proofledger-Linux.txt
proof/proofledger-macOS.txt
proof/proofledger-Windows.txt



Ledger includes:

- OS info  
- Commit hash  
- Timestamp  
- SHA-256 of all build outputs  
- SHA-256 of all source files  
- SHA-256 of examples  

This provides transparent, reproducible build integrity.

---

## ▶ Running

After build:

```bash
./dist/slh examples/demo.szh



The sample example demonstrates:




Scala-style operators


Haskell-style recursion


Zig-style control and clarity





📦 Automatic Releases


The workflow automatically:




Creates a timestamp version tag


Collects all artifacts from all OS


Bundles everything into one unified ZIP


Publishes GitHub Release


Prevents infinite-loop triggers via tags-ignore




Every release is self-contained and reproducible.



🧩 Why This Combination?




Language
Contribution




Scala
Pattern matching + functional expression design


Haskell
Pure evaluation + recursion model


Zig
Low-level safe control + predictable execution




This fusion provides high-level semantics + low-level determinism,

a rare and interesting intersection.



🔮 Future Expansions




Pattern matching DSL


Meaning-level intermediate form


Zig-powered backend runtime


Multi-Main language bridging


Heap-Hop edition reduction rules


RustSpec compatibility layer


Interpreter → Transpiler chain





🌍 Part of Freeing-the-Lang Ecosystem


This project lives alongside:




Scala-like-Haskell


Haskell-like-Rust


Zig-like-Java


Pure-Rust-No-LLVM


Go-like-Rust


Rust-like-Ruby


And 60+ other experimental hybrid languages




Each repository explores a different fusion model or runtime approach.



License


MIT License.

Free to fork, extend, rewrite, or replace.



---

