# Alejandro Soto Franco

Rust + Math. Founding Principal at [Holonomy Securities](https://holonomysecurities.com), where a three-person team ships systematic trading engines (Polybius, Malliavin, Bismut, Hsu) on a shared platform substrate ([Colosseum](https://colosseum.holonomysecurities.com), just launched). Polybius, our Polymarket-native binary options engine, is up roughly 81% since going live.

BS/MSE Biomedical Engineering, Johns Hopkins University. Previously a trading strategies developer at Anti Capital (New York), building multi-exchange async execution systems in Rust.

In parallel I maintain open-source Rust libraries for geometric computing and stochastic analysis (cartan, pathwise, volterra, elworthy), and collaborate with the University of Pittsburgh School of Medicine on applying mermin's topological-defect pipeline to human vaginal fibroblast microscopy.

[![Website](https://img.shields.io/badge/sotofranco.dev-000?style=flat-square&logo=vercel&logoColor=white)](https://sotofranco.dev)

## Open source

| Repository | Language | What it does | CI |
|---|---|---|---|
| [`cartan`](https://github.com/alejandro-soto-franco/cartan) | Rust + Python | Riemannian geometry, Lie-group optimisation, and stochastic analysis on manifolds | [![CI](https://github.com/alejandro-soto-franco/cartan/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/cartan/actions/workflows/ci.yml) |
| [`volterra`](https://github.com/alejandro-soto-franco/volterra) | Rust + Python | Covariant active-nematics solver via discrete exterior calculus | [![CI](https://github.com/alejandro-soto-franco/volterra/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/volterra/actions/workflows/ci.yml) |
| [`pathwise`](https://github.com/alejandro-soto-franco/pathwise) | Rust + Python | Simulation and calibration of non-Markovian stochastic differential equations | [![CI](https://github.com/alejandro-soto-franco/pathwise/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/pathwise/actions/workflows/ci.yml) |
| [`elworthy`](https://github.com/alejandro-soto-franco/elworthy) | Rust + Python | JIT compiler specialising Bismut-Elworthy-Li Greeks into SIMD kernels | [![CI](https://github.com/alejandro-soto-franco/elworthy/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/elworthy/actions/workflows/ci.yml) |
| [`hurst`](https://github.com/alejandro-soto-franco/hurst) | Rust | Rough volatility on the correlation manifold; Hurst estimation on SPD(N) | [![CI](https://github.com/alejandro-soto-franco/hurst/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/hurst/actions/workflows/ci.yml) |
| [`vonkarman`](https://github.com/alejandro-soto-franco/vonkarman) | Rust | Pseudospectral DNS for the 3D incompressible Navier-Stokes equations | [![CI](https://github.com/alejandro-soto-franco/vonkarman/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/vonkarman/actions/workflows/ci.yml) |
| [`gpufft`](https://github.com/alejandro-soto-franco/gpufft) | Rust | Unified GPU FFT: VkFFT on Vulkan, cuFFT on CUDA | [![CI](https://github.com/alejandro-soto-franco/gpufft/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/gpufft/actions/workflows/ci.yml) |
| [`ferrum-gpu`](https://github.com/alejandro-soto-franco/ferrum-gpu) | Rust + Python | Pure-Rust GPU compute: Rust-to-PTX FFT kernels with Python bindings | [![CI](https://github.com/alejandro-soto-franco/ferrum-gpu/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/ferrum-gpu/actions/workflows/ci.yml) |
| [`spirv-oxide`](https://github.com/alejandro-soto-franco/spirv-oxide) | Rust | Rust-to-SPIR-V GPU compiler via Pliron MLIR | [![CI](https://github.com/alejandro-soto-franco/spirv-oxide/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/spirv-oxide/actions/workflows/ci.yml) |
| [`ermak`](https://github.com/alejandro-soto-franco/ermak) | Rust + Python | GPU Brownian dynamics for ligand dissociation kinetics | [![CI](https://github.com/alejandro-soto-franco/ermak/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/ermak/actions/workflows/ci.yml) |
| [`inferCNAsc`](https://github.com/alejandro-soto-franco/inferCNAsc) | Rust + Python | Copy-number alteration inference from single-cell RNA-seq | [![CI](https://github.com/alejandro-soto-franco/inferCNAsc/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/inferCNAsc/actions/workflows/ci.yml) |
| [`mermin`](https://github.com/alejandro-soto-franco/mermin) | Rust + Python | k-atic alignment analysis of fluorescence microscopy | [![CI](https://github.com/alejandro-soto-franco/mermin/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/mermin/actions/workflows/ci.yml) |
| [`tikhonov`](https://github.com/alejandro-soto-franco/tikhonov) | Rust | Pure-Rust Harmony2 for single-cell data integration | [![CI](https://github.com/alejandro-soto-franco/tikhonov/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/tikhonov/actions/workflows/ci.yml) |
| [`collint`](https://github.com/alejandro-soto-franco/collint) | Rust + Python | Detect and auto-fix visual collisions in matplotlib figures | [![CI](https://github.com/alejandro-soto-franco/collint/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/collint/actions/workflows/ci.yml) |
| [`kloeden`](https://github.com/alejandro-soto-franco/kloeden) | C++ + Rust | Hand-SIMD C++ versus Rust SDE-scheme benchmark companion | [![CI](https://github.com/alejandro-soto-franco/kloeden/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/kloeden/actions/workflows/ci.yml) |
| [`rotorlab`](https://github.com/alejandro-soto-franco/rotorlab) | Rust | Geometric-algebra maths-animation engine, rendered via Vulkan | [![CI](https://github.com/alejandro-soto-franco/rotorlab/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/rotorlab/actions/workflows/ci.yml) |
| [`vigild`](https://github.com/alejandro-soto-franco/vigild) | Rust | Multi-host Linux service-health daemon | [![CI](https://github.com/alejandro-soto-franco/vigild/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/vigild/actions/workflows/ci.yml) |
| [`navier-stokes`](https://github.com/alejandro-soto-franco/navier-stokes) | Python + Lean | 3D Navier-Stokes regularity: Lean, numerics, and theory | [![CI](https://github.com/alejandro-soto-franco/navier-stokes/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/navier-stokes/actions/workflows/ci.yml) |
| [`Meridian`](https://github.com/alejandro-soto-franco/Meridian) | Lean 4 | Metaprogramming toolkit: sorry inventory, proof search, dependency graphs | [![CI](https://github.com/alejandro-soto-franco/Meridian/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/Meridian/actions/workflows/ci.yml) |
| [`meridian-vscode`](https://github.com/alejandro-soto-franco/meridian-vscode) | TypeScript | VS Code companion: interactive dependency graph and Mathlib symbol index | [![CI](https://github.com/alejandro-soto-franco/meridian-vscode/actions/workflows/ci.yml/badge.svg)](https://github.com/alejandro-soto-franco/meridian-vscode/actions/workflows/ci.yml) |

## Research and formalisation

Three-track architecture (Lean 4 + LaTeX + SymPy / Cadabra2) with chapter-level synchronisation between formal, narrative, and symbolic verification. The public Navier-Stokes track is in the table above; the items below are private or pre-release.

| Project | Language | Description |
|---------|----------|-------------|
| **elliptic-dirichlet** (private) | Lean 4 | Machine-verified existence and uniqueness of the weak $H_0^1$ solution of the Dirichlet problem for a uniformly elliptic, divergence-form operator, via Lax-Milgram. Joint formalisation with Kobe Marshall-Stevens. |
| **mars-lnp** (private) | Rust | Defect-mediated hydrodynamic transfer of orientational order in coupled active-lyotropic nematic systems. Simulations on `volterra`, defect detection via `cartan` holonomy. |

## Upstream contributions

| Date | Project | Description | Reference |
|------|---------|-------------|-----------|
| 14 Apr 2026 | [Mathlib4](https://github.com/leanprover-community/mathlib4) | `HasCompactMulSupport` closure under product operations: submonoid, List, Multiset, and Finset variants, with `@[to_additive]`. | [#38022](https://github.com/leanprover-community/mathlib4/pull/38022) · [`2ff8885`](https://github.com/leanprover-community/mathlib4/commit/2ff88851d5) |
| 12 May 2026 | [cuda-oxide](https://github.com/NVlabs/cuda-oxide) | `fix(codegen)`: convert three silent miscompiles in the Rust-to-PTX code generator into hard build errors, including the invalid `.version` emitted for `compute_*` targets that `ptxas` rejects only at JIT time. | [#27](https://github.com/NVlabs/cuda-oxide/pull/27) · [`3697238`](https://github.com/NVlabs/cuda-oxide/commit/369723899a) |

## Quantitative Finance

Private repositories under [Holonomy Securities](https://holonomysecurities.com).

| Project | Description |
|---------|-------------|
| [**Colosseum**](https://colosseum.holonomysecurities.com) | Multi-asset quantitative backtesting platform. WASM strategy sandbox, CLOB-native data, configurable fill models, full audit trail. Rust engine + axum API + Next.js frontend. |
| **Polybius** | Binary options engine for prediction markets. Non-stationary SDE models, Kelly sizing, CLOB execution. Polymarket live, Kalshi planned. 16-crate workspace. |
| **Malliavin** | Regime-conditional equity options engine. Directional spreads + vol selling on QQQ. Polygon + CBOE data, Deribit/IBKR venue integrations. |
| **Bismut** | Volatility surface curvature signals. SSVI fitting, Riemannian curvature extraction, walk-forward backtesting with butterfly and straddle strategies. |
| **Hsu** | Manifold-valued covariance research engine. Realised covariance matrices as points on SPD(N) with affine-invariant metrics, tangent-space MLE calibration. Built on `cartan` and `pathwise`. |

<p align="center">
  <img src="https://github-readme-stats-kohl-nine-83.vercel.app/api/top-langs/?username=alejandro-soto-franco&layout=compact&theme=github_dark&hide_border=true&bg_color=00000000&langs_count=10&hide=html,jupyter%20notebook,mdx,tex,makefile,css,plpgsql&cache_seconds=1800&v=1" />
</p>
