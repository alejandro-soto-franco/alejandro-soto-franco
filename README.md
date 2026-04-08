# Alejandro Soto Franco

Rust + Math. Founding Principal at [Holonomy Securities](https://holonomysecurities.com).

BS/MSE Biomedical Engineering, Johns Hopkins University. Previously a trading strategies developer at Anti Capital (New York), building multi-exchange async execution systems in Rust.

I build high-performance numerical software: quantitative trading engines, computational geometry libraries, and PDE solvers. Everything ships in Rust by default.

[![Website](https://img.shields.io/badge/sotofranco.dev-000?style=flat-square&logo=vercel&logoColor=white)](https://sotofranco.dev)



## Quantitative Finance

Private repositories under [Holonomy Securities](https://holonomysecurities.com).

| Project | Description |
|---------|-------------|
| **Polybius** | Binary options engine for prediction markets. Non-stationary SDE models, Kelly sizing, CLOB execution. Polymarket live, Kalshi planned. 16-crate workspace. |
| **Malliavin** | Regime-conditional equity options engine. Directional spreads + vol selling on QQQ. Polygon + CBOE data, Deribit/IBKR venue integrations. |
| **Bismut** | Volatility surface curvature signals. SSVI fitting, Riemannian curvature extraction, walk-forward backtesting with butterfly and straddle strategies. |
| **Hsu** | Manifold-valued covariance research engine. Realized covariance matrices as points on SPD(N) with affine-invariant metrics, tangent-space MLE calibration. Built on `cartan` and `pathwise`. |

## Computational Mathematics

Open-source libraries for differential geometry, simulation, and scientific computing.

| Project | Description |
|---------|-------------|
| [**cartan**](https://github.com/alejandro-soto-franco/cartan) | Riemannian and Lie-group optimization in Rust. 6 crates on [crates.io](https://crates.io/crates/cartan), Python bindings on [PyPI](https://pypi.org/project/cartan/). Benchmarks and docs at [cartan.sotofranco.dev](https://cartan.sotofranco.dev). |
| [**volterra**](https://github.com/alejandro-soto-franco/volterra) | Covariant active nematics solver for arbitrary dimensions. Discrete exterior calculus on simplicial meshes. |
| [**pathwise**](https://github.com/alejandro-soto-franco/pathwise) | Simulation and calibration of non-Markovian stochastic differential equations. Geodesic integrators on manifold state spaces. |
| [**vonkarman**](https://github.com/alejandro-soto-franco/vonkarman) | 3D Navier-Stokes solver in Rust. |
| [**inferCNAsc**](https://github.com/alejandro-soto-franco/inferCNAsc) | Copy number alteration inference from single-cell RNA-seq. Rust HPC backend + Python interface. |

## Research

Interested in the 3D Navier-Stokes smooth solution existence and uniqueness problem. Active research in defect-mediated hydrodynamics of coupled active-lyotropic nematic systems (with the [Beller Lab](https://danielbeller.com) at JHU).



<p align="center">
  <img src="https://github-readme-stats-kohl-nine-83.vercel.app/api/top-langs/?username=alejandro-soto-franco&layout=compact&theme=github_dark&hide_border=true&bg_color=00000000&langs_count=10&hide=html,jupyter%20notebook,mdx,tex,makefile,css,plpgsql" />
</p>
