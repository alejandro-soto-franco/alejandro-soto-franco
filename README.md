# Alejandro Soto Franco

Rust + Math. Founding Principal at [Holonomy Securities](https://holonomysecurities.com), where a three-person team ships systematic trading engines (Polybius, Malliavin, Bismut, Hsu) on a shared platform substrate ([Colosseum](https://colosseum.holonomysecurities.com), just launched). Polybius, our Polymarket-native binary options engine, is up roughly 81% since going live.

BS/MSE Biomedical Engineering, Johns Hopkins University. Previously a trading strategies developer at Anti Capital (New York), building multi-exchange async execution systems in Rust.

In parallel I maintain open-source Rust libraries for geometric computing and stochastic analysis (cartan, pathwise, volterra, elworthy), and collaborate with the University of Pittsburgh School of Medicine on applying mermin's topological-defect pipeline to human vaginal fibroblast microscopy.

[![Website](https://img.shields.io/badge/sotofranco.dev-000?style=flat-square&logo=vercel&logoColor=white)](https://sotofranco.dev)



## Research

Active research programmes developed along a three-track architecture (Lean 4 + LaTeX + SymPy / Cadabra2) with chapter-level synchronisation between formal, narrative, and symbolic verification.

| Project | Description |
|---------|-------------|
| [**3d-navier-stokes**](https://github.com/alejandro-soto-franco/navier-stokes) | A geometric-analytic attack on 3D Navier-Stokes regularity (Clay Millennium), via the Biot-Savart connection. |
| [**elliptic-dirichlet**](https://github.com/alejandro-soto-franco/elliptic-dirichlet) | Machine-verified existence and uniqueness, in Lean 4, of the weak $H_0^1$ solution of the Dirichlet problem for a uniformly elliptic, divergence-form linear operator on a bounded domain, via the Lax-Milgram route. Joint formalisation with Kobe Marshall-Stevens, with a companion LaTeX paper and a `cartan`-FEM / SymPy numerical track. |
| **mars-lnp** | Defect-mediated hydrodynamic transfer of orientational order in coupled active-lyotropic nematic systems. Magnetically actuated nematic rotor suspension plus lyotropic lipid phase; simulations run on `volterra` with defect detection via `cartan` holonomy. Every paper equation traced to a SymPy (symbolic / dimensional) + NumPy (numerical sanity) + Lean 4 / Mathlib (topological claims) check. |

## Lean 4 Metaprogramming

| Project | Description |
|---------|-------------|
| [**Meridian**](https://github.com/alejandro-soto-franco/Meridian) | Lean 4 metaprogramming toolkit for mathematical formalisation. Sorry analysis with Mathlib `DiscrTree` coverage (available / partially available / not available), DOT dependency graphs, IDA* proof search with memoisation over the tactic state, and work-in-progress domain tactics for distributional PDEs (Sobolev exponent arithmetic, Biot-Savart, curvature, helicity) and geometric measure theory (varifolds, first variation, stationary varifolds, interior monotonicity). Apache 2.0. Runs entirely locally. |
| [**meridian-vscode**](https://github.com/alejandro-soto-franco/meridian-vscode) | Companion VS Code extension. Interactive 2-hop dependency graph laid out as *imports → refs → decls* with status-coloured declarations, a full-project Mathlib symbol index that resolves transitive imports and bare identifiers, and edge-click detail surfacing per-line usage classified as *signature* (type-level) vs *proof / body* (value-level). Paul Tol bright palette with an opt-in CVD-safe mode. Pan / zoom / focus-mode interactions. Entirely local execution; prepared for VS Code Marketplace release. |

## Computational Mathematics

Open-source libraries for differential geometry, simulation, and scientific computing.

| Project | Description |
|---------|-------------|
| [**cartan**](https://github.com/alejandro-soto-franco/cartan) | Riemannian geometry, Lie-group optimisation, and stochastic analysis on manifolds in Rust. 7 crates on [crates.io](https://crates.io/crates/cartan), Python bindings on [PyPI](https://pypi.org/project/cartan/). Latest addition: `cartan-stochastic` provides the orthonormal frame bundle, Stratonovich development (Eells-Elworthy-Malliavin construction of Brownian motion on a manifold), Bures-Wasserstein SPD geometry, and the Wishart SPD diffusion: the foundation for downstream Bismut-Elworthy-Li Greeks work. Benchmarks and docs at [cartan.sotofranco.dev](https://cartan.sotofranco.dev). |
| [**volterra**](https://github.com/alejandro-soto-franco/volterra) | Covariant active nematics solver for arbitrary dimensions. Discrete exterior calculus on simplicial meshes. Rust crates on [crates.io](https://crates.io/crates/volterra), Python bindings on [PyPI](https://pypi.org/project/volterra-nematic/). |
| [**pathwise**](https://github.com/alejandro-soto-franco/pathwise) | Simulation and calibration of non-Markovian stochastic differential equations. Geodesic integrators on manifold state spaces. Rust crates on [crates.io](https://crates.io/crates/pathwise-core), Python bindings on [PyPI](https://pypi.org/project/pathwise-sde/). |
| [**vonkarman**](https://github.com/alejandro-soto-franco/vonkarman) | Pseudospectral DNS solver for the 3D incompressible Navier-Stokes equations. ETD-RK4 time integration, cuFFT GPU backend via runtime-loaded CUDA, checkpoint/restart, spectral convergence verified. 5 crates on [crates.io](https://crates.io/crates/vonkarman-core). Cross-validated against JHU's [hit3d](https://github.com/cpraveen/hit3d) (Fortran) on Taylor-Green Re=1600. |
| [**gpufft**](https://github.com/alejandro-soto-franco/gpufft) | Unified GPU-accelerated FFT for Rust with a single trait surface over VkFFT on Vulkan and cuFFT on CUDA. Backend-typed plans for C2C, R2C, and C2R at f32 and f64; cross-backend mixing is a compile error. Zero-copy C2C via `VkFFTLaunchParams` buffer override, compute-shader padder for R2C / C2R innermost-axis alignment. On NVIDIA RTX 5060 the 3D R2C+C2R pair runs at 86&nbsp;µs (32³), 386&nbsp;µs (128³), and 5.28&nbsp;ms (256³) on Vulkan, 2–3× the cuFFT baseline across sizes. Ships with a standalone C++ repro (`investigations/vkfft_multidim_r2c/`) that isolates an upstream VkFFT multi-dim C2R + launch-override bug. 3 crates on [crates.io](https://crates.io/crates/gpufft). Consumed by `vonkarman` for its NVIDIA FFT backend. |
| [**ferrum-gpu**](https://github.com/alejandro-soto-franco/ferrum-gpu) | Pure-Rust GPU compute substrate with Python bindings: FFT kernels compiled from Rust source straight to PTX (no CUDA C) and run on NVIDIA via [cuda-oxide](https://github.com/NVlabs/cuda-oxide), with cross-vendor `spirv-oxide` → Vulkan on the v0.2 roadmap. Shares the `fft_1d_c2c_pow2` API surface with `gpufft` and is validated against NumPy. `v0.1.0` on [PyPI](https://pypi.org/project/ferrum-gpu/). |
| [**elworthy**](https://github.com/alejandro-soto-franco/elworthy) | JIT compiler that specialises Bismut-Elworthy-Li formulas into SIMD kernels for unbiased Monte Carlo Greeks on non-stationary SDEs. Symbolic AST, Cranelift lowering (scalar + F64X2), multi-dimensional Heston driver, pathwise and Malliavin-weight parameter Greeks (machine-checked with SymPy). European call price and BEL delta cross-validated against Black-Scholes closed form and the independent [`blackscholes`](https://github.com/hayden4r4/blackscholes-rust) crate; both agree within four Monte Carlo standard errors. 6 crates on [crates.io](https://crates.io/crates/elworthy). ~22x over the tree-walking interpreter on GBM paths. |
| [**kloeden**](https://github.com/alejandro-soto-franco/kloeden) | Hand-written SIMD C++ vs Rust (LLVM + Cranelift) benchmark companion to `pathwise` and `elworthy`, named after Peter Kloeden. Single-thread, pinned-core throughput on one shared Brownian-increment buffer across four impls (cpp-strict, cpp-fast, pathwise-LLVM, elworthy-Cranelift) for scalar Euler / Milstein / Taylor 1.5 on GBM; `cpp-strict` and `pathwise` land within 4–15% of each other on every scheme. Plus a digital-delta correctness table showing naive pathwise-diff silently returns 0 in both languages (Dirac in `f'`) while the Bismut-Elworthy-Li constant-flow weight matches analytic Δ within 4 MC standard errors, bitwise-identical across hand-rolled C++, hand-rolled Rust, and `elworthy_rt::from_paths::bel_delta_constant_flow_from_paths`. |

## Bioinformatics

| Project | Description |
|---------|-------------|
| [**inferCNAsc**](https://github.com/alejandro-soto-franco/inferCNAsc) | Copy number alteration inference from single-cell RNA-seq. Rust HPC backend + Python interface. On [crates.io](https://crates.io/crates/infercnasc) and [PyPI](https://pypi.org/project/infercnasc/). |
| [**mermin**](https://github.com/alejandro-soto-franco/mermin) | k-atic alignment analysis of fluorescence microscopy. Minkowski tensor shape descriptors, multiscale structure tensor, topological defect detection via `cartan-geo` SO(3) holonomy, persistent homology, and Landau-de Gennes parameter fitting on cell monolayers. 7 crates on [crates.io](https://crates.io/crates/mermin), Python bindings on [PyPI](https://pypi.org/project/mermin/). |

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
