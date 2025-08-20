# LambdaTesseract

**Founder:** NIKHIL REDDY


**Easy to write. Hard to hack. Fast to compile.**  
This is a _starter repo_ scaffold with an interpreter (Python), a compiler (Rust → WASM/native), a minimal stdlib,
tests, CI/CD, security gates, and proposal (LTP) workflow.

> This is a template for you to push to GitHub and iterate. Nothing here phones home.

## Fast compile, secure-by-default principles
- Compiler and runtime in **Rust** for memory safety and performance.
- **Incremental & parallel** compilation with a content-hash module cache.
- **Effect-typed IO** to constrain capabilities at the type level.
- **Sandboxed** execution for untrusted code (WASM default target).
- **Supply-chain hardening**: lockfiles, checksum verification, and optional Sigstore signing.
- **Continuous fuzzing** and **static analysis** hooks provided in CI template.

## Quick start (local)
```bash
# Interpreter (quick dev loop)
python3 -m venv .venv && source .venv/bin/activate
pip install -r interpreter/requirements.txt
python interpreter/ltrepl.py

# Compiler (Rust)
cd compiler && cargo build
```

## Directory layout
- `spec/` — Language spec skeleton
- `rfcs/` — LambdaTesseract Proposals (LTPs)
- `interpreter/` — Python interpreter (reference semantics)
- `compiler/` — Rust compiler (front/mid/back, IR, incremental cache)
- `runtime/` — Rust runtime (scheduler, tasks, GC/ARC shim)
- `stdlib/` — Core library (Option/Result/List/Map/String/IO/Task)
- `tools/` — ltfmt (formatter), lttest (test runner) stubs
- `lsp/` — Language Server Protocol (TypeScript) scaffold
- `pm/` — Package manager scaffold (`ltpm`)
- `tests/` — Conformance tests and samples
- `.github/workflows/` — CI/CD with security gates

## License
Apache-2.0 (see `LICENSE`)
