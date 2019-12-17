# Optimized graphics routines for s390x in pixman

## Description
Pixman (http://www.pixman.org/) is a library that provides low-level pixel manipulation features such as image compositing and trapezoid rasterization.

With the introduction of VirtIO GPU hardware (virtual graphic adapter for KVM-based virtual machines) for the s390x platform it makes sense
to provide optimized routines in the pixman library also the s390x architecture. AFAIK a VNC based desktop environment also uses pixman underneath.

## Additional Information
* https://cgit.freedesktop.org/pixman/tree/pixman/pixman-vmx.c - implementation for Power VMX SIMD

## Desirable Skills
* C
* graphics algorithms
* vector/SIMD instructions for s390x

## Expected Outcome
OpenBLAS is able to select the right optimized library during runtime

## Difficultly
Medium

## Mentors
  * Dan Horák <sharkcz@fedoraproject.org>

## Additional Contacts
* #fedora-s390x on FreeNode IRC
* https://lists.fedoraproject.org/archives/list/s390x@lists.fedoraproject.org/
