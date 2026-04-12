# Alejandro Soto Franco

Rust + Math. Founding Principal at [Holonomy Securities](https://holonomysecurities.com).

BS/MSE Biomedical Engineering, Johns Hopkins University. Previously a trading strategies developer at Anti Capital (New York), building multi-exchange async execution systems in Rust.

I build high-performance numerical software: quantitative trading engines, computational geometry libraries, and PDE solvers. Everything ships in Rust by default.

[![Website](https://img.shields.io/badge/sotofranco.dev-000?style=flat-square&logo=vercel&logoColor=white)](https://sotofranco.dev)



## Research

Active research programmes developed along a three-track architecture (Lean 4 + LaTeX + SymPy / Cadabra2) with chapter-level synchronisation between formal, narrative, and symbolic verification.

| Project | Description |
|---------|-------------|
| [**3d-navier-stokes**](https://github.com/alejandro-soto-franco/navier-stokes) | A geometric-analytic approach to the Clay Millennium regularity problem for the 3D incompressible Navier-Stokes equations via the Biot-Savart connection on the divergence-free bundle. Six-chapter monograph in LaTeX; Lean 4 formalisation (21 theorems proved against Mathlib, ~2,400 lines of user code) with sorry-counts named by blocker; SymPy + Cadabra2 symbolic cross-checks on every coordinate and abstract-index identity. Chapters 3-4 develop the connection as Levi-Civita of the $L^2$ metric on $\mathrm{SDiff}(\mathbb{T}^3)$, prove the CKN bridge theorem in full, and derive a curvature-measure bound $\mu_R = |R|^{6/5}$ finite at Leray-Hopf regularity. |
| [**mars-lnp**](https://github.com/alejandro-soto-franco/mars-lnp) | Defect-mediated hydrodynamic transfer of orientational order in coupled active-lyotropic nematic systems. Magnetically actuated nematic rotor suspension plus lyotropic lipid phase; simulations run on `volterra` with defect detection via `cartan` holonomy. Every paper equation traced to a SymPy (symbolic / dimensional) + NumPy (numerical sanity) + Lean 4 / Mathlib (topological claims) check. |

## Computational Mathematics

Open-source libraries for differential geometry, simulation, and scientific computing.

| Project | Description |
|---------|-------------|
| [**cartan**](https://github.com/alejandro-soto-franco/cartan) | Riemannian and Lie-group optimization in Rust. 6 crates on [crates.io](https://crates.io/crates/cartan), Python bindings on [PyPI](https://pypi.org/project/cartan/). Benchmarks and docs at [cartan.sotofranco.dev](https://cartan.sotofranco.dev). |
| [**volterra**](https://github.com/alejandro-soto-franco/volterra) | Covariant active nematics solver for arbitrary dimensions. Discrete exterior calculus on simplicial meshes. Rust crates on [crates.io](https://crates.io/crates/volterra), Python bindings on [PyPI](https://pypi.org/project/volterra-nematic/). |
| [**pathwise**](https://github.com/alejandro-soto-franco/pathwise) | Simulation and calibration of non-Markovian stochastic differential equations. Geodesic integrators on manifold state spaces. Rust crates on [crates.io](https://crates.io/crates/pathwise-core), Python bindings on [PyPI](https://pypi.org/project/pathwise-sde/). |
| [**vonkarman**](https://github.com/alejandro-soto-franco/vonkarman) | Pseudospectral DNS solver for the 3D incompressible Navier-Stokes equations. ETD-RK4 time integration, cuFFT GPU backend via runtime-loaded CUDA, checkpoint/restart, spectral convergence verified. 5 crates on [crates.io](https://crates.io/crates/vonkarman-core). Cross-validated against JHU's [hit3d](https://github.com/cpraveen/hit3d) (Fortran) on Taylor-Green Re=1600. |
| [**elworthy**](https://github.com/alejandro-soto-franco/elworthy) | JIT compiler that specialises Bismut-Elworthy-Li formulas into SIMD kernels for unbiased Monte Carlo Greeks on non-stationary SDEs. Symbolic AST, Cranelift lowering (scalar + F64X2), multi-dimensional Heston driver, pathwise and Malliavin-weight parameter Greeks (machine-checked with SymPy). European call price and BEL delta cross-validated against Black-Scholes closed form and the independent [`blackscholes`](https://github.com/hayden4r4/blackscholes-rust) crate; both agree within four Monte Carlo standard errors. 6 crates on [crates.io](https://crates.io/crates/elworthy). ~22x over the tree-walking interpreter on GBM paths. |

## Bioinformatics

| Project | Description |
|---------|-------------|
| [**inferCNAsc**](https://github.com/alejandro-soto-franco/inferCNAsc) | Copy number alteration inference from single-cell RNA-seq. Rust HPC backend + Python interface. On [crates.io](https://crates.io/crates/infercnasc) and [PyPI](https://pypi.org/project/infercnasc/). |
| [**mermin**](https://github.com/alejandro-soto-franco/mermin) | k-atic alignment analysis of fluorescence microscopy. Minkowski tensor shape descriptors, multiscale structure tensor, topological defect detection via `cartan-geo` SO(3) holonomy, persistent homology, and Landau-de Gennes parameter fitting on cell monolayers. 7 crates on [crates.io](https://crates.io/crates/mermin), Python bindings on [PyPI](https://pypi.org/project/mermin/). |

## Quantitative Finance

Private repositories under [Holonomy Securities](https://holonomysecurities.com).

| Project | Description |
|---------|-------------|
| **Colosseum** | Multi-asset quantitative backtesting platform. WASM strategy sandbox, CLOB-native data, configurable fill models, full audit trail. Rust engine + axum API + Next.js frontend. |
| **Polybius** | Binary options engine for prediction markets. Non-stationary SDE models, Kelly sizing, CLOB execution. Polymarket live, Kalshi planned. 16-crate workspace. |
| **Malliavin** | Regime-conditional equity options engine. Directional spreads + vol selling on QQQ. Polygon + CBOE data, Deribit/IBKR venue integrations. |
| **Bismut** | Volatility surface curvature signals. SSVI fitting, Riemannian curvature extraction, walk-forward backtesting with butterfly and straddle strategies. |
| **Hsu** | Manifold-valued covariance research engine. Realized covariance matrices as points on SPD(N) with affine-invariant metrics, tangent-space MLE calibration. Built on `cartan` and `pathwise`. |



<p align="center">
  <img src="https://github-readme-stats-kohl-nine-83.vercel.app/api/top-langs/?username=alejandro-soto-franco&layout=compact&theme=github_dark&hide_border=true&bg_color=00000000&langs_count=10&hide=html,jupyter%20notebook,mdx,tex,makefile,css,plpgsql" />
</p>
