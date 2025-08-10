
# Forge Compiler Toolchain

Forge is a modular compiler toolchain written in Go. It aims to provide a full pipeline from preprocessing to code generation, supporting C-like languages and extensible for new frontends and backends.

## Features

- C-like preprocessor with macro replacement and file inclusion
- Lexical analysis (lexer/tokenizer)
- Parsing (AST builder)
- Semantic analysis (type checking, symbol table)
- Code generation (assembly, bytecode, or other targets)
- Cycle detection for includes
- Simple, extensible design

## Project Structure

```
cmd/forgec/         # Compiler CLI entry point
internal/cpreproc/  # Preprocessor
internal/lexer/     # Lexical analysis
internal/parser/    # Syntax analysis
internal/ast/       # AST definitions
internal/semantic/  # Semantic analysis
internal/codegen/   # Code generation
```

## Development

- Extend each stage (preprocessor, lexer, parser, etc.) as needed
- Add more macro types or conditional compilation
- Add tests for each stage in `*_test.go` files
- Use a logger for diagnostics and debugging

## License

MIT License
