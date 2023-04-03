
# CRAN-like R package repositories for R-hub

These repositories are **experimental**.

## Can use PPPM:

* [ ] `ubuntu-next` (CRAN's `r-patched-linux-x86_64`)
* [ ] `ubuntu-release` (CRAN's `r-release-linux-x86_64`)

## `ubuntu-22.04-R4.4`

* [x] `ubuntu-clang` (CRAN's `r-devel-linux-x86_64-debian-clang`)
* [x] `ubuntu-gcc12` (CRAN's `r-devel-linux-x86_64-debian-gcc`)
* [ ] `ubuntu-gcc` (CRAN's `r-devel-linux-x86_64-fedora-gcc`)
* [x] `nold` (extra `noLD`)
* [ ] `c23` (extra `C23`)
* [ ] `lto` (extra `LTO`)
* [ ] `donttest` (extra `donttest`)
* [ ] `gcc-asan` (extra `gcc-ASAN` and `gcc-UBSAN`)
* [ ] `noomp` (extra `noOMP`)
* [ ] `nosuggests` (extra `noSuggests`)
* [ ] `valgrind` (extra `valgrind`)
* [ ] `rcnst` (extra `rcnst`)
* [ ] `rlibro` (extra `rlibro`)

## `ubuntu-22.04-R4.4-libc++`

* [x] `clang-asan` (extra `clang-ASAN` and `clang-UBSAN`)
* [x] `clang16`
* [ ] `ubuntu-libc++` (CRAN's `r-devel-linux-x86_64-fedora-clang`)

## `ubuntu-22.04-R4.4-noshlib`

ALthough we can potentially use packages that were built with
a shared R lib, by removing the linkage after installation.

* [ ] `rchk` (extra `rchk`)

## `fedora-36-R4.4`

* [x] `atlas` (extra `ATLAS`)
* [ ] `mkl` (extra `MKL`)
* [ ] `openblas` (extra `OpenBLAS`)

## `fedora-38-R4.4`

* [x] `gcc13` (extra `gcc13`)

## Not needed?

* [ ] extra `BLAS`
* [ ] extra `gcc11`
* [ ] extra `gcc12`

# License

MIT @ The R Consortium, Posit PBC
