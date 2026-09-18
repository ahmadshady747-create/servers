# GAMA MCP Server

Official Model Context Protocol (MCP) server for **GAMA Engine** — Biomechanical, Spatial & Multi-Dimensional Hyper-Physics Simulation Engine (2D/3D/4D/5D) with GAMA-Forge Procedural Modeling.

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue.svg)](https://modelcontextprotocol.io)
[![Release](https://img.shields.io/github/v/release/ahmadshady747-create/gama-binaries?label=gama-binaries)](https://github.com/ahmadshady747-create/gama-binaries/releases/latest)
[![License](https://img.shields.io/badge/license-Apache--2.0-green.svg)](LICENSE)

GAMA is an ultra-high performance physics simulation and spatial computation engine designed for AI agents, physics-driven simulations, procedural generation, and game worlds.

---

## 🌟 Key Capabilities

1. **Multi-Dimensional Hyper-Physics (2D to 5D):**
   - Deterministic spatial simulation across Euclidean 2D, 3D, 4D, and 5D manifolds.
   - Clifford algebra rotors, 4D vector projections, and N-dimensional SAT collision solvers.
2. **GAMA-Forge Procedural Modeling & CSG:**
   - 3D Signed Distance Fields (SDF), boolean constructive solid geometry (CSG), smooth blending (`opSmoothUnion`), watertight polygonal mesh extraction, and binary glTF 2.0 (`.glb`) export.
3. **Biomechanical & Kinetic Controllers:**
   - SAT collision solver, momentum conservation, facial deformation simulation, and motion matching.
4. **Spatial Acoustics & Dynamic Raytracing:**
   - Real-time acoustic bounce tracing, occlusion simulation, and adaptive spatial audio synthesis.
5. **Zero-GC & Microsecond Invariants:**
   - Pre-allocated entity pools, vectors, and matrices with zero dynamic allocations inside hot simulation loops.

---

## 📦 Distribution & Binaries

Pre-compiled, standalone release distributions for GAMA are hosted on the official binary repository:
- **Download Latest Release:** [gama-binaries Releases (v1.0.0)](https://github.com/ahmadshady747-create/gama-binaries/releases/latest)
  - Release Package: [`gama-v1.0.0-dist.zip`](https://github.com/ahmadshady747-create/gama-binaries/releases/download/v1.0.0/gama-v1.0.0-dist.zip)
  - Integrity Checksums: [`SHA256SUMS.txt`](https://github.com/ahmadshady747-create/gama-binaries/releases/download/v1.0.0/SHA256SUMS.txt)

---

## 🚀 Quickstart

### Running via npx

```bash
npx -y gama-mcp-server
```

On Windows (Command Prompt / PowerShell):
```cmd
npx -y gama-mcp-server
```

### Running Native Engine

```bash
# Set custom GAMA binary location for the MCP server wrapper
export GAMA_BIN_PATH="/path/to/gama"
```

---

## ⚙️ MCP Client Configuration

### Claude Desktop

Add GAMA to your `claude_desktop_config.json`:

#### macOS / Linux:
```json
{
  "mcpServers": {
    "gama": {
      "command": "npx",
      "args": ["-y", "gama-mcp-server"]
    }
  }
}
```

#### Windows:
```json
{
  "mcpServers": {
    "gama": {
      "command": "cmd",
      "args": ["/c", "npx", "-y", "gama-mcp-server"]
    }
  }
}
```

#### Standalone Native Distribution Configuration:
```json
{
  "mcpServers": {
    "gama": {
      "command": "C:\\path\\to\\gama.exe",
      "args": ["mcp"]
    }
  }
}
```

---

## 🛠️ Tool Catalog (48 Native Tools)

| Subsystem | Key Tools | Description |
| :--- | :--- | :--- |
| **Multi-Dimensional Physics** | `gama_simulate_2d`, `gama_simulate_3d`, `gama_simulate_4d`, `gama_simulate_5d` | Discrete physics step integration across 2D, 3D, 4D, and 5D coordinate frames |
| **4D / Clifford Mathematics** | `gama_rotate_4d_vector`, `gama_project_4d`, `gama_clifford_rotor` | 4D hyper-rotations, perspective stereographic projections, and bivector rotors |
| **GAMA-Forge Procedural CSG** | `forge_create_sdf_primitive`, `forge_apply_operator`, `forge_apply_csg`, `forge_extract_mesh`, `forge_export_asset`, `forge_validate_manifold` | Procedural Signed Distance Fields, boolean operations, watertight mesh extraction, and GLB export |
| **Biomechanical & Kinematics** | `gama_facial_simulate_tick`, `gama_facial_evaluate_ssss`, `gama_motion_matching_query`, `gama_motion_inertialize`, `gama_rigging_autorig` | Biomechanical muscle simulations, facial deformation, inertialization, and autorigging |
| **Spatial & Acoustic Simulation** | `gama_spatial_acoustic_raytrace`, `gama_synthesize_audio`, `gama_audio_adaptive_step` | Real-time impulse response raytracing, reflection modeling, and procedural audio synthesis |
| **Continuous Dynamics & Materials** | `gama_fdtd_em_step`, `gama_cosserat_step`, `gama_soil_dem_step`, `gama_granular_step`, `gama_voronoi_fracture`, `gama_terrain_blast` | Finite-difference time-domain EM, Cosserat rods, discrete element soil, and Voronoi fracture |
| **Streaming & Telemetry** | `gama_streaming_query_octree`, `gama_streaming_shift_origin`, `gama_inspector_telemetry`, `gama_benchmark_master` | Hierarchical octree queries, floating-point origin shifts, and telemetry profiling |

---

## 📜 License

Apache-2.0 License.
