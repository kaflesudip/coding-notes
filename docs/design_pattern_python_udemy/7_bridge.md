## 1. Motivation

- "Cartesian product" complexity explosion
- E.g. ThreadScheduler that can run on Windows or Unix
- End up 2x2- WindowsPTS, UnixPTS, WindowsCTS, UnixCTS
- It decouples interface (hierarchy) for an implementation (hierarchy)

## 2. Bridge

- circle square
- vector raster
- Goal escape complexity by connecting hierarchy to two classes.
- It is still not very good in terms of Open close principles

## 3. Summary

- Decouple abstraction for implementation
- Stronger form of encapsulation

