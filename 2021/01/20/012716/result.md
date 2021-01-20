# Benchmark result

* Pull request commit: [`2e25d8599fc3fc29aa22400d58c076a1dadbd959`](https://github.com/tkf/ThreadsX.jl/commit/2e25d8599fc3fc29aa22400d58c076a1dadbd959)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 20 Jan 2021 - 01:19
    - Baseline: 20 Jan 2021 - 01:26
* Package commits:
    - Target: cec925
    - Baseline: 819e90
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
| `["findfirst", "0%", "base"]`                                      | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx-noterm"]`                                 | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                                       |                1.39 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx-noterm"]`                                |                1.48 (5%) :x: |                1.28 (1%) :x: |
| `["findfirst", "20%", "tx"]`                                       |                1.39 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx-noterm"]`                                |                1.56 (5%) :x: | 0.78 (1%) :white_check_mark: |
| `["findfirst", "30%", "base"]`                                     | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                                       |                1.31 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                                |                1.49 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                                       |                1.38 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                                |                1.64 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                                       |                1.34 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.78 (5%) :x: |                   1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Matrix"]`                                | 0.75 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Transpose"]`                             | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Vector"]`                                  |                1.34 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "man"]`                       |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |                1.24 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |            44277.61 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |            45271.62 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |            43904.47 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "collatz", "base"]`                                      | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                                        |                   0.96 (5%)  | 0.95 (1%) :white_check_mark: |
| `["mapi", "consume-100us", "tx"]`                                  |                   0.99 (5%)  |                1.01 (1%) :x: |
| `["mapi", "consume-1ms", "tx"]`                                    |                   1.00 (5%)  |                1.02 (1%) :x: |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "Base"]`                                   |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |                1.09 (5%) :x: |                   1.00 (1%)  |

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
- `["mapi", "collatz"]`
- `["mapi", "consume-100us"]`
- `["mapi", "consume-1ms"]`
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
  uname: Linux 5.4.0-1036-azure #38~18.04.1-Ubuntu SMP Wed Jan 6 18:26:30 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      60156 s          0 s       3010 s      47430 s          0 s
       #2  2095 MHz      66771 s          0 s       3000 s      41257 s          0 s
       
  Memory: 6.791393280029297 GB (2440.08984375 MB free)
  Uptime: 1124.0 sec
  Load Avg:  1.26416015625  1.33154296875  0.9658203125
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
  uname: Linux 5.4.0-1036-azure #38~18.04.1-Ubuntu SMP Wed Jan 6 18:26:30 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      91500 s          0 s       3875 s      58929 s          0 s
       #2  2095 MHz      91582 s          0 s       3988 s      59161 s          0 s
       
  Memory: 6.791393280029297 GB (2853.90625 MB free)
  Uptime: 1562.0 sec
  Load Avg:  1.28857421875  1.3642578125  1.11767578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 20 Jan 2021 - 1:19
* Package commit: cec925
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
| `["findfirst", "0%", "tx"]`                                        |  26.101 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  21.100 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 195.672 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  87.602 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  93.003 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 284.008 μs (5%) |           |  42.31 KiB (1%) |         784 |
| `["findfirst", "10%", "tx-seq"]`                                   |  88.002 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 175.304 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 183.304 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 302.408 μs (5%) |           |  33.08 KiB (1%) |         614 |
| `["findfirst", "20%", "tx-seq"]`                                   | 176.004 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 284.808 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 234.706 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 321.309 μs (5%) |           |  28.42 KiB (1%) |         529 |
| `["findfirst", "30%", "tx-seq"]`                                   | 263.507 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 350.509 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 328.709 μs (5%) |           |  35.39 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-noterm"]`                                | 384.610 μs (5%) |           |  35.42 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-seq"]`                                   | 351.309 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 438.212 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 371.610 μs (5%) |           |  37.81 KiB (1%) |         705 |
| `["findfirst", "50%", "tx-noterm"]`                                | 533.714 μs (5%) |           |  54.06 KiB (1%) |        1003 |
| `["findfirst", "50%", "tx-seq"]`                                   | 438.812 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 361.961 ms (5%) | 38.434 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 260.130 ms (5%) | 36.163 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  33.572 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   7.303 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |  17.230 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.834 ms (5%) |           |  12.77 KiB (1%) |         125 |
| `["foreach_seq", "base", "Matrix"]`                                | 626.432 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.983 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 627.132 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 843.142 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.997 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 835.942 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  20.401 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  18.601 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  22.702 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  19.601 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  43.974 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  44.278 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  45.272 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  43.904 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 931.579 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 931.069 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.300 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.311 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 356.957 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 234.537 ms (5%) |  6.635 ms | 155.53 MiB (1%) |     2016683 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.176 ms (5%) |           |  59.52 KiB (1%) |        1122 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.320 ms (5%) |           |  59.88 KiB (1%) |        1131 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.391 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.099 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 599.737 μs (5%) |           | 965.14 KiB (1%) |        1228 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 622.338 μs (5%) |           |   1.02 MiB (1%) |        1247 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.500 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   6.077 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.879 ms (5%) |           |   1.01 MiB (1%) |        2149 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.897 ms (5%) |           |   1.39 MiB (1%) |        2196 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 121.003 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 109.203 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 109.003 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 108.207 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   7.342 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   5.155 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.696 ms (5%) |           |   1.01 MiB (1%) |        2237 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.433 ms (5%) |           |   1.40 MiB (1%) |        2270 |
| `["sort", "reversed", "Base"]`                                     | 802.948 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.277 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 932.755 μs (5%) |           | 998.77 KiB (1%) |        1872 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.500 ms (5%) |           |   1.36 MiB (1%) |        1902 |
| `["sort", "sorted", "Base"]`                                       | 795.446 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 901.150 μs (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 963.054 μs (5%) |           | 998.72 KiB (1%) |        1869 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.099 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   9.269 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   5.359 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.800 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.685 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
- `["mapi", "collatz"]`
- `["mapi", "consume-100us"]`
- `["mapi", "consume-1ms"]`
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
  uname: Linux 5.4.0-1036-azure #38~18.04.1-Ubuntu SMP Wed Jan 6 18:26:30 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      60156 s          0 s       3010 s      47430 s          0 s
       #2  2095 MHz      66771 s          0 s       3000 s      41257 s          0 s
       
  Memory: 6.791393280029297 GB (2440.08984375 MB free)
  Uptime: 1124.0 sec
  Load Avg:  1.26416015625  1.33154296875  0.9658203125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 20 Jan 2021 - 1:26
* Package commit: 819e90
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
| `["findfirst", "0%", "base"]`                                      |   3.500 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  24.901 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  22.601 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 196.294 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  87.603 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  67.003 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 191.407 μs (5%) |           |  33.00 KiB (1%) |         612 |
| `["findfirst", "10%", "tx-seq"]`                                   |  87.903 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 175.306 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 131.405 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 194.308 μs (5%) |           |  42.25 KiB (1%) |         779 |
| `["findfirst", "20%", "tx-seq"]`                                   | 175.906 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 305.212 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 179.507 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 215.809 μs (5%) |           |  28.39 KiB (1%) |         527 |
| `["findfirst", "30%", "tx-seq"]`                                   | 263.410 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 350.514 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 238.510 μs (5%) |           |  35.41 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-noterm"]`                                | 234.709 μs (5%) |           |  35.44 KiB (1%) |         658 |
| `["findfirst", "40%", "tx-seq"]`                                   | 351.114 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 438.117 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 277.811 μs (5%) |           |  37.84 KiB (1%) |         707 |
| `["findfirst", "50%", "tx-noterm"]`                                | 299.512 μs (5%) |           |  54.08 KiB (1%) |        1004 |
| `["findfirst", "50%", "tx-seq"]`                                   | 438.917 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 361.469 ms (5%) | 33.281 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 255.137 ms (5%) | 31.962 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  32.708 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.948 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |  16.942 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.720 ms (5%) |           |  12.77 KiB (1%) |         125 |
| `["foreach_seq", "base", "Matrix"]`                                | 836.027 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   3.436 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 629.720 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 843.627 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.965 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 625.120 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  17.200 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  17.701 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  18.301 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  20.201 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  43.770 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 900.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 800.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.300 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.300 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 382.830 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 245.346 ms (5%) |  8.733 ms | 162.96 MiB (1%) |     2016652 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.187 ms (5%) |           |  58.91 KiB (1%) |        1110 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.277 ms (5%) |           |  58.86 KiB (1%) |        1111 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.399 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.865 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 548.518 μs (5%) |           | 965.14 KiB (1%) |        1228 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 581.319 μs (5%) |           |   1.02 MiB (1%) |        1247 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.539 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   6.068 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.246 ms (5%) |           |   1.01 MiB (1%) |        2149 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.018 ms (5%) |           |   1.39 MiB (1%) |        2196 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 121.704 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 108.604 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 107.903 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 108.404 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   6.482 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.601 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.474 ms (5%) |           |   1.01 MiB (1%) |        2237 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.160 ms (5%) |           |   1.40 MiB (1%) |        2273 |
| `["sort", "reversed", "Base"]`                                     | 798.727 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.123 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 905.630 μs (5%) |           | 998.70 KiB (1%) |        1868 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.307 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["sort", "sorted", "Base"]`                                       | 760.626 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 807.527 μs (5%) |           |   1.18 MiB (1%) |         431 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 834.928 μs (5%) |           | 998.72 KiB (1%) |        1869 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.062 ms (5%) |           |   1.36 MiB (1%) |        1902 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   9.325 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   5.150 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.086 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.725 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
- `["mapi", "collatz"]`
- `["mapi", "consume-100us"]`
- `["mapi", "consume-1ms"]`
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
  uname: Linux 5.4.0-1036-azure #38~18.04.1-Ubuntu SMP Wed Jan 6 18:26:30 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      91500 s          0 s       3875 s      58929 s          0 s
       #2  2095 MHz      91582 s          0 s       3988 s      59161 s          0 s
       
  Memory: 6.791393280029297 GB (2853.90625 MB free)
  Uptime: 1562.0 sec
  Load Avg:  1.28857421875  1.3642578125  1.11767578125
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
    CPU MHz:             2095.112
    BogoMIPS:            4190.22
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

