# Luma

<p align="center">
  <img src="../assets/luma.png" alt="Luma Logo" width="200"/>
</p>

<p align="center">
  <strong>A modern systems programming language with manual memory control and compile-time safety</strong>
</p>

<p align="center">
  <a href="https://github.com/Luma-Programming-Language/Luma">Compiler</a> •
  <a href="https://bit.ly/lux-discord">Discord</a> •
  <a href="https://github.com/Luma-Programming-Language/Luma/blob/main/docs/docs.md">Documentation</a>
</p>

---

## What is Luma?

Luma is a low-level compiled programming language designed to rival C and C++ in performance while providing modern safety guarantees through static analysis. It combines:

- **🚀 Blazing fast compilation** — 50ms builds for complete applications
- **⚡ C-level performance** — Zero runtime overhead, 24KB binaries
- **🔒 Compile-time safety** — Memory verification without borrow checkers or lifetimes
- **🎯 Explicit control** — Manual memory management with ownership annotations

**Unlike Rust:** No lifetimes, no borrow checker  
**Unlike C/C++:** Memory safety verified at compile time  
**Unlike Go:** No garbage collector, true systems-level control

```luma
@module "main"

@use "memory" as mem

pub const main -> fn() int {
    let buf = mem::calloc(128, 1);
    defer { free(buf); }  // Verified safe at compile time
    
    output("Hello from Luma!\n");
    return 0;
}
```

---

## Performance at a Glance

| Metric | Luma | Rust | C/C++ |
|--------|------|------|-------|
| **Compile Time** | 51ms | 3-5s | 300ms |
| **Binary Size** | 24KB | 150-400KB | 40-80KB |
| **Runtime** | None | None | None |
| **Safety** | Compile-time | Compile-time | Manual |

---

## Organization Structure

This organization houses the complete Luma ecosystem:

### Core Projects

- **[luma](https://github.com/Luma-Programming-Language/Luma)** — The Luma compiler and language specification
- **[luma-std](https://github.com/Luma-Programming-Language/Luma-std)** — Standard library (math, memory, strings, I/O, etc)
- **[luma-docs](https://github.com/Luma-Programming-Language/luma-docs)** — Official documentation and tutorials

### Tooling

- **[luma-vscode](https://github.com/Luma-Programming-Language/Luma/tree/main/src/lsp/language-support)** *(coming soon)* — VS Code extension with syntax highlighting and LSP
- **[luma-lsp](https://github.com/Luma-Programming-Language/Luma/tree/main/src/lsp)** *(coming soon)* — Language Server Protocol implementation
- **[luma-fmt](https://github.com/Luma-Programming-Language/Luma/tree/main/src/lsp/formatter)** *(coming soon)* — Code formatter

### Examples & Learning

- **[luma-examples](https://github.com/luma-lang/luma-examples)** *(coming soon)* — Sample projects and tutorials
- **[awesome-luma](https://github.com/luma-lang/awesome-luma)** *(coming soon)* — Curated list of Luma resources

---

## Getting Started

### Installation

See the [main compiler repository](https://github.com/Luma-Programming-Language/Luma?tab=readme-ov-file#getting-started) for detailed installation instructions.

**Requirements:**
- LLVM 20.0+
- GCC
- Make

### Quick Example

```bash
# Write your first Luma program
echo '@module "main"

pub const main -> fn() int {
    output("Hello, Luma!\n");
    return 0;
}' > hello.lx

# Compile and run
luma hello.lx -name hello
./hello
```

### Learn More

- 📖 [Language Guide](https://github.com/Luma-Programming-Language/Luma?tab=readme-ov-file#luma) — Complete language overview
- 🎓 [Examples](https://github.com/Luma-Programming-Language/Luma/tree/main/tests) — Real-world code samples
- 📚 [API Docs](https://thedevconnor.github.io/Luma/) — Architecture and internals
- 💬 [Discord Community](https://bit.ly/lux-discord) — Get help and share projects

---

## Contributing

Luma is in early development and we welcome contributors!

**Ways to contribute:**

- 🐛 Report bugs or suggest features in the [main repository](https://github.com/Luma-Programming-Language/Luma/issues)
- 📝 Improve documentation and examples
- 🔧 Build tools and editor plugins
- 💻 Contribute to the compiler or standard library
- 🌟 Share your Luma projects with the community

See our [contribution guidelines](https://github.com/Luma-Programming-Language/Luma/blob/main/CONTRIBUTING.md) to get started.

---

## Project Status

**Current Phase:** Early Development

The language core is functional with:

- ✅ Complete lexer, parser, and type system
- ✅ Static memory analysis with ownership tracking
- ✅ LLVM backend for native code generation
- ✅ Working standard library
- ✅ Real-world applications (3D graphics, systems tools)

Check the [project roadmap](https://github.com/Luma-Programming-Language/Luma/blob/main/todo.md) to see what's being worked on.

---

## Community

- **Discord:** [Join our server](https://bit.ly/lux-discord)
- **GitHub:** [luma-lang](https://github.com/Luma-Programming-Language/Luma)
- **Discussions:** [GitHub Discussions]()

---

## License

Projects in this organization are licensed under their respective licenses. See individual repositories for details.

---

<p align="center">
  <strong>Built with ❤️ by the Luma community</strong>
</p>
