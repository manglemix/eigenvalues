
[![Build Status](https://github.com/felipeZ/eigenvalues/workflows/build/badge.svg)](https://github.com/felipeZ/eigenvalues/actions)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![crates.io badge](https://img.shields.io/crates/v/eigenvalues.svg)](https://crates.io/crates/eigenvalues)
[![docs](https://docs.rs/eigenvalues/badge.svg)](https://docs.rs/eigenvalues/0.4.0/eigenvalues/)

Eigenvalue Decomposition
========================
This package contains some iterative algorithms for computing the eigenvalues/eigenvectors of a symmetric matrix **H**, implemented in [Rust](https://www.rust-lang.org/).

## Matrix Representation
The library examples represent **H** using the [nalgebra](https://nalgebra.org/) *DMatrix* type, but the matrix **H** does not need to be dense. Sparse or other representations are handled by implementing the `Matrixoperations` trait.

## Available Algorithms:
 * **Davidson** using either  Diagonal-Preconditioned-Residue (**DPR**) or Generalized Jacobi Davidson (**GJD**). See [Davidson Diagonalization Method](https://www.semanticscholar.org/paper/DAVIDSON-DIAGONALIZATION-METHOD-AND-ITS-APPLICATION-Liao/5811eaf768d1a006f505dfe24f329874a679ba59)
 * **Lanczos**, see [Hermitian Lanczos](https://en.wikipedia.org/wiki/Lanczos_algorithm)


### Note:
The Davidson method is suitable for **diagonal-dominant symmetric matrices** that are quite common
in certain scientific problems like [electronic structure calculations](https://en.wikipedia.org/wiki/Electronic_structure). The Davidson method could be not practical
for other kind of symmetric matrices.
