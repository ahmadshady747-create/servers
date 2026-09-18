# LOCUS MCP Server

Official Model Context Protocol (MCP) server for **LOCUS Engine** — The Deterministic AST Safety Guard, Verification Engine & Sovereign Code Agent Guardrails.

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue.svg)](https://modelcontextprotocol.io)
[![Release](https://img.shields.io/github/v/release/ahmadshady747-create/locus-binaries?label=locus-binaries)](https://github.com/ahmadshady747-create/locus-binaries/releases/latest)
[![License](https://img.shields.io/badge/license-Apache--2.0-green.svg)](LICENSE)

LOCUS provides deterministic guardrails for AI coding agents across multiple programming languages (Rust, TypeScript, JavaScript, TSX/JSX, Svelte, Astro, Vue, Python). It enforces strict pre-generation contract synthesis, token-efficient AST slicing, surgical verified patching, 32-pass AST safety checks, and ACID multi-file transactions.

---

## 🌟 Key Capabilities

1. **Deterministic AST Safety Guard (32-Pass Verification):**
   - Validates code across syntax, memory safety, async lock balance, hook rules, and secret leaks before disk writes.
2. **Intent Synthesis & Contract Scaffolding:**
   - Synthesizes formal contracts and invariants before modifying or generating code.
3. **Surgical Patching & Blast Radius Analysis:**
   - Evaluates downstream impacts on caller symbols across multi-file repositories.
4. **ACID Workspace Transactions:**
   - Full staging, in-memory isolation, atomic commit, and instant rollback.
5. **SSA Taint Tracking & Mathematical Proofs:**
   - Inter-procedural taint flow analysis and Weakest Precondition (WP) formal verification.

---

## 📦 Distribution & Binaries

Pre-compiled, standalone release binaries for LOCUS are distributed via the official binary repository:
- **Download Latest Release:** [locus-binaries Releases (v1.0.0)](https://github.com/ahmadshady747-create/locus-binaries/releases/latest)
  - Windows x64: [`locus.exe`](https://github.com/ahmadshady747-create/locus-binaries/releases/download/v1.0.0/locus.exe) / [`locus-v1.0.0-windows-x64.zip`](https://github.com/ahmadshady747-create/locus-binaries/releases/download/v1.0.0/locus-v1.0.0-windows-x64.zip)
  - Integrity Checksums: [`SHA256SUMS.txt`](https://github.com/ahmadshady747-create/locus-binaries/releases/download/v1.0.0/SHA256SUMS.txt)

---

## 🚀 Quickstart

### Running via npx

```bash
npx -y locus-mcp-server
```

On Windows (Command Prompt / PowerShell):
```cmd
npx -y locus-mcp-server
```

### Running Native Binary

```bash
# Direct execution
./locus mcp

# Set custom binary location for the MCP server wrapper
export LOCUS_BIN_PATH="/path/to/locus"
```

---

## ⚙️ MCP Client Configuration

### Claude Desktop

Add LOCUS to your `claude_desktop_config.json`:

#### macOS / Linux:
```json
{
  "mcpServers": {
    "locus": {
      "command": "npx",
      "args": ["-y", "locus-mcp-server"]
    }
  }
}
```

#### Windows:
```json
{
  "mcpServers": {
    "locus": {
      "command": "cmd",
      "args": ["/c", "npx", "-y", "locus-mcp-server"]
    }
  }
}
```

#### Standalone Native Executable Configuration:
```json
{
  "mcpServers": {
    "locus": {
      "command": "C:\\path\\to\\locus.exe",
      "args": ["mcp"]
    }
  }
}
```

---

## 🛠️ Tool Catalog (30 Native Sovereign Tools)

| Tool Name | Scope & Description |
| :--- | :--- |
| `check_safety` | 32-pass deterministic AST safety verification (leaks, locks, hooks, invariants) |
| `synthesize_contract` | Synthesizes formal contracts and invariant checklists before generation |
| `extract_intent_slice` | Extracts minimal AST context slice (<0.25ms) based on intent |
| `prepare_context` | Combined high-throughput intake (AST skeleton, slice, blast radius) |
| `verified_patch` | Atomic in-memory verification -> full file check -> disk commit |
| `verify_contract` | Validates implementation against synthesized formal contracts |
| `get_blast_radius` | Traces downstream callers and calculates break risk score |
| `patch_symbol` | Surgical symbol replacement preserving formatting and comments |
| `resolve_symbol` | Polyglot symbol definition and scope resolution |
| `find_references` | Finds all usages and call sites of a symbol across workspace |
| `begin_tx` | Opens an ACID workspace transaction with isolated staging buffer |
| `stage_tx` | Stages file mutations inside an active ACID transaction |
| `commit_tx` | Atomically commits staged mutations to disk |
| `rollback_tx` | Aborts transaction and discards staged modifications |
| `auto_remediate` | Deterministic AST self-healing rewriter for detected violations |
| `acquire_symbol_lease` | Distributed lease locking on specific code symbols |
| `release_symbol_lease` | Releases acquired symbol lease |
| `renew_symbol_lease` | Extends symbol lease expiration TTL |
| `acquire_subtree_lease`| Wildcard directory/subtree lease lock for swarm concurrency |
| `verify_occ_token` | Optimistic Concurrency Control token verification |
| `morph_ast` | Deterministic AST rewriter for imports, signatures, and blocks |
| `query_cst` | Lossless Concrete Syntax Tree pattern matching |
| `trace_taint_flow` | Inter-procedural SSA data-flow taint propagation analysis |
| `audit_taint_path` | Deep source-to-sink vulnerability audit |
| `simd_vector_search` | AVX2/NEON SIMD-accelerated code embedding search |
| `hybrid_search` | Combined lexical and semantic AST graph retrieval |
| `semantic_analyze` | Deep semantic symbol reachability analysis |
| `skeletonize` | Generates ultra-compressed AST interface skeleton |
| `index_graph` | Reindexes repository dependency graph into memory |
| `verify_proof` | Formal proof verification with SHA-256 validation certificates |

---

## 📜 License

Apache-2.0 License.
