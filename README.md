<h1 align="center">Rust-Utils</h1>
<p align="center"><strong>Core Unix CLI Utilities Reimplemented in Rust</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/Rust-1.75+-DEA584?style=flat-square&logo=rust" />
  <img src="https://img.shields.io/badge/Platform-Unix%2FLinux-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" />
</p>

<p align="center">
  Rust reimplementations of essential Unix/Linux command-line utilities. Built as a hands-on exploration of Rust's strengths in systems programming, CLI tooling, and safe low-level file system operations.
</p>

---

## The Motivation

Rust is widely regarded as one of the best languages for building CLI tools — fast startup, zero-cost abstractions, strong type safety, and excellent error handling. Reimplementing core Unix utilities is a practical way to learn the language while working with real-world concerns like file I/O, permissions, directory traversal, and encoding.

## The Utilities

| Utility | Description |
|---|---|
| **`cat`** | Concatenate and display file contents |
| **`ls`** | List directory contents |
| **`cp`** | Copy files and directories |
| **`mv`** | Move or rename files and directories |
| **`mkdir`** | Create directories |
| **`basename`** | Strip directory and suffix from filenames |
| **`base32`** | Encode/decode data in Base32 format |
| **`arch`** | Display the system architecture |

---

## Quick Start

### Prerequisites

- Rust 1.75+
- Cargo

### 1. Clone and build

```bash
git clone https://github.com/prranavv/Rust-Utils.git
cd Rust-Utils

cargo build --release
```

### 2. Run a utility

```bash
cargo run --bin cat -- file.txt
cargo run --bin ls -- /home
cargo run --bin cp -- source.txt dest.txt
cargo run --bin mv -- old_name.txt new_name.txt
cargo run --bin mkdir -- new_directory
cargo run --bin basename -- /path/to/file.txt
cargo run --bin base32 -- input.txt
cargo run --bin arch
```

---

## Tech Stack

| Component | Technology | Purpose |
|---|---|---|
| **Language** | Rust | Memory-safe systems programming |
| **Standard Library** | `std::fs`, `std::io`, `std::path` | File system operations, I/O, path manipulation |
| **Build** | Cargo | Build system and package manager |

---

## FAQ's

**"Why rewrite utilities that already exist?"**
> It's one of the most effective ways to learn a systems language. Each utility is small enough to finish in a sitting but touches real concerns — file permissions, buffered I/O, error propagation, argument parsing — that you'd encounter in any production Rust codebase.

**"Why Rust for CLI tools?"**
> Rust binaries start instantly (no runtime or VM), handle errors explicitly through `Result` types instead of silently failing, and compile to a single static binary with no dependencies. These properties make it ideal for command-line tools where correctness and startup latency matter.

**"Are these drop-in replacements for GNU coreutils?"**
> No — these are simplified implementations focused on the core functionality of each utility. They don't aim for full GNU compatibility or POSIX compliance. For a production-grade effort in that direction, see [uutils/coreutils](https://github.com/uutils/coreutils).

---

## License

MIT — see [LICENSE](LICENSE) for details.

---

<p align="center">
  <sub>Built by <a href="https://github.com/prranavv">prranavv</a></sub>
</p>