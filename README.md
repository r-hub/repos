
# CRAN-like R package repositories for R-hub

These repositories are **experimental**. They are **not** compatible
with `install.packages()`, only with pak.

* [Ubuntu 22.04 + R-devel](#ubuntu-2204--r-devel-ubuntu-2204-r46)
* [Ubuntu 22.04 + R-devel + libc++](#ubuntu-2204--r-devel--libc-ubuntu-2204-r46-libc)
* [Ubuntu 24.04 + R-devel](#ubuntu-2404--r-devel-ubuntu-2404-r46)
* [Ubuntu 22.04 + R-release on aarch64](#ubuntu-2204--r-release-on-aarch64-ubuntu-2204-aarch64-r44)
* [Ubuntu 24.04 + R-release on aarch64](#ubuntu-2404--r-release-on-aarch64-ubuntu-2404-aarch64-r44)
* [Fedora 42 + R-devel](#fedora-42--r-devel-fedora-42-r46)
* [macOS 11 Big Sur or later, x86_64 + R-devel](#macos-11-big-sur-or-later-x86_64--r-devel-macos-x86_64-r46)
* [macOS 11 Big Sur or later, arm64 + R-devel](#macos-11-big-sur-or-later-arm64--r-devel-macos-arm64-r46)
* [Ubuntu 22.04 + R 4.1 on s390x](#ubuntu-2204--r-41-on-s390x-ubuntu-2204-s390x-r41)

<details><summary>Retired repositories</summary>
These are not updated any more, no new packages are added to them,
but existing builds are still functional.

- Fedora 36 + R 4.4 (last update: 2024-03-19)\
  `https://raw.githubusercontent.com/r-hub/repos/main/fedora-36/4.4`
- Fedora 38 + R 4.4 (last update: 2024-03-27)\
  `https://raw.githubusercontent.com/r-hub/repos/main/fedora-38/4.4`
- Fedora 38 + R 4.5 (last update: 2025-03-15)\
  `https://raw.githubusercontent.com/r-hub/repos/main/fedora-38/4.5`
- Fedora 38 + R 4.6 (last update: 2026-03-15)\
  `https://raw.githubusercontent.com/r-hub/repos/main/fedora-38/4.5`
- Fedora 40 + R 4.5 (last update: 2025-03-15)\
  `https://raw.githubusercontent.com/r-hub/repos/main/fedora-40/4.5`
- Fedora 40 + R 4.6 (last update: 2026-03-15)\
  `https://raw.githubusercontent.com/r-hub/repos/main/fedora-40/4.5`
- Ubuntu 22.04 + R 4.3 on aarch64 (last update: 2024-03-20)\
  `https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04-aarch64/4.3`
- Ubuntu 22.04 + R 4.4 on aarch64 (last update: 2024-04-14)\
  `https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04-aarch64/4.4`
- Ubuntu 22.04 + R 4.1 on s390x (last update: 2025-03-15)\
  `https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04-s390x/4.1`
- Ubuntu 22.04 + R 4.4 on x86_64 (last update: 2024-03-27)\
  `https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04/4.4`
- Ubuntu 22.04 + R 4.5 on x86_64 (last update: 2025-03-15)\
  `https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04/4.5`
- Ubuntu 22.04 + R 4.4 + libc++ on x86_64 (last update: 2024-03-27)\
  `https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04/libc++/4.4`
- Ubuntu 22.04 + R 4.5 + libc++ on x86_64 (last update: 2025-03-15)\
  `https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04/libc++/4.5`
- Ubuntu 24.04 + R 4.4 on aarch64 (last update: 2024-04-14)\
  `https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-24.04-aarch64/4.4`
- macOS 11 Big Sur or later, arm64 + R 4.4 (last update: 2024-03-27)\
  `https://raw.githubusercontent.com/r-hub/repos/main/macos-arm64/4.4`
- macOS 11 Big Sur or later, arm64 + R 4.5 (last update: 2025-03-15)\
  `https://raw.githubusercontent.com/r-hub/repos/main/macos-arm64/4.5`
- macOS 11 Big Sur or later, x86_64 + R 4.4 (last update: 2024-03-27)\
  `https://raw.githubusercontent.com/r-hub/repos/main/macos-x86_64/4.4`
- macOS 11 Big Sur or later, x86_64 + R 4.5 (last update: 2025-03-15)\
  `https://raw.githubusercontent.com/r-hub/repos/main/macos-x86_64/4.5`
</details>

## Can use PPPM:

* [x] `ubuntu-next` (CRAN's `r-patched-linux-x86_64`)
* [x] `ubuntu-release` (CRAN's `r-release-linux-x86_64`)

## Ubuntu 22.04 + R-devel (`ubuntu-22.04-R4.6`)

### Setup

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04/4.6",
  CRAN = "https://cloud.r-project.org"
))
```

### Containers using this repo

* [x] `ubuntu-clang` (CRAN's `r-devel-linux-x86_64-debian-clang`)
* [ ] `ubuntu-gcc` (CRAN's `r-devel-linux-x86_64-fedora-gcc`)
* [x] `nold` (extra `noLD`)
* [ ] `lto` (extra `LTO`)
* [x] `donttest` (extra `donttest`)
* [ ] `noomp` (extra `noOMP`)
* [ ] `rcnst` (extra `rcnst`)
* [ ] `rlibro` (extra `rlibro`)
* [x] `rchk` (extra `rchk`)

## Ubuntu 22.04 + R-devel + libc++ (`ubuntu-22.04-R4.6-libc++`)

### Setup

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04/4.6/libc++",
  CRAN = "https://cloud.r-project.org"
))
```

### Containers using this repo

* [x] `clang-asan` (extra `clang-ASAN`)
* [x] `clang-ubsan` (extra `clang-UBSAN`)
* [x] `clang21`
* [x] `clang22`
* [ ] `ubuntu-libc++` (CRAN's `r-devel-linux-x86_64-fedora-clang`)

## Ubuntu 24.04 + R-devel (`ubuntu-24.04-R4.6`)

### Setup

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-24.04/4.6",
  CRAN = "https://cloud.r-project.org"
))
```

### Containers using this repo

* [x] `ubuntu-gcc15` (CRAN's `r-devel-linux-x86_64-debian-gcc`)

## Fedora 42 + R-devel (`fedora-42-R4.6`)

### Setup

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/fedora-42/4.6",
  CRAN = "https://cloud.r-project.org"
))
```

### Containers using this repo

* [x] `atlas` (extra `ATLAS`)
* [x] `gcc-asan` (extra `gcc-ASAN` and `gcc-UBSAN`)
* [x] `mkl` (extra `MKL`)
* [ ] `openblas` (extra `OpenBLAS`)
* [x] `nosuggests` (extra `noSuggests`)
* [x] `valgrind` (extra `valgrind`)

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

## macOS 11 Big Sur or later, x86_64 + R-devel (`macos-x86_64-R4.6`)

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/macos-x86_64/4.6",
  CRAN = "https://cloud.r-project.org"
))
```

## macOS 11 Big Sur or later, arm64 + R-devel (`macos-arm64-R4.6`)

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/macos-arm64/4.6",
  CRAN = "https://cloud.r-project.org"
))
```

## Ubuntu 22.04 + R 4.3 on s390x (`ubuntu-22.04-s390x-R4.3`)

```
options(repos = c(
  RHUB = "https://raw.githubusercontent.com/r-hub/repos/main/ubuntu-22.04-s390x/4.3",
  CRAN = "https://cloud.r-project.org"
))
```

## Not needed?

We probably do not need to create containers for these CRAN platforms:

* [ ] extra `BLAS`

## Not possible (= very hard) currently

We practically cannot implement this platform currently:

* [ ] `m1mac` (extra `M1mac`)

## By CRAN container

[CRAN Package Check Flavors](https://cran.r-project.org/web/checks/check_flavors.html)

Name             | CRAN                              | ✓ | Repo
-----------------|-----------------------------------|---|--------------------------
`ubuntu-clang`   | r-devel-linux-x86_64-debian-clang | ✓ | ubuntu-22.04-R4.6
`ubuntu-gcc15`   | r-devel-linux-x86_64-debian-gcc   | ✓ | ubuntu-24.04-R4.6
`ubuntu-libc++`  | r-devel-linux-x86_64-fedora-clang |   | ubuntu-22.04-R4.6-libc++
`fedora-gcc`     | r-devel-linux-x86_64-fedora-gcc   |   | fedora-42-R4.6
`windows`        | r-devel-windows-x86_64            | ✓ | CRAN
`ubuntu-next`    | r-patched-linux-x86_64            | ✓ | PPM
`ubuntu-release` | r-release-linux-x86_64            | ✓ | PPM
`macos-arm64`    | r-release-macos-arm64             | ✓ | CRAN
`macos`          | r-release-macos-x86_64            | ✓ | CRAN
`windows`        | r-release-windows-x86_64          | ✓ | CRAN
`macos-arm64`    | r-oldrel-macos-arm64              | ✓ | CRAN
`windows`        | r-oldrel-windows-x86_64	     | ✓ | CRAN

[CRAN Package Check Issue Kinds](https://cran.r-project.org/web/checks/check_issue_kinds.html)

Name         | CRAN       | ✓ | Repo                      | Description
-------------|------------|---|---------------------------|---------------------------------------------------
`atlas`      | ATLAS      | ✓ | fedora-42-R4.6            | Tests with alternative BLAS/LAPACK implementations
`blas`       | BLAS       |   |                           | Use of BLAS/LAPACK from C/C++ code
`clang-asan` | clang-ASAN | ✓ | ubuntu-22.04-R4.6-libc++  | Tests of memory access errors using AddressSanitizer
`clang-ubsan`| clang-UBSAN| ✓ | ubuntu-22.04-R4.6-libc++  | Tests of memory access errors using Undefined Behavior Sanitizer
`clang21`    | clang21    | ✓ | ubuntu-22.04-R4.6-libc++  | Checks with LLVM 21.x
`clang22`    | clang22    | ✓ | ubuntu-22.04-R4.6-libc++  | Checks with LLVM 22.x
`donttest`   | donttest   | ✓ | ubuntu-22.04-R4.6         | Tests including `\donttest` examples
`gcc-asan`   | gcc-ASAN   | ✓ | fedora-42-R4.6            | Tests of memory access errors using AddressSanitizer
`gcc-asan`   | gcc-UBSAN  | ✓ | fedora-42-R4.6            | Tests of memory access errors using Undefined Behavior Sanitizer
`gcc16`      | gcc16      | ✓ |                           | Installation checks with a snapshot of GCC pre-16
`lto`        | LTO        |   | ubuntu-22.04-R4.6         | Tests for link-time optimization type mismatches
`m1mac`      | M1mac      |   | CRAN?                     | Checks on a M1 (arm64) Mac
`mkl`        | MKL        | ✓ | fedora-42-R4.6            | Tests with alternative BLAS/LAPACK implementations
`nold`       | noLD       | ✓ | ubuntu-22.04-R4.6         | Tests without long double
`noomp`      | noOMP      |   | ubuntu-22.04-R4.6         | Tests without OpenMP support
`nosuggests` | noSuggests | ✓ | fedora-42-R4.6            | Tests without suggested packages
`openblas`   | OpenBLAS   |   | fedora-42-R4.6            | Tests with alternative BLAS/LAPACK implementations
`rchk`       | rchk       | ✓ | ubuntu-22.04-R4.6         | Checks of native code (C/C++) based on static code analysis
`rcnst`      | rcnst      |   | ubuntu-22.04-R4.6         | Checks of corruption of constants
`rlibro`     | rlibro     |   | ubuntu-22.04-R4.6         | Checks with read-only user library
`valgrind`   | valgrind   | ✓ | fedora-42-R4.6            | Tests of memory access errors using valgrind

### Deprecated containers

<details><summary>See list.</summary>

Name         | CRAN       | ✓ | Repo                      | Description
-------------|------------|---|---------------------------|---------------------------------------------------
`c23`        | C23        | ✓ | ubuntu-22.04-R4.6-libc++  | Checks of compiling C code in C23 mode
`clang16`    | clang16    | ✓ | ubuntu-22.04-R4.6-libc++  | Checks with Clang 16.0.0
`clang17`    | clang17    | ✓ | ubuntu-22.04-R4.6-libc++  | Checks with LLVM pre-17.0.0
`clang18`    | clang18    | ✓ | ubuntu-22.04-R4.6-libc++  | Checks with LLVM pre-18.0.0
`clang19`    | clang19    | ✓ | ubuntu-22.04-R4.6-libc++  | Checks with LLVM pre-19.0.0
`clang20`    | clang20    | ✓ | ubuntu-22.04-R4.6-libc++  | Checks with LLVM pre-20.0.0
`gcc13`      | gcc13      | ✓ | fedora-38-R4.6            | Checks with GCC trunk aka 13.0
`gcc14`      | gcc14      | ✓ | fedora-40-R4.6            | Checks with GCC trunk aka 14.0
`gcc15`      | gcc15      |   | fedora-42-R4.6            | Installation checks with a snapshot of GCC pre-15
`intel`      | Intel      | ✓ | fedora-38-R4.6            | Checks with Intel oneAPI 2023.x compilers
`noremap`    | noRemap    | ✓ | ubuntu-22.04-R4.6         | Checks with `-DR_NO_REMAP` used for C++ code

</details>

# License

MIT @ The R Consortium, Posit PBC
