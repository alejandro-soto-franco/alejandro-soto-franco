# Alejandro Soto Franco

I implement mathematics. Differential geometry, stochastic analysis and PDE theory, as Rust libraries you can run, Lean developments you can check, and the GPU compilers underneath both.

Founding Principal at [Holonomy Securities](https://holonomysecurities.com), a three-person team building systematic trading engines on a shared platform substrate. Previously a trading strategies developer at Anti Capital in New York. BS/MSE Biomedical Engineering, Johns Hopkins University.

[![Website](https://img.shields.io/badge/sotofranco.dev-000?style=flat-square&logo=vercel&logoColor=white)](https://sotofranco.dev)

## Formal methods and proof tooling

| Repository | Language | What it does |
|---|---|---|
| [`proofsense`](https://github.com/alejandro-soto-franco/proofsense) | Rust + Lean 4 | Proof-linting. Lean answers whether a proof typechecks; proofsense answers whether it matches the source it claims to formalise. The English rendering is a deterministic fold over the declaration's own type expression, so a model never writes the claim it judges. |
| [`EllipticPDE`](https://github.com/alejandro-soto-franco/EllipticPDE) | Lean 4 | Second-order elliptic equations on Mathlib: existence and uniqueness, the Gårding inequality, the Fredholm alternative, spectral compactness, interior $H^2$ regularity. No `sorry`; axioms limited to the standard three. |
| [`Meridian`](https://github.com/alejandro-soto-franco/Meridian) | Lean 4 | Metaprogramming toolkit: sorry inventory with Mathlib `DiscrTree` coverage, dependency graphs, gap reports, counterexample search, type-class diagnostics, IDA* proof search. |
| [`meridian-vscode`](https://github.com/alejandro-soto-franco/meridian-vscode) | TypeScript | VS Code extension over Meridian. |
| `3d-navier-stokes` (private) | Lean 4 | Chapter-scale formalisation of 3D Navier-Stokes regularity theory, on a three-track architecture with symbolic and numerical companions. |

## Compilers and GPU

| Repository | Language | What it does |
|---|---|---|
| [`spirv-oxide`](https://github.com/alejandro-soto-franco/spirv-oxide) | Rust | Rust to SPIR-V compiler through the Pliron MLIR framework. Cross-vendor sibling of the PTX path. |
| [`cubecl-cuda-oxide`](https://github.com/alejandro-soto-franco/cubecl-cuda-oxide) | Rust | CubeCL backend compiling kernels to PTX through cuda-oxide. Pure-Rust GPU JIT, no nvrtc. |
| [`ferrum-gpu`](https://github.com/alejandro-soto-franco/ferrum-gpu) | Rust + Python | Pure-Rust GPU compute substrate with Python bindings. |
| [`gpufft`](https://github.com/alejandro-soto-franco/gpufft) | Rust | Unified GPU FFT: VkFFT on Vulkan, cuFFT on CUDA, one trait over both. |
| [`elworthy`](https://github.com/alejandro-soto-franco/elworthy) | Rust + Python | JIT compiler. Symbolically differentiates SDE coefficients and lowers a Monte Carlo inner loop into a single Cranelift kernel, one path per SIMD lane. |
| [`kloeden`](https://github.com/alejandro-soto-franco/kloeden) | C++ + Rust | Hand-written SIMD C++ against Rust on LLVM and Cranelift, over SDE schemes and Monte Carlo Greeks. |

Upstream compiler work on [NVlabs/cuda-oxide](https://github.com/NVlabs/cuda-oxide) is listed below.

## Stochastic analysis, geometry and simulation

| Repository | Language | What it does |
|---|---|---|
| [`cartan`](https://github.com/alejandro-soto-franco/cartan) | Rust + Python | Riemannian geometry, Lie-group optimisation, and stochastic analysis on manifolds. |
| [`pathwise`](https://github.com/alejandro-soto-franco/pathwise) | Rust + Python | Simulation and calibration of non-Markovian stochastic differential equations. |
| [`hurst`](https://github.com/alejandro-soto-franco/hurst) | Rust | Rough volatility on the correlation manifold: fractional processes and Hurst estimation on SPD(N). |
| [`volterra`](https://github.com/alejandro-soto-franco/volterra) | Rust + Python | Covariant active-nematics solver on simplicial meshes, through discrete exterior calculus. |
| [`vonkarman`](https://github.com/alejandro-soto-franco/vonkarman) | Rust | Pseudospectral DNS for the 3D incompressible Navier-Stokes equations. |
| [`ermak`](https://github.com/alejandro-soto-franco/ermak) | Rust + Python | GPU Brownian dynamics for ligand diffusion and dissociation kinetics in crowded environments. |
| [`mermin`](https://github.com/alejandro-soto-franco/mermin) | Rust + Python | k-atic alignment and topological-defect analysis of fluorescence microscopy. |
| [`inferCNAsc`](https://github.com/alejandro-soto-franco/inferCNAsc) | Rust + Python | Copy-number alteration inference from single-cell RNA-seq. |
| [`tikhonov`](https://github.com/alejandro-soto-franco/tikhonov) | Rust | Pure-Rust Harmony2 for single-cell data integration. |

## Systems and tooling

| Repository | Language | What it does |
|---|---|---|
| [`lichtung`](https://github.com/alejandro-soto-franco/lichtung) | Rust | Actor library with first-class causal observability: lock-free vector-clock mailboxes, and a dual-mode executor giving record and deterministic replay. |
| [`vigild`](https://github.com/alejandro-soto-franco/vigild) | Rust | Multi-host Linux service health daemon. |
| [`cc-harness`](https://github.com/alejandro-soto-franco/cc-harness) | Rust | Multi-session agent launcher backed by tmux. |
| [`collint`](https://github.com/alejandro-soto-franco/collint) | Rust + Python | Detects and auto-fixes visual collisions in matplotlib figures. |
| [`rotorlab`](https://github.com/alejandro-soto-franco/rotorlab) | Rust | Maths-animation engine on a const-generic geometric-algebra core, rendered through raw Vulkan. |

## Upstream contributions

| Date | Project | Contribution | Reference |
|---|---|---|---|
| 14 Apr 2026 | [Mathlib4](https://github.com/leanprover-community/mathlib4) | `HasCompactMulSupport` closure under product operations: submonoid, `List`, `Multiset` and `Finset` variants, with `@[to_additive]`. | [#38022](https://github.com/leanprover-community/mathlib4/pull/38022) |
| 12 May 2026 | [cuda-oxide](https://github.com/NVlabs/cuda-oxide) | Converted three silent miscompiles in the Rust-to-PTX code generator into hard build errors, each with a regression-test crate. | [#27](https://github.com/NVlabs/cuda-oxide/pull/27) |
| 18 Jun 2026 | cuda-oxide | Fused-multiply-add contraction as the default, matching `nvcc --fmad=true`, with an `-O3` pass. | [#117](https://github.com/NVlabs/cuda-oxide/pull/117) |
| 20 Jun 2026 | cuda-oxide | `cargo oxide emit-ltoir`, building a crate's LTOIR in one step, and a cached-backend rebuild fix. | [#256](https://github.com/NVlabs/cuda-oxide/pull/256) · [#257](https://github.com/NVlabs/cuda-oxide/pull/257) |
| 30 Jun 2026 | cuda-oxide | `cuda-oxide-codegen`: extracted the dialect-MIR-to-PTX backend into a rustc-independent crate, so front ends other than the Rust path can drive the same pipeline. | [#314](https://github.com/NVlabs/cuda-oxide/pull/314) |
| 10 Jul 2026 | [Daft](https://github.com/Eventual-Inc/Daft) | Lowered the release opt-level for `opendal-service-oss`. | [#7249](https://github.com/Eventual-Inc/Daft/pull/7249) |
| 11 Jul 2026 | [txm](https://github.com/thatmagicalcat/txm) | Font-alphabet commands, inline symbols, single-token arguments and accents. | [#14](https://github.com/thatmagicalcat/txm/pull/14) |
| 13 Jul 2026 | Daft | Dashboard build support for `OUT_DIR` on a filesystem other than the source tree's. | [#7246](https://github.com/Eventual-Inc/Daft/pull/7246) |

Five further cuda-oxide pull requests are open, among them a fourth silent miscompile ([#394](https://github.com/NVlabs/cuda-oxide/pull/394): aggregate constant fields read at the wrong layout offsets, with no diagnostic) and harness work on the differential fuzzer ([#395](https://github.com/NVlabs/cuda-oxide/pull/395)).

## Quantitative finance

Private repositories under [Holonomy Securities](https://holonomysecurities.com).

| Project | Description |
|---|---|
| [**Colosseum**](https://colosseum.holonomysecurities.com) | Multi-asset backtesting and execution platform. WASM strategy sandbox, CLOB-native data, configurable fill models, full audit trail. Rust engine, axum API, Next.js frontend. |
| **Polybius** | Binary options engine for prediction markets. Non-stationary SDE models, Kelly sizing, CLOB execution. Live on Polymarket. |
| **Malliavin** | Regime-conditional equity options engine. Directional spreads and volatility selling. |
| **Bismut** | Volatility-surface curvature signals: SSVI fitting, Riemannian curvature extraction, walk-forward backtesting. |
| **Hsu** | Manifold-valued covariance research. Realised covariance matrices as points on SPD(N) under affine-invariant metrics. |

## Writing

[Lecture notes and exercises](https://github.com/alejandro-soto-franco/jhu) for a Johns Hopkins BS/MSE curriculum (CC BY 4.0), [manuscripts](https://github.com/alejandro-soto-franco/manuscripts), and articles at [sotofranco.dev](https://sotofranco.dev).
