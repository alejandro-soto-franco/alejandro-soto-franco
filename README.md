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

<!-- personal:contributions:begin id=table -->
| Date | Project | Contribution | Reference |
|---|---|---|---|
| 14 Apr 2026 | [Mathlib4](https://github.com/leanprover-community/mathlib4) | `HasCompactMulSupport` closure under product operations: submonoid, `List`, `Multiset` and `Finset` variants, with `@[to_additive]`. | [#38022](https://github.com/leanprover-community/mathlib4/pull/38022) |
| 12 May 2026 | [cuda-oxide](https://github.com/NVlabs/cuda-oxide) | Converted three silent miscompiles in the Rust-to-PTX code generator into hard build errors, each with a regression-test crate. | [#27](https://github.com/NVlabs/cuda-oxide/pull/27) |
| 18 Jun 2026 | cuda-oxide | Fused-multiply-add contraction as the default, matching `nvcc --fmad=true`, with an `-O3` pass. | [#117](https://github.com/NVlabs/cuda-oxide/pull/117) |
| 20 Jun 2026 | cuda-oxide | `cargo oxide emit-ltoir`, building a crate's LTOIR in one step, which enables LTO across the Rust and CUDA C boundary. | [#256](https://github.com/NVlabs/cuda-oxide/pull/256) |
| 20 Jun 2026 | cuda-oxide | Rebuild the cached backend when its source advances, eliminating stale compiled artefacts after an upstream update. | [#257](https://github.com/NVlabs/cuda-oxide/pull/257) |
| 4 Jul 2026 | cuda-oxide | `cuda-oxide-codegen`: extracted the dialect-MIR-to-PTX backend into a rustc-independent crate, so front ends other than the Rust path can drive the same pipeline. | [#314](https://github.com/NVlabs/cuda-oxide/pull/314) |
| 10 Jul 2026 | [Daft](https://github.com/Eventual-Inc/Daft) | Lowered the release `opt-level` for `opendal-service-oss`, sidestepping an LLVM SLP-vectoriser stall that hung the build for tens of minutes. | [#7249](https://github.com/Eventual-Inc/Daft/pull/7249) |
| 11 Jul 2026 | [txm](https://github.com/thatmagicalcat/txm) | Font-alphabet commands, inline symbols, single-token macro arguments and accents, which together carry geometric-algebra and quaternion notation in a terminal. | [#14](https://github.com/thatmagicalcat/txm/pull/14) |
| 13 Jul 2026 | Daft | Dashboard build support for `OUT_DIR` on a filesystem other than the source tree's, falling back to copy-then-remove when `rename(2)` returns `EXDEV`. | [#7246](https://github.com/Eventual-Inc/Daft/pull/7246) |
| 22 Jul 2026 | cuda-oxide | Ran fuzzer seeds whose device code calls libdevice, loading through `kernels::load` so cubin, PTX, NVVM IR and LTOIR each dispatch to the right loader. | [#395](https://github.com/NVlabs/cuda-oxide/pull/395) |
| 22 Jul 2026 | cuda-oxide | Tightened the standalone compiler's clone, liveness and diagnostic paths: an erase guard on the panic path, an opt-in module clone, and toolchain selection recorded for the caller. | [#415](https://github.com/NVlabs/cuda-oxide/pull/415) |
| 23 Jul 2026 | cuda-oxide | A fourth silent miscompile: aggregate constant fields read at the wrong layout offsets, with no diagnostic. | [#394](https://github.com/NVlabs/cuda-oxide/pull/394) |
| 24 Jul 2026 | cuda-oxide | Target selection attributed to whoever chose the target. | [#416](https://github.com/NVlabs/cuda-oxide/pull/416) |
| 24 Jul 2026 | cuda-oxide | The standalone compiler's scratch directory backed by `tempfile`. | [#417](https://github.com/NVlabs/cuda-oxide/pull/417) |
| 24 Jul 2026 | cuda-oxide | Publish the backend to the shared cache on setup. | [#445](https://github.com/NVlabs/cuda-oxide/pull/445) |
| 24 Jul 2026 | cuda-oxide | Report the shared cache in `doctor`. | [#447](https://github.com/NVlabs/cuda-oxide/pull/447) |
| 27 Jul 2026 | cuda-oxide | `SwitchInt` arms compared at the discriminant width, so a match on a 128-bit scrutinee compiles. Found by the differential fuzzer: a `u64::try_from` clamp on the arm values refused a case the 64-bit enum carrier limit never covered. | [#482](https://github.com/NVlabs/cuda-oxide/pull/482) |
| 27 Jul 2026 | cuda-oxide | NVVM IR target rejections reported at the input stage, closing a follow-up the maintainer left on #416: the resolver had labelled target-attributable rejections as export-stage failures. | [#483](https://github.com/NVlabs/cuda-oxide/pull/483) |
| 27 Jul 2026 | cuda-oxide | Fuzzer traces widened to `f32` and `f64`, folded as raw bits with no ULP tolerance, which keeps the trace comparison bit-for-bit. Runs under `--no-fmad`, since contraction is on by default and GPU `fma.rn` would otherwise diverge from the CPU oracle's separate roundings. | [#484](https://github.com/NVlabs/cuda-oxide/pull/484) |
| 27 Jul 2026 | cuda-oxide | Workspace test targets linted in CI. The workspace clippy step was the only one of three missing `--all-targets`, which is why an `unnecessary_mut_passed` inside a `#[cfg(test)]` module had stayed invisible. | [#486](https://github.com/NVlabs/cuda-oxide/pull/486) |
| 28 Jul 2026 | cuda-oxide | An exact launch-contract block shape carried into the compiled artifact as `.reqntid`, so the CUDA driver enforces it per axis at every launch, including raw `_unchecked` ones that bypass preparation. | [#514](https://github.com/NVlabs/cuda-oxide/pull/514) |
| 31 Jul 2026 | cuda-oxide | Opt-in libdevice linking for the standalone PTX API, closing #485. A frontend driving `cuda_oxide_codegen::experimental` stopped at the first `sqrt`, since float intrinsics lower to libdevice `__nv_*` calls and v1 rejected every unresolved external symbol, at a site sitting directly above the IR-level libdevice link that would have resolved them. `Linking::SelfContained` stays the default and changes no compilation that succeeds today. | [#596](https://github.com/NVlabs/cuda-oxide/pull/596) |
| 5 Aug 2026 | cuda-oxide | Added enum payload addressing to the MIR importer's projection walker, closing #651. A mutable borrow of a payload had no address to write through and was refused outright, and `(x as Variant).field = v` failed separately as an unimplemented projection pair; one address fixes both. | [#652](https://github.com/NVlabs/cuda-oxide/pull/652) |
| 5 Aug 2026 | cuda-oxide | Bound a `DisjointSlice`'s runtime row width into its index space at the host boundary, closing #516 and reworking the design closed in #515. A per-call witness cannot carry uniformity across a thread-varying selection, so two threads could disagree about the row width; binding it once at launch removes the choice. | [#653](https://github.com/NVlabs/cuda-oxide/pull/653) |
| 5 Aug 2026 | cuda-oxide | Gave a thread its whole contiguous run through `ThreadRunMut32`, closing #583. `LinearTiles<N>` already proved ownership of `N` elements for a whole tile; this adds the clipped tail for the thread whose run straddles the end of the buffer, and grid-stride iteration over runs. | [#654](https://github.com/NVlabs/cuda-oxide/pull/654) |
| 5 Aug 2026 | cuda-oxide | Made the warp a `ThreadIndex` index space so a warp reduction writes its result through the ordinary bounds-checked `get_mut`, closing #584 with no new uniqueness-witness mechanism. `warp_index()` mints a witness only for lane 0 of each warp, so no `unsafe` is needed at the write site. | [#655](https://github.com/NVlabs/cuda-oxide/pull/655) |
| 6 Aug 2026 | cuda-oxide | Fixes device codegen for constructing a `DisjointSlice` inside a kernel: the constructor's struct literal only sometimes folds away before import, and when it survives crossing a call the aggregate lowering mistook the slice for a scalar-lowered newtype and found no field to write. Adds `mir.construct_disjoint_slice` alongside the fixed-arity `mir.construct_slice`. | [#670](https://github.com/NVlabs/cuda-oxide/pull/670) |
| 6 Aug 2026 | cuda-oxide | Removes a redundant bounds check from `ThreadRunMut32::at`, which re-derived the pointer and length by hand instead of deferring to the view each variant already holds. The `&mut`-through-enum-downcast restriction that justified the raw-parts path no longer holds after #652's payload addressing. | [#671](https://github.com/NVlabs/cuda-oxide/pull/671) |
| 6 Aug 2026 | cuda-oxide | Adds partial-warp reductions for blocks whose width is not a multiple of 32, so the tail warp has something to call. #655's `warp_sums` example carried an ad hoc butterfly correct only for a power-of-two tail; this clamps every shuffle source to the last live lane and handles an arbitrary live-lane count in `ceil(log2(live))` steps. | [#672](https://github.com/NVlabs/cuda-oxide/pull/672) |
| 6 Aug 2026 | cuda-oxide | Adds lowering for mutating a canonical-storage enum payload, such as a `bool` payload stored as a full `i8`, by rebuilding the enum around the new value and storing it whole. #652 correctly refuses to hand out a raw address for a payload whose bytes are held in converted form. | [#673](https://github.com/NVlabs/cuda-oxide/pull/673) |
| 8 Aug 2026 | cuda-oxide | Reading one field of a tuple held in an array copied the whole array first, once per field, because `mir.field_addr`'s verifier accepted struct, union and enum pointees while rejecting tuples, which sent the read down the value path that materialises the entire array. Adds the tuple arm at all three layers with no new MIR op, resolving the GEP slot through `StructLayoutInfo::of_tuple` so it names the memory slot under rustc's reordering of `(u8, u32)`. A 256-entry table drops from 878 `st.local` and a 4 KiB per-thread depot to 512 and 2 KiB. | [#709](https://github.com/NVlabs/cuda-oxide/pull/709) |
| 8 Aug 2026 | cuda-oxide | `CudaContext` exposed no way to choose the primary context's `CU_CTX_SCHED_*` policy, so reaching `CU_CTX_SCHED_BLOCKING_SYNC` meant going through `cuda_core::sys` directly and re-deriving the primary-context caveat at every call site. Adds a `SyncPolicy` enum with `set_sync_policy` and `sync_policy` over `cuDevicePrimaryCtxGetState` and `cuDevicePrimaryCtxSetFlags_v2`, replacing only the three scheduling bits so any independently set flag survives. Device-scoped, matching the primary context `CudaContext` retains, rather than `cuCtxSetFlags`, which follows whatever context is current on the calling thread. | [#710](https://github.com/NVlabs/cuda-oxide/pull/710) |
| 8 Aug 2026 | cuda-oxide | Static shared-memory globals were named from a process-global `AtomicUsize`, so the `__shared_mem_N` index depended on how many other modules the process had lowered first and in what thread order, and two builds of identical source could emit the same globals under different names. Moves the counter onto `MirToLlvmConversionDriver`, which is already instantiated fresh once per module. The maintainer extended the same fix to `__device_global_N` on top, which makes device codegen naming reproducible end to end. | [#711](https://github.com/NVlabs/cuda-oxide/pull/711) |
| 8 Aug 2026 | cuda-oxide | `find_inner_verification_error` re-walked the operation tree recursively to name the operation that failed verification. Rewrites the descent as two passes over an explicit stack, preserving the children-before-parent order the recursive contract required, so which operation a multi-failure tree reports stays fixed. Depth tracks region nesting rather than module size, so this was never a live crash, and nothing in the function held that bound in place. First tests for the file, one of which asserts the middle of three malformed siblings is the operation returned. | [#713](https://github.com/NVlabs/cuda-oxide/pull/713) |
| 8 Aug 2026 | cuda-oxide | `verify_operation`'s doc comment described it as mir-importer pipeline plumbing outside the frontend contract, understating its in-crate role. The first version of this PR replaced that with a claim that mir-importer never calls it, which was wrong: it calls it at `mir-importer/src/pipeline.rs:319` through the `__private` re-export, as the per-function post-translation verification step on the live `#[kernel]` path. The corrected comment names the full consumer set and records why the function is `pub` plus `#[doc(hidden)]`, so a later demotion to `pub(crate)` does not look safe. | [#714](https://github.com/NVlabs/cuda-oxide/pull/714) |
<!-- personal:contributions:end id=table -->

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
