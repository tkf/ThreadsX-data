# Benchmark result

* Pull request commit: [`76a43ff4f4124ab7ee60f20818bffada19d66876`](https://github.com/tkf/ThreadsX.jl/commit/76a43ff4f4124ab7ee60f20818bffada19d66876)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 18 Sep 2020 - 00:40
    - Baseline: 18 Sep 2020 - 00:46
* Package commits:
    - Target: 08fad8
    - Baseline: a4d2d1
* Julia commits:
    - Target: 44fa15
    - Baseline: 44fa15
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 2`
    - Baseline: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 2`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                                 | time ratio                   | memory ratio  |
|--------------------------------------------------------------------|------------------------------|---------------|
| `["findfirst", "0%", "base"]`                                      |                1.15 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "10%", "base"]`                                     | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                                       |                1.16 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "10%", "tx-noterm"]`                                |                1.34 (5%) :x: | 1.13 (1%) :x: |
| `["findfirst", "10%", "tx-seq"]`                                   | 0.75 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "20%", "base"]`                                     | 0.75 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                                       |                1.14 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "20%", "tx-noterm"]`                                |                1.33 (5%) :x: | 1.17 (1%) :x: |
| `["findfirst", "20%", "tx-seq"]`                                   | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                                       |                1.30 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                                |                1.55 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                                       |                1.26 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                                |                1.32 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "50%", "base"]`                                     | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                                       |                1.23 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.46 (5%) :x: |    1.00 (1%)  |
| `["foreach", "base", "A .= B .+ B'"]`                              | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach", "base", "A .= B .+ C"]`                               | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ C"]`                          | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq", "base", "Matrix"]`                                | 0.67 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq", "base", "Vector"]`                                | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq", "tx", "Vector"]`                                  |                1.34 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |            43740.40 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |            51064.71 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |            43739.39 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.31 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.06 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |                1.11 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |                1.11 (5%) :x: |    1.00 (1%)  |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |                1.06 (5%) :x: |    1.00 (1%)  |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["findfirst", "0%"]`
- `["findfirst", "10%"]`
- `["findfirst", "20%"]`
- `["findfirst", "30%"]`
- `["findfirst", "40%"]`
- `["findfirst", "50%"]`
- `["foreach", "base"]`
- `["foreach", "broadcast"]`
- `["foreach", "tx"]`
- `["foreach_seq", "base"]`
- `["foreach_seq", "tx"]`
- `["foreach_seq_double", "cartesian"]`
- `["foreach_seq_double", "cartesian", "tx"]`
- `["foreach_seq_double", "linear"]`
- `["foreach_seq_double", "linear", "tx"]`
- `["foreach_seq_sum_many", ":nvecs => 8"]`
- `["foreach_seq_sum_many", ":nvecs => 8", "tx"]`
- `["sort", "F64 (narrow)"]`
- `["sort", "F64 (wide)"]`
- `["sort", "I64 (narrow)"]`
- `["sort", "I64 (wide)"]`
- `["sort", "reversed"]`
- `["sort", "sorted"]`
- `["unique", "rand(1:10, 1000000)"]`
- `["unique", "rand(1:1000, 1000000)"]`

## Julia versioninfo

### Target
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1025-azure #25~18.04.1-Ubuntu SMP Sat Sep 5 15:28:57 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      52354 s          0 s       2304 s      41057 s          0 s
       #2  2095 MHz      61319 s          0 s       3187 s      32312 s          0 s
       
  Memory: 6.791393280029297 GB (1848.9453125 MB free)
  Uptime: 984.0 sec
  Load Avg:  1.388671875  1.3759765625  0.9345703125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1025-azure #25~18.04.1-Ubuntu SMP Sat Sep 5 15:28:57 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      69778 s          0 s       2845 s      62345 s          0 s
       #2  2095 MHz      94219 s          0 s       4184 s      37701 s          0 s
       
  Memory: 6.791393280029297 GB (2211.546875 MB free)
  Uptime: 1377.0 sec
  Load Avg:  1.39990234375  1.35400390625  1.0732421875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 18 Sep 2020 - 0:40
* Package commit: 08fad8
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                 | time            | GC time   | memory          | allocations |
|--------------------------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["findfirst", "0%", "base"]`                                      |   3.000 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  25.302 μs (5%) |           |  11.98 KiB (1%) |         220 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  23.102 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 218.567 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  87.606 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  77.806 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 266.120 μs (5%) |           |  39.92 KiB (1%) |         738 |
| `["findfirst", "10%", "tx-seq"]`                                   |  87.806 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 175.312 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 157.711 μs (5%) |           |  21.41 KiB (1%) |         398 |
| `["findfirst", "20%", "tx-noterm"]`                                | 285.120 μs (5%) |           |  33.09 KiB (1%) |         615 |
| `["findfirst", "20%", "tx-seq"]`                                   | 175.913 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 305.327 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 243.521 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 352.830 μs (5%) |           |  28.44 KiB (1%) |         530 |
| `["findfirst", "30%", "tx-seq"]`                                   | 263.723 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 350.527 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 303.923 μs (5%) |           |  35.39 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-noterm"]`                                | 353.927 μs (5%) |           |  35.42 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-seq"]`                                   | 351.126 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 438.136 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 348.028 μs (5%) |           |  37.81 KiB (1%) |         705 |
| `["findfirst", "50%", "tx-noterm"]`                                | 475.238 μs (5%) |           |  54.08 KiB (1%) |        1004 |
| `["findfirst", "50%", "tx-seq"]`                                   | 438.735 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 302.915 ms (5%) | 27.413 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 238.982 ms (5%) | 26.625 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   7.900 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.483 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   4.119 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.334 ms (5%) |           |  12.77 KiB (1%) |         125 |
| `["foreach_seq", "base", "Matrix"]`                                | 651.939 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   1.969 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 626.236 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 849.649 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.048 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 835.648 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  21.101 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  19.901 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  24.702 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  19.001 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  43.941 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  43.740 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  51.065 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  43.739 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.180 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.060 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.678 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.678 μs (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.606 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.086 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 625.339 μs (5%) |           | 965.13 KiB (1%) |        1227 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 617.738 μs (5%) |           |   1.02 MiB (1%) |        1246 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.254 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.815 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.646 ms (5%) |           |   1.01 MiB (1%) |        2147 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.917 ms (5%) |           |   1.39 MiB (1%) |        2198 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 134.409 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 110.406 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 106.107 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 109.107 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   7.646 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   5.040 ms (5%) |           |   1.19 MiB (1%) |         553 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.773 ms (5%) |           |   1.01 MiB (1%) |        2239 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.224 ms (5%) |           |   1.40 MiB (1%) |        2270 |
| `["sort", "reversed", "Base"]`                                     | 811.050 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.316 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 985.160 μs (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.563 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["sort", "sorted", "Base"]`                                       | 770.147 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 935.156 μs (5%) |           |   1.18 MiB (1%) |         431 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 885.553 μs (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.056 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   9.742 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   5.393 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.567 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.597 ms (5%) |           |   1.07 MiB (1%) |        1186 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["findfirst", "0%"]`
- `["findfirst", "10%"]`
- `["findfirst", "20%"]`
- `["findfirst", "30%"]`
- `["findfirst", "40%"]`
- `["findfirst", "50%"]`
- `["foreach", "base"]`
- `["foreach", "broadcast"]`
- `["foreach", "tx"]`
- `["foreach_seq", "base"]`
- `["foreach_seq", "tx"]`
- `["foreach_seq_double", "cartesian"]`
- `["foreach_seq_double", "cartesian", "tx"]`
- `["foreach_seq_double", "linear"]`
- `["foreach_seq_double", "linear", "tx"]`
- `["foreach_seq_sum_many", ":nvecs => 8"]`
- `["foreach_seq_sum_many", ":nvecs => 8", "tx"]`
- `["sort", "F64 (narrow)"]`
- `["sort", "F64 (wide)"]`
- `["sort", "I64 (narrow)"]`
- `["sort", "I64 (wide)"]`
- `["sort", "reversed"]`
- `["sort", "sorted"]`
- `["unique", "rand(1:10, 1000000)"]`
- `["unique", "rand(1:1000, 1000000)"]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1025-azure #25~18.04.1-Ubuntu SMP Sat Sep 5 15:28:57 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      52354 s          0 s       2304 s      41057 s          0 s
       #2  2095 MHz      61319 s          0 s       3187 s      32312 s          0 s
       
  Memory: 6.791393280029297 GB (1848.9453125 MB free)
  Uptime: 984.0 sec
  Load Avg:  1.388671875  1.3759765625  0.9345703125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 18 Sep 2020 - 0:46
* Package commit: a4d2d1
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                 | time            | GC time   | memory          | allocations |
|--------------------------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["findfirst", "0%", "base"]`                                      |   2.601 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  25.604 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  22.503 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 221.802 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     | 101.811 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  67.208 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 198.622 μs (5%) |           |  35.31 KiB (1%) |         653 |
| `["findfirst", "10%", "tx-seq"]`                                   | 117.113 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 233.626 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 138.616 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 214.924 μs (5%) |           |  28.38 KiB (1%) |         526 |
| `["findfirst", "20%", "tx-seq"]`                                   | 204.123 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 305.238 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 186.823 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 227.829 μs (5%) |           |  28.42 KiB (1%) |         529 |
| `["findfirst", "30%", "tx-seq"]`                                   | 263.633 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 350.541 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 240.928 μs (5%) |           |  35.41 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-noterm"]`                                | 267.432 μs (5%) |           |  35.42 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-seq"]`                                   | 351.041 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 468.558 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 282.235 μs (5%) |           |  37.84 KiB (1%) |         707 |
| `["findfirst", "50%", "tx-noterm"]`                                | 325.439 μs (5%) |           |  54.08 KiB (1%) |        1004 |
| `["findfirst", "50%", "tx-seq"]`                                   | 438.853 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 320.474 ms (5%) | 25.427 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 254.033 ms (5%) | 24.778 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   9.394 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   7.062 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   4.217 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.351 ms (5%) |           |  12.77 KiB (1%) |         125 |
| `["foreach_seq", "base", "Matrix"]`                                | 970.183 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.021 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 726.562 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 841.970 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.031 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 625.553 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  20.402 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  21.002 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  25.602 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  20.402 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  43.740 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 900.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.000 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.700 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   3.000 μs (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.495 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.184 ms (5%) |           |   1.19 MiB (1%) |         534 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 604.457 μs (5%) |           | 965.14 KiB (1%) |        1228 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 557.252 μs (5%) |           |   1.02 MiB (1%) |        1248 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.235 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   6.146 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.233 ms (5%) |           |   1.01 MiB (1%) |        2146 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.047 ms (5%) |           |   1.39 MiB (1%) |        2195 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 128.113 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 122.711 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 124.512 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 109.911 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   7.895 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   5.173 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.752 ms (5%) |           |   1.01 MiB (1%) |        2239 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.641 ms (5%) |           |   1.40 MiB (1%) |        2273 |
| `["sort", "reversed", "Base"]`                                     | 812.475 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.351 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.006 ms (5%) |           | 998.72 KiB (1%) |        1869 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.492 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["sort", "sorted", "Base"]`                                       | 765.369 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 960.185 μs (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 895.480 μs (5%) |           | 998.77 KiB (1%) |        1872 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.150 ms (5%) |           |   1.36 MiB (1%) |        1902 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   8.751 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   5.169 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.281 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.265 ms (5%) |           |   1.07 MiB (1%) |        1186 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["findfirst", "0%"]`
- `["findfirst", "10%"]`
- `["findfirst", "20%"]`
- `["findfirst", "30%"]`
- `["findfirst", "40%"]`
- `["findfirst", "50%"]`
- `["foreach", "base"]`
- `["foreach", "broadcast"]`
- `["foreach", "tx"]`
- `["foreach_seq", "base"]`
- `["foreach_seq", "tx"]`
- `["foreach_seq_double", "cartesian"]`
- `["foreach_seq_double", "cartesian", "tx"]`
- `["foreach_seq_double", "linear"]`
- `["foreach_seq_double", "linear", "tx"]`
- `["foreach_seq_sum_many", ":nvecs => 8"]`
- `["foreach_seq_sum_many", ":nvecs => 8", "tx"]`
- `["sort", "F64 (narrow)"]`
- `["sort", "F64 (wide)"]`
- `["sort", "I64 (narrow)"]`
- `["sort", "I64 (wide)"]`
- `["sort", "reversed"]`
- `["sort", "sorted"]`
- `["unique", "rand(1:10, 1000000)"]`
- `["unique", "rand(1:1000, 1000000)"]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1025-azure #25~18.04.1-Ubuntu SMP Sat Sep 5 15:28:57 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      69778 s          0 s       2845 s      62345 s          0 s
       #2  2095 MHz      94219 s          0 s       4184 s      37701 s          0 s
       
  Memory: 6.791393280029297 GB (2211.546875 MB free)
  Uptime: 1377.0 sec
  Load Avg:  1.39990234375  1.35400390625  1.0732421875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:        x86_64
    CPU op-mode(s):      32-bit, 64-bit
    Byte Order:          Little Endian
    CPU(s):              2
    On-line CPU(s) list: 0,1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    NUMA node(s):        1
    Vendor ID:           GenuineIntel
    CPU family:          6
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:            4
    CPU MHz:             2095.247
    BogoMIPS:            4190.49
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

