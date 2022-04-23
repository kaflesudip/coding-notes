# 5 Steps to Speed Up Your Data-Analysis on a Single Core

- Author: Jonathan Striebel
- Talk: https://2022.pycon.de/program/VYS8XY/



## Why speed up?

- Only speed up when it's too slow
- Don't overoptimize berforehand.



## Why speed up on single core?

1. You may not have parallelization
   1. Needs resources [cores, memory, money]
   2. Code may be difficult or sometimes impossible to parallelise
2. When you optimize for single core, pays off when you parallelize



## 5 Steps



### 1. Profiling

- Most important step
- Find what is slow part
- Tools
  1. yappi
  2. **py-spy**
  3. cprofile
  4. pyinstument
  5. palanteer
- All tools except py-spy instrument python code and may make slower
- py-spy is based on rust and is sampling based.



### 2. Efficient IO

- Use binary files instead of Text based
- Text bases
  - CSV
  - JSON
  - YAML
- Binary
  - Hdf5
  - npy
  - parquet
  - pickle
  - sqlite
  - zarr

### 3. Vectorization

- Use Numpy built-in methods
- Pandas may have some bottlenecks. Alternatives
  - Polars: https://github.com/pola-rs/polars
  - Modin [Multi-threaded]
  - Vaex
  - Dask Dataframes



### 4. Memory and Precision Tradeoff

1. Change data types
   1. Sometimes you may not need precision or large values
   2. int32 vs int64
   3. float32 vs float64
2. Use iterative methods
   1. e.g. divide and conquer



### 5. Jit-ing with Numba

- Use decorator
  - @numba.njit

