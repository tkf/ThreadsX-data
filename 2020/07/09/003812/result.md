# Benchmark result

* Pull request commit: [`3eb34621dbf943b2f401fcb76776257f02eded46`](https://github.com/tkf/ThreadsX.jl/commit/3eb34621dbf943b2f401fcb76776257f02eded46)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Jul 2020 - 00:31
    - Baseline: 9 Jul 2020 - 00:37
* Package commits:
    - Target: 93f77b
    - Baseline: ad3e39
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

| ID                                                                 | time ratio                   | memory ratio                 |
|--------------------------------------------------------------------|------------------------------|------------------------------|
| `["findfirst", "0%", "tx"]`                                        | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx-noterm"]`                                 | 0.72 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                                       |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx-noterm"]`                                |                1.11 (5%) :x: |                1.21 (1%) :x: |
| `["findfirst", "10%", "tx-seq"]`                                   |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx-noterm"]`                                |                1.09 (5%) :x: | 0.67 (1%) :white_check_mark: |
| `["findfirst", "20%", "tx-seq"]`                                   |                1.49 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                                       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                                |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-seq"]`                                   |                1.49 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                                       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                                |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-seq"]`                                   |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                                       | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.16 (5%) :x: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx-seq"]`                                   |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "tx", "A .= B .+ B'"]`                                | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "man"]`                       | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |            45555.56 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |            45841.78 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |            43667.68 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.35 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "Base"]`                                 |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |                1.09 (5%) :x: |                   1.00 (1%)  |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1031-azure #32~18.04.1-Ubuntu SMP Mon Jun 22 15:27:23 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      60259 s          0 s       3027 s      33666 s          0 s
       #2  2095 MHz      47928 s          0 s       2864 s      41505 s          0 s
       
  Memory: 6.764884948730469 GB (1805.3125 MB free)
  Uptime: 1027.0 sec
  Load Avg:  1.2724609375  1.33056640625  0.96728515625
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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1031-azure #32~18.04.1-Ubuntu SMP Mon Jun 22 15:27:23 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      84138 s          0 s       3933 s      45125 s          0 s
       #2  2095 MHz      71693 s          0 s       3485 s      53378 s          0 s
       
  Memory: 6.764884948730469 GB (2237.2421875 MB free)
  Uptime: 1392.0 sec
  Load Avg:  1.3369140625  1.3671875  1.1025390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 9 Jul 2020 - 0:31
* Package commit: 93f77b
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
| `["findfirst", "0%", "base"]`                                      |   2.200 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  18.700 μs (5%) |           |  11.98 KiB (1%) |         220 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  15.800 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 188.539 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  87.700 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  88.100 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 253.401 μs (5%) |           |  39.95 KiB (1%) |         740 |
| `["findfirst", "10%", "tx-seq"]`                                   |  88.100 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 175.201 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 154.301 μs (5%) |           |  21.41 KiB (1%) |         398 |
| `["findfirst", "20%", "tx-noterm"]`                                | 262.001 μs (5%) |           |  28.39 KiB (1%) |         527 |
| `["findfirst", "20%", "tx-seq"]`                                   | 175.900 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 262.900 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 203.101 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 303.000 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 263.401 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 350.401 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 276.101 μs (5%) |           |  35.38 KiB (1%) |         655 |
| `["findfirst", "40%", "tx-noterm"]`                                | 327.301 μs (5%) |           |  35.42 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-seq"]`                                   | 351.001 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 438.001 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 316.800 μs (5%) |           |  37.81 KiB (1%) |         705 |
| `["findfirst", "50%", "tx-noterm"]`                                | 409.501 μs (5%) |           |  49.45 KiB (1%) |         921 |
| `["findfirst", "50%", "tx-seq"]`                                   | 438.801 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 271.841 ms (5%) | 23.873 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 210.728 ms (5%) | 23.805 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   7.054 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.284 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   3.814 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.241 ms (5%) |           |  12.73 KiB (1%) |         123 |
| `["foreach_seq", "base", "Matrix"]`                                | 621.101 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   1.765 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 621.402 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 624.802 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               | 972.003 μs (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 620.902 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  17.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  17.000 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  18.800 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  17.401 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  43.737 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  45.556 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  45.842 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  43.668 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 930.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 947.421 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.300 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.300 μs (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.141 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.693 ms (5%) |           |   1.19 MiB (1%) |         532 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 562.801 μs (5%) |           | 965.13 KiB (1%) |        1227 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 592.301 μs (5%) |           |   1.02 MiB (1%) |        1247 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.494 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.069 ms (5%) |           |   1.19 MiB (1%) |         563 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.441 ms (5%) |           |   1.01 MiB (1%) |        2148 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.974 ms (5%) |           |   1.39 MiB (1%) |        2196 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 114.801 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 104.700 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 104.601 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 103.901 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.367 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.141 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.071 ms (5%) |           |   1.01 MiB (1%) |        2238 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.567 ms (5%) |           |   1.40 MiB (1%) |        2270 |
| `["sort", "reversed", "Base"]`                                     | 595.202 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.092 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 854.002 μs (5%) |           | 998.77 KiB (1%) |        1872 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.208 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["sort", "sorted", "Base"]`                                       | 562.701 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 774.703 μs (5%) |           |   1.18 MiB (1%) |         431 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 806.202 μs (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   | 946.203 μs (5%) |           |   1.36 MiB (1%) |        1903 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   8.227 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.725 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.235 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.944 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1031-azure #32~18.04.1-Ubuntu SMP Mon Jun 22 15:27:23 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      60259 s          0 s       3027 s      33666 s          0 s
       #2  2095 MHz      47928 s          0 s       2864 s      41505 s          0 s
       
  Memory: 6.764884948730469 GB (1805.3125 MB free)
  Uptime: 1027.0 sec
  Load Avg:  1.2724609375  1.33056640625  0.96728515625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 9 Jul 2020 - 0:37
* Package commit: ad3e39
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
| `["findfirst", "0%", "base"]`                                      |   2.200 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  21.600 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  21.800 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 195.989 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  87.600 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  76.401 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 228.100 μs (5%) |           |  33.08 KiB (1%) |         614 |
| `["findfirst", "10%", "tx-seq"]`                                   |  58.700 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 175.200 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 158.700 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 241.101 μs (5%) |           |  42.25 KiB (1%) |         779 |
| `["findfirst", "20%", "tx-seq"]`                                   | 118.201 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 262.801 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 223.401 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 268.401 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 176.400 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 350.401 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 305.101 μs (5%) |           |  35.39 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-noterm"]`                                | 295.501 μs (5%) |           |  35.42 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-seq"]`                                   | 234.701 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 438.001 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 346.001 μs (5%) |           |  37.84 KiB (1%) |         707 |
| `["findfirst", "50%", "tx-noterm"]`                                | 351.701 μs (5%) |           |  54.08 KiB (1%) |        1004 |
| `["findfirst", "50%", "tx-seq"]`                                   | 293.101 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 273.862 ms (5%) | 21.519 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 203.190 ms (5%) | 28.930 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   8.200 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.360 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   4.287 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.191 ms (5%) |           |  12.75 KiB (1%) |         124 |
| `["foreach_seq", "base", "Matrix"]`                                | 620.902 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   1.764 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 621.401 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 628.302 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               | 972.903 μs (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 621.202 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  20.100 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  17.000 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  21.700 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  18.200 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  43.737 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 800.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 700.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.300 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.300 μs (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.124 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.315 ms (5%) |           |   1.19 MiB (1%) |         534 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 499.601 μs (5%) |           | 965.11 KiB (1%) |        1226 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 519.002 μs (5%) |           |   1.02 MiB (1%) |        1246 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.388 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.472 ms (5%) |           |   1.19 MiB (1%) |         563 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.347 ms (5%) |           |   1.01 MiB (1%) |        2147 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.336 ms (5%) |           |   1.39 MiB (1%) |        2196 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 103.801 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 102.800 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 104.700 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 102.000 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.366 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   3.722 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   2.680 ms (5%) |           |   1.01 MiB (1%) |        2238 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.257 ms (5%) |           |   1.40 MiB (1%) |        2271 |
| `["sort", "reversed", "Base"]`                                     | 593.202 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.020 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 777.002 μs (5%) |           | 998.73 KiB (1%) |        1870 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.145 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["sort", "sorted", "Base"]`                                       | 559.502 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 746.402 μs (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 742.503 μs (5%) |           | 998.73 KiB (1%) |        1870 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   | 889.003 μs (5%) |           |   1.36 MiB (1%) |        1903 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   7.859 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.216 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.152 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.518 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1031-azure #32~18.04.1-Ubuntu SMP Mon Jun 22 15:27:23 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      84138 s          0 s       3933 s      45125 s          0 s
       #2  2095 MHz      71693 s          0 s       3485 s      53378 s          0 s
       
  Memory: 6.764884948730469 GB (2237.2421875 MB free)
  Uptime: 1392.0 sec
  Load Avg:  1.3369140625  1.3671875  1.1025390625
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
    CPU MHz:             2095.075
    BogoMIPS:            4190.15
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves
    

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
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

