
# CRAN-like R package repositories for R-hub

These repositories are **experimental**. They are **not** compatible
with `install.packages()`, only with pak.

* [Ubuntu 22.04 + R-devel](#ubuntu-2204--r-devel-ubuntu-2204-r45)
* [Ubuntu 22.04 + R-devel + libc++](#ubuntu-2204--r-devel--libc-ubuntu-2204-r45-libc)
* [Fedora 38 + R-devel](#fedora-38--r-devel-fedora-38-r45)
* [Fedora 40 + R-devel](#fedora-40--r-devel-fedora-40-r45)
* [Ubuntu 22.04 + R-release on aarch64](#ubuntu-2204--r-release-on-aarch64-ubuntu-2204-aarch64-r44)
* [Ubuntu 24.04 + R-release on aarch64](#ubuntu-2404--r-release-on-aarch64-ubuntu-2404-aarch64-r44)
* [macOS 11 Big Sur or later, x86_64 + R-devel](#macos-11-big-sur-or-later-x86_64--r-devel-macos-x86_64-r45)
* [macOS 11 Big Sur or later, arm64 + R-devel](#macos-11-big-sur-or-later-arm64--r-devel-macos-arm64-r45)
* [Ubuntu 22.04 + R 4.1 on s390x](#ubuntu-2204--r-41-on-s390x-ubuntu-2204-s390x-r41)

## Can use PPPM:

* [x] `ubuntu-next` (CRAN's `r-patched-linux-x86_64`)
* [x] `ubuntu-release` (CRAN's `r-release-linux-x86_64`)

## Ubuntu 22.04 + R-devel (`ubuntu-22.04-R4.5`)

### Setup

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04/4.5",
  CRAN = "https://cloud.r-project.org"
))
```

### Containers using this repo

* [x] `ubuntu-clang` (CRAN's `r-devel-linux-x86_64-debian-clang`)
* [x] `ubuntu-gcc12` (CRAN's `r-devel-linux-x86_64-debian-gcc`)
* [ ] `ubuntu-gcc` (CRAN's `r-devel-linux-x86_64-fedora-gcc`)
* [x] `nold` (extra `noLD`)
* [ ] `lto` (extra `LTO`)
* [x] `donttest` (extra `donttest`)
* [ ] `gcc-asan` (extra `gcc-ASAN` and `gcc-UBSAN`)
* [ ] `noomp` (extra `noOMP`)
* [ ] `rcnst` (extra `rcnst`)
* [ ] `rlibro` (extra `rlibro`)
* [x] `noremap` (extra `noremap`)
* [x] `rchk` (extra `rchk`)

## Ubuntu 22.04 + R-devel + libc++ (`ubuntu-22.04-R4.5-libc++`)

### Setup

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04/4.5/libc++",
  CRAN = "https://cloud.r-project.org"
))
```

### Containers using this repo

* [x] `c23` (extra `C23`)
* [x] `clang-asan` (extra `clang-ASAN`)
* [x] `clang-ubsan` (extra `clang-UBSAN`)
* [x] `clang16`
* [x] `clang17`
* [x] `clang18`
* [x] `clang19`
* [ ] `ubuntu-libc++` (CRAN's `r-devel-linux-x86_64-fedora-clang`)

## Fedora 38 + R-devel (`fedora-38-R4.5`)

### Setup

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/fedora-38/4.5",
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

## Fedora 40 + R-devel (`fedora-40-R4.5`)

### Setup

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/fedora-40/4.5",
  CRAN = "https://cloud.r-project.org"
))
```

### Containers using this repo

* [x] `gcc14` (extra `gcc14`)

## Ubuntu 22.04 + R-release on aarch64 (`ubuntu-22.04-aarch64-R4.4`)

### Setup

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04-aarch64/4.4",
  CRAN = "https://cloud.r-project.org"
))
```

## Ubuntu 24.04 + R-release on aarch64 (`ubuntu-24.04-aarch64-R4.4`)

### Setup

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-24.04-aarch64/4.4",
  CRAN = "https://cloud.r-project.org"
))
```

## macOS 11 Big Sur or later, x86_64 + R-devel (`macos-x86_64-R4.5`)

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/macos-x86_64/4.5",
  CRAN = "https://cloud.r-project.org"
))
```

## macOS 11 Big Sur or later, arm64 + R-devel (`macos-arm64-R4.5`)

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/macos-arm64/4.5",
  CRAN = "https://cloud.r-project.org"
))
```

## Ubuntu 22.04 + R 4.1 on s390x (`ubuntu-22.04-s390x-R4.1`)

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04-s390x/4.1",
  CRAN = "https://cloud.r-project.org"
))
```

## Not needed?

We probably do not need to create containers for these CRAN platforms:

* [ ] extra `BLAS`
* [ ] extra `gcc11`
* [ ] extra `gcc12`

## Not possible (= very hard) currently

We practically cannot implement this platform currently:

* [ ] `m1mac` (extra `M1mac`)

## By CRAN container

[CRAN Package Check Flavors](https://cran.r-project.org/web/checks/check_flavors.html)

Name             | CRAN                              | ✓ | Repo
-----------------|-----------------------------------|---|--------------------------
`ubuntu-clang`   | r-devel-linux-x86_64-debian-clang | ✓ | ubuntu-22.04-R4.5
`ubuntu-gcc12`   | r-devel-linux-x86_64-debian-gcc   | ✓ | ubuntu-22.04-R4.5
`ubuntu-libc++`  | r-devel-linux-x86_64-fedora-clang |   | ubuntu-22.04-R4.5-libc++
`fedora-gcc`     | r-devel-linux-x86_64-fedora-gcc   |   | fedora-38-R4.5
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
`atlas`      | ATLAS      | ✓ | fedora-38-R4.5            | Tests with alternative BLAS/LAPACK implementations
`blas`       | BLAS`      |   |                           | Use of BLAS/LAPACK from C/C++ code
`intel`      | Intel      | ✓ | fedora-38-R4.5            | Checks with Intel oneAPI 2023.x compilers
`lto`        | LTO        |   | ubuntu-22.04-R4.5         | Tests for link-time optimization type mismatches
`m1mac`      | M1mac      |   | CRAN?                     | Checks on a M1 (arm64) Mac
`mkl`        | MKL        | ✓ | fedora-38-R4.5            | Tests with alternative BLAS/LAPACK implementations
`openblas`   | OpenBLAS   |   | fedora-38-R4.5            | Tests with alternative BLAS/LAPACK implementations
`c23`        | `C23`      | ✓ | ubuntu-22.04-R4.5-libc++  | Checks of compiling C code in C23 mode
`clang-asan` | clang-ASAN | ✓ | ubuntu-22.04-R4.5-libc++  | Tests of memory access errors using AddressSanitizer
`clang-ubsan`| clang-UBSAN| ✓ | ubuntu-22.04-R4.5-libc++  | Tests of memory access errors using Undefined Behavior Sanitizer
`clang16`    | clang16    | ✓ | ubuntu-22.04-R4.5-libc++  | Checks with Clang 16.0.0
`clang17`    | clang17    | ✓ | ubuntu-22.04-R4.5-libc++  | Checks with LLVM pre-17.0.0
`clang18`    | clang18    | ✓ | ubuntu-22.04-R4.5-libc++  | Checks with LLVM pre-18.0.0
`clang19`    | clang19    | ✓ | ubuntu-22.04-R4.5-libc++  | Checks with LLVM pre-19.0.0
`donttest`   | donttest   | ✓ | ubuntu-22.04-R4.5         | Tests including `\donttest` examples
`gcc-asan`   | gcc-ASAN   |   | ubuntu-22.04-R4.5         | Tests of memory access errors using AddressSanitizer
`gcc-asan`   | gcc-UBSAN  |   | ubuntu-22.04-R4.5         | Tests of memory access errors using Undefined Behavior Sanitizer
`gcc11`      | gcc11      |   |                           | Checks with GCC trunk aka 11.0
`gcc12`      | gcc12      |   |                           | Installation issues with fedora-gcc but not fedora-clang
`gcc13`      | gcc13      | ✓ | fedora-38-R4.5            | Checks with GCC trunk aka 13.0
`gcc14`      | gcc14      | ✓ | fedora-40-R4.5            | Checks with GCC trunk aka 14.0
`gcc15`      | gcc15      |   |                           | Installation checks with a snapshot of GCC pre-15
`nold`       | noLD`      | ✓ | ubuntu-22.04-R4.5         | Tests without long double
`noomp`      | noOMP      |   | ubuntu-22.04-R4.5         | Tests without OpenMP support
`nosuggests` | noSuggests | ✓ | fedora-38-R4.5            | Tests without suggested packages
`valgrind`   | valgrind   | ✓ | fedora-38-R4.5            | Tests of memory access errors using valgrind
`rchk`       | rchk       | ✓ | ubuntu-22.04-R4.5         | Checks of native code (C/C++) based on static code analysis
`rcnst`      | rcnst      |   | ubuntu-22.04-R4.5         | Checks of corruption of constants
`rlibro`     | rlibro     |   | ubuntu-22.04-R4.5         | Checks with read-only user library
`noremap`    | noRemap    | ✓ | ubuntu-22.04-R4.5         | Checks with `-DR_NO_REMAP` used for C++ code

# License

MIT @ The R Consortium, Posit PBC
