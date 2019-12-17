# Dynamic CPU support for s390x in OpenBLAS

## Description
OpenBLAS (http://www.openblas.net/) is an optimized BLAS (linear algebra) library that can be built for multiple architectures and optimized for multiple architecture levels.
For most architectures the optimization is set during build time, leading to non-optimal performance when application runs on a newer architecture level.
Only Intel/AMD and AArch64 support the dynamic (runtime) selection of the best implementation now.

The goal of this project is to provide the necessary dynamic CPU support code for the s390x architecture.

## Additional Information
https://github.com/xianyi/OpenBLAS/issues/1737 - upstream ticket
https://github.com/xianyi/OpenBLAS/commit/d5aeff636f2d8ba99d1e5ed511c3770970f440af - implementation for AArch64

## Desirable Skills
* C
* Makefile

## Expected Outcome
OpenBLAS is able to select the right optimized library during runtime

## Difficultly
Easy

## Mentors
  * Dan Horák <sharkcz@fedoraproject.org>

## Additional Contacts
* #fedora-s390x on FreeNode IRC
* https://lists.fedoraproject.org/archives/list/s390x@lists.fedoraproject.org/
