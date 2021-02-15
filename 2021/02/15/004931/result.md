# Benchmark result

* Pull request commit: [`b869342b7391766e32348d1757554a21f26fbabf`](https://github.com/tkf/ThreadsX.jl/commit/b869342b7391766e32348d1757554a21f26fbabf)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 15 Feb 2021 - 00:41
    - Baseline: 15 Feb 2021 - 00:48
* Package commits:
    - Target: 045b54
    - Baseline: 9d3911
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
| `["findfirst", "0%", "base"]`                                      | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx"]`                                        |                   1.02 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "0%", "tx-noterm"]`                                 |               27.52 (5%) :x: |                2.06 (1%) :x: |
| `["findfirst", "0%", "tx-seq"]`                                    | 0.68 (5%) :white_check_mark: | 0.71 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx"]`                                       |                3.75 (5%) :x: |                2.90 (1%) :x: |
| `["findfirst", "10%", "tx-noterm"]`                                |                3.10 (5%) :x: | 0.53 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "20%", "tx"]`                                       |                2.46 (5%) :x: |                1.74 (1%) :x: |
| `["findfirst", "20%", "tx-noterm"]`                                |                2.70 (5%) :x: | 0.59 (1%) :white_check_mark: |
| `["findfirst", "20%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "30%", "tx"]`                                       |                1.99 (5%) :x: |                   0.99 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                                |                2.84 (5%) :x: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "30%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx"]`                                       |                1.73 (5%) :x: | 0.99 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx-noterm"]`                                |                3.06 (5%) :x: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx"]`                                       |                1.88 (5%) :x: |                1.41 (1%) :x: |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.92 (5%) :x: | 0.46 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx-seq"]`                                   |                1.09 (5%) :x: | 0.72 (1%) :white_check_mark: |
| `["foreach", "base", "A .= B .+ C"]`                               | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |                2.45 (5%) :x: |                   1.00 (1%)  |
| `["foreach", "tx", "A .= B .+ B'"]`                                |                2.38 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Transpose"]`                             | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Vector"]`                                |                1.33 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Matrix"]`                                  | 0.75 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Transpose"]`                               |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "man"]`                       |                1.30 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |            43667.68 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |            45233.27 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |            43737.37 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapi", "collatz", "base"]`                                      | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                                        | 0.93 (5%) :white_check_mark: |                1.06 (1%) :x: |
| `["sort", "F64 (narrow)", "Base"]`                                 |                1.24 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "Base"]`                                   |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   |                   1.01 (5%)  | 0.59 (1%) :white_check_mark: |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   |                   0.98 (5%)  | 0.59 (1%) :white_check_mark: |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             |                   1.01 (5%)  | 0.59 (1%) :white_check_mark: |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sort", "sorted", "Base"]`                                       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          | 0.92 (5%) :white_check_mark: | 0.55 (1%) :white_check_mark: |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |                   0.96 (5%)  | 0.98 (1%) :white_check_mark: |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1039-azure #41-Ubuntu SMP Mon Jan 18 13:22:11 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      64064 s         18 s       2699 s      36284 s          0 s
       #2  2095 MHz      67336 s          6 s       2750 s      33137 s          0 s
       
  Memory: 6.791374206542969 GB (2321.81640625 MB free)
  Uptime: 1048.0 sec
  Load Avg:  1.28076171875  1.33056640625  1.00341796875
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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1039-azure #41-Ubuntu SMP Mon Jan 18 13:22:11 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      93492 s         18 s       3728 s      49624 s          0 s
       #2  2095 MHz      94007 s          6 s       3540 s      49416 s          0 s
       
  Memory: 6.791374206542969 GB (2698.28125 MB free)
  Uptime: 1486.0 sec
  Load Avg:  1.22607421875  1.3154296875  1.11181640625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 15 Feb 2021 - 0:41
* Package commit: 045b54
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
| `["findfirst", "0%", "base"]`                                      |   3.100 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  23.100 μs (5%) |           |  11.77 KiB (1%) |         218 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 575.204 μs (5%) |           |  24.70 KiB (1%) |         245 |
| `["findfirst", "0%", "tx-seq"]`                                    | 132.800 ns (5%) |           |  400 bytes (1%) |          13 |
| `["findfirst", "10%", "base"]`                                     |  87.601 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       | 252.902 μs (5%) |           |  41.84 KiB (1%) |         779 |
| `["findfirst", "10%", "tx-noterm"]`                                | 595.303 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "10%", "tx-seq"]`                                   |  88.001 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "20%", "base"]`                                     | 175.401 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 283.201 μs (5%) |           |  37.27 KiB (1%) |         694 |
| `["findfirst", "20%", "tx-noterm"]`                                | 582.103 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "20%", "tx-seq"]`                                   | 175.801 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "30%", "base"]`                                     | 281.402 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 357.303 μs (5%) |           |  28.09 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-noterm"]`                                | 588.604 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "30%", "tx-seq"]`                                   | 263.402 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "40%", "base"]`                                     | 350.502 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 382.003 μs (5%) |           |  35.05 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-noterm"]`                                | 707.004 μs (5%) |           |  24.80 KiB (1%) |         251 |
| `["findfirst", "40%", "tx-seq"]`                                   | 350.902 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "50%", "base"]`                                     | 438.103 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 520.304 μs (5%) |           |  53.56 KiB (1%) |        1001 |
| `["findfirst", "50%", "tx-noterm"]`                                | 632.803 μs (5%) |           |  24.91 KiB (1%) |         258 |
| `["findfirst", "50%", "tx-seq"]`                                   | 478.303 μs (5%) |           |  416 bytes (1%) |          14 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 342.577 ms (5%) | 31.610 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 238.777 ms (5%) | 32.146 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  33.258 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   7.459 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |  16.638 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.761 ms (5%) |           |  12.77 KiB (1%) |         125 |
| `["foreach_seq", "base", "Matrix"]`                                | 835.904 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.917 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 835.994 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 632.301 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   2.381 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 622.001 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  23.200 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  20.200 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  26.600 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  17.500 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  43.769 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  43.668 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  45.233 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  43.737 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 920.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 930.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.311 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.311 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 353.866 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 226.469 ms (5%) |  6.215 ms | 160.76 MiB (1%) |     2016645 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.182 ms (5%) |           |  59.25 KiB (1%) |        1115 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.282 ms (5%) |           |  60.00 KiB (1%) |        1130 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.865 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.002 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 605.804 μs (5%) |           | 965.14 KiB (1%) |        1228 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 570.003 μs (5%) |           |   1.02 MiB (1%) |        1248 |
| `["sort", "F64 (wide)", "Base"]`                                   |   7.124 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   6.004 ms (5%) |           |   1.19 MiB (1%) |         563 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.208 ms (5%) |           |   1.01 MiB (1%) |        2149 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.549 ms (5%) |           |   1.39 MiB (1%) |        2197 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 118.301 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 107.701 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 107.501 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 108.100 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (wide)", "Base"]`                                   |   7.468 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   5.237 ms (5%) |           |   1.19 MiB (1%) |         549 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.813 ms (5%) |           |   1.01 MiB (1%) |        2229 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.537 ms (5%) |           |   1.39 MiB (1%) |        2267 |
| `["sort", "reversed", "Base"]`                                     | 804.805 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.253 ms (5%) |           |   1.18 MiB (1%) |         430 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 938.305 μs (5%) |           | 998.41 KiB (1%) |        1866 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.411 ms (5%) |           |   1.36 MiB (1%) |        1899 |
| `["sort", "sorted", "Base"]`                                       | 768.005 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 906.106 μs (5%) |           |   1.18 MiB (1%) |         427 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 948.006 μs (5%) |           | 998.41 KiB (1%) |        1866 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.159 ms (5%) |           |   1.36 MiB (1%) |        1899 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |  10.117 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   5.138 ms (5%) |           |  27.81 KiB (1%) |         352 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   9.078 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.408 ms (5%) |           |   1.04 MiB (1%) |         656 |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1039-azure #41-Ubuntu SMP Mon Jan 18 13:22:11 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      64064 s         18 s       2699 s      36284 s          0 s
       #2  2095 MHz      67336 s          6 s       2750 s      33137 s          0 s
       
  Memory: 6.791374206542969 GB (2321.81640625 MB free)
  Uptime: 1048.0 sec
  Load Avg:  1.28076171875  1.33056640625  1.00341796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 15 Feb 2021 - 0:48
* Package commit: 9d3911
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
| `["findfirst", "0%", "tx"]`                                        |  22.600 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  20.900 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 196.302 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  87.600 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  67.400 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 191.802 μs (5%) |           |  46.81 KiB (1%) |         860 |
| `["findfirst", "10%", "tx-seq"]`                                   |  87.900 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 175.301 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 115.300 μs (5%) |           |  21.41 KiB (1%) |         398 |
| `["findfirst", "20%", "tx-noterm"]`                                | 215.702 μs (5%) |           |  42.25 KiB (1%) |         779 |
| `["findfirst", "20%", "tx-seq"]`                                   | 175.901 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 278.402 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 179.201 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 207.302 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 263.402 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 350.501 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 220.501 μs (5%) |           |  35.41 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-noterm"]`                                | 231.301 μs (5%) |           |  35.39 KiB (1%) |         655 |
| `["findfirst", "40%", "tx-seq"]`                                   | 351.102 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 438.102 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 276.802 μs (5%) |           |  37.86 KiB (1%) |         708 |
| `["findfirst", "50%", "tx-noterm"]`                                | 329.601 μs (5%) |           |  54.08 KiB (1%) |        1004 |
| `["findfirst", "50%", "tx-seq"]`                                   | 438.703 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 327.719 ms (5%) | 32.742 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 253.545 ms (5%) | 33.175 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  13.565 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   7.312 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   6.977 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.717 ms (5%) |           |  12.77 KiB (1%) |         125 |
| `["foreach_seq", "base", "Matrix"]`                                | 835.805 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   3.178 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 627.401 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 843.205 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   2.055 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 626.904 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  17.800 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  18.400 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  23.200 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  16.700 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  43.769 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 800.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 900.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.700 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.700 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 383.147 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 244.403 ms (5%) |  6.398 ms | 151.44 MiB (1%) |     2016678 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.180 ms (5%) |           |  59.22 KiB (1%) |        1114 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.282 ms (5%) |           |  59.94 KiB (1%) |        1132 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.307 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.907 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 574.703 μs (5%) |           | 965.16 KiB (1%) |        1229 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 590.803 μs (5%) |           |   1.02 MiB (1%) |        1249 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.344 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   6.134 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.156 ms (5%) |           |   1.01 MiB (1%) |        2148 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.934 ms (5%) |           |   1.39 MiB (1%) |        2197 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 118.700 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 106.600 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 109.901 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 106.701 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   7.544 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   5.093 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.714 ms (5%) |           |   1.01 MiB (1%) |        2239 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.433 ms (5%) |           |   1.40 MiB (1%) |        2272 |
| `["sort", "reversed", "Base"]`                                     | 797.705 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.154 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 919.805 μs (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.403 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["sort", "sorted", "Base"]`                                       | 819.305 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 914.106 μs (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 926.905 μs (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.049 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   9.947 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   5.589 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   9.081 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.662 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1039-azure #41-Ubuntu SMP Mon Jan 18 13:22:11 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      93492 s         18 s       3728 s      49624 s          0 s
       #2  2095 MHz      94007 s          6 s       3540 s      49416 s          0 s
       
  Memory: 6.791374206542969 GB (2698.28125 MB free)
  Uptime: 1486.0 sec
  Load Avg:  1.22607421875  1.3154296875  1.11181640625
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

    Architecture:                    x86_64
    CPU op-mode(s):                  32-bit, 64-bit
    Byte Order:                      Little Endian
    Address sizes:                   46 bits physical, 48 bits virtual
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    NUMA node(s):                    1
    Vendor ID:                       GenuineIntel
    CPU family:                      6
    Model:                           85
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:                        4
    CPU MHz:                         2095.078
    BogoMIPS:                        4190.15
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2 MiB
    L3 cache:                        35.8 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Vulnerable
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

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

