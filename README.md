
# CRAN-like R package repositories for R-hub

These repositories are **experimental**. They are **not** compatible
with `install.packages()`, only with pak.

## Can use PPPM:

* [x] `ubuntu-next` (CRAN's `r-patched-linux-x86_64`)
* [x] `ubuntu-release` (CRAN's `r-release-linux-x86_64`)

## `ubuntu-22.04-R4.4`

### Setup

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04/4.4",
  CRAN = "https://cloud.r-project.org"
))
```

### Containers using this repo

* [x] `ubuntu-clang` (CRAN's `r-devel-linux-x86_64-debian-clang`)
* [x] `ubuntu-gcc12` (CRAN's `r-devel-linux-x86_64-debian-gcc`)
* [ ] `ubuntu-gcc` (CRAN's `r-devel-linux-x86_64-fedora-gcc`)
* [x] `nold` (extra `noLD`)
* [ ] `c23` (extra `C23`)
* [ ] `lto` (extra `LTO`)
* [x] `donttest` (extra `donttest`)
* [ ] `gcc-asan` (extra `gcc-ASAN` and `gcc-UBSAN`)
* [ ] `noomp` (extra `noOMP`)
* [ ] `rcnst` (extra `rcnst`)
* [ ] `rlibro` (extra `rlibro`)

## `ubuntu-22.04-R4.4-libc++`

### Setup

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04/4.4/libc++",
  CRAN = "https://cloud.r-project.org"
))
```

### Containers using this repo

* [x] `clang-asan` (extra `clang-ASAN` and `clang-UBSAN`)
* [x] `clang16`
* [x] `clang17`
* [x] `clang18`
* [ ] `ubuntu-libc++` (CRAN's `r-devel-linux-x86_64-fedora-clang`)

## `ubuntu-22.04-R4.4-noshlib`

ALthough we can potentially use packages that were built with
a shared R lib, by removing the linkage after installation.

### Containers using this repo

* [ ] `rchk` (extra `rchk`)

## `fedora-38-R4.4`

### Setup

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/fedora-38/4.4",
  CRAN = "https://cloud.r-project.org"
))
```

### Containers using this repo

* [x] `atlas` (extra `ATLAS`)
* [x] `gcc13` (extra `gcc13`)
* [x] `intel` (extra `Intel`)
* [x] `mkl` (extra `MKL`)
* [ ] `openblas` (extra `OpenBLAS`)
* [x] `nosuggests` (extra `noSuggests`)
* [x] `valgrind` (extra `valgrind`)

## Not needed?

* [ ] extra `BLAS`
* [ ] extra `gcc11`
* [ ] extra `gcc12`

## Not possible (= very hard) currently

* [ ] `m1mac` (extra `M1mac`)

## By CRAN container

[CRAN Package Check Flavors](https://cran.r-project.org/web/checks/check_flavors.html)

Name             | CRAN                              | ✓ | Repo
-----------------|-----------------------------------|---|--------------------------
`ubuntu-clang`   | r-devel-linux-x86_64-debian-clang | ✓ | ubuntu-22.04-R4.4
`ubuntu-gcc12`   | r-devel-linux-x86_64-debian-gcc   | ✓ | ubuntu-22.04-R4.4
`ubuntu-libc++`  | r-devel-linux-x86_64-fedora-clang |   | ubuntu-22.04-R4.4-libc++
`fedora-gcc`     | r-devel-linux-x86_64-fedora-gcc   |   | fedora-38-R4.4
`windows`        | r-devel-windows-x86_64            | ✓ | CRAN
`ubuntu-next`    | r-patched-linux-x86_64            | ✓ | PPM
`ubuntu-release` | r-release-linux-x86_64            | ✓ | PPM
`macos-arm64`    | r-release-macos-arm64             | ✓ | CRAN
`macos`          | r-release-macos-x86_64            | ✓ | CRAN
`windows`        | r-release-windows-x86_64          | ✓ | CRAN
`macos-arm64`    | r-oldrel-macos-arm64              | ✓ | CRAN
`windows`        | r-oldrel-windows-x86_64	         | ✓ | CRAN

[CRAN Package Check Issue Kinds](https://cran.r-project.org/web/checks/check_issue_kinds.html)

Name         | CRAN       | ✓ | Repo                      | Description
-------------|------------|---|---------------------------|---------------------------------------------------
`atlas`      | ATLAS      | ✓ | fedora-38-R4.4            | Tests with alternative BLAS/LAPACK implementations
`blas`       | BLAS`      |   |                           | Use of BLAS/LAPACK from C/C++ code
`c23`        | C23        |   | ubuntu-22.04-R4.4         | Checks of compiling C code in C23 mode
`intel`      | Intel      | ✓ | fedora-38-R4.4            | Checks with Intel oneAPI 2023.x compilers
`lto`        | LTO        |   | ubuntu-22.04-R4.4         | Tests for link-time optimization type mismatches
`m1mac`      | M1mac      |   | CRAN?                     | Checks on a M1 (arm64) Mac
`mkl`        | MKL        | ✓ | fedora-38-R4.4            | Tests with alternative BLAS/LAPACK implementations
`openblas`   | OpenBLAS   |   | fedora-38-R4.4            | Tests with alternative BLAS/LAPACK implementations
`clang-asan` | clang-ASAN | ✓ | ubuntu-22.04-R4.4-libc++  | Tests of memory access errors using AddressSanitizer
`clang-asan` | clang-UBSAN| ✓ | ubuntu-22.04-R4.4-libc++  | Tests of memory access errors using Undefined Behavior Sanitizer
`clang16`    | clang16    | ✓ | ubuntu-22.04-R4.4-libc++  | Checks with Clang 16.0.0
`clang17`    | clang17    | ✓ | ubuntu-22.04-R4.4-libc++  | Checks with LLVM pre-17.0.0
`clang18`    | clang18    |   | ubuntu-22.04-R4.4-libc++  | Checks with LLVM pre-18.0.0
`donttest`   | donttest   | ✓ | ubuntu-22.04-R4.4         | Tests including `\donttest` examples
`gcc-asan`   | gcc-ASAN   |   | ubuntu-22.04-R4.4         | Tests of memory access errors using AddressSanitizer
`gcc-asan`   | gcc-UBSAN  |   | ubuntu-22.04-R4.4         | Tests of memory access errors using Undefined Behavior Sanitizer
`gcc11`      | gcc11      |   |                           | Checks with GCC trunk aka 11.0
`gcc12`      | gcc12      |   |                           | Installation issues with fedora-gcc but not fedora-clang
`gcc13`      | gcc13      | ✓ | fedora-38-R4.4            | Checks with GCC trunk aka 13.0
`nold`       | noLD`      | ✓ | ubuntu-22.04-R4.4         | Tests without long double
`noomp`      | noOMP      |   | ubuntu-22.04-R4.4         | Tests without OpenMP support
`nosuggests` | noSuggests | ✓ | fedora-38-R4.4            | Tests without suggested packages
`valgrind`   | valgrind   | ✓ | fedora-38-R4.4            | Tests of memory access errors using valgrind
`rchk`       | rchk       |   | ubuntu-22.04-R4.4-noshlib | Checks of native code (C/C++) based on static code analysis
`rcnst`      | rcnst      |   | ubuntu-22.04-R4.4         | Checks of corruption of constants
`rlibro`     | rlibro     |   | ubuntu-22.04-R4.4         | Checks with read-only user library

# License

MIT @ The R Consortium, Posit PBC
