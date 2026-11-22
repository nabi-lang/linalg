# Changelog

All notable changes to this package. Versions follow semver, independent of the Nabi toolchain.

## 0.1.1 (2026-11-22)

- The crate docs open with a tutorial: matrices and vectors, solving a
  system, least squares, eigenvalues and the SVD. It moved here from the
  Nabi docs site; each step is a doc test.

## 0.1.0 (2026-11-21)

First release.

- Dense linear algebra on core's `Matrix` / `Vector`: f64, f32,
  `Complex<f64>` and `Complex<f32>` wherever the algorithm is the same; no
  BLAS or LAPACK.
- Cache-blocked, parallel products: `matmul`, `matvec`, `dot`, `outer`,
  `kron`, `matrix_power`.
- Factorizations as types (`Lu`, `Cholesky`, `Ldlt`, `Qr`, `Svd`, `Eigh`,
  `Eig`, `Schur`), built by `lu`, `cholesky`, `ldlt`, `qr`, `qr_pivoted`,
  `svd`, `eigh`, `eig`, `schur`.
- Solvers and quantities: `solve`, `lstsq`, `solve_triangular`, `inv`,
  `pinv`, `det`, `slogdet`, `rank`, `cond`, `null_space`, norms, `expm`.
- `AsVector<T>`: the one-dimensional input the science packages share.
- The `ops` feature (default): `@` / `⊡`, `⊗`, `\` / `⧵` and `†`.
- `LinalgError` for bad input. Pure Nabi, every target including wasm.
  Needs Nabi 0.1 or later.
