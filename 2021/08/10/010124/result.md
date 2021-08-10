# Benchmark result

* Pull request commit: [`9ffeb6ee7ba57f64c8e1ba81640a1d3ae866c136`](https://github.com/tkf/ThreadsX.jl/commit/9ffeb6ee7ba57f64c8e1ba81640a1d3ae866c136)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 10 Aug 2021 - 00:53
    - Baseline: 10 Aug 2021 - 01:00
* Package commits:
    - Target: a89ac9
    - Baseline: dd3d4e
* Julia commits:
    - Target: 1b93d5
    - Baseline: 1b93d5
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
| `["findfirst", "0%", "tx"]`                                        |                1.19 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "0%", "tx-noterm"]`                                 |                1.58 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                                       |                1.28 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "10%", "tx-noterm"]`                                |                1.58 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "10%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                                       |                1.29 (5%) :x: | 1.23 (1%) :x: |
| `["findfirst", "20%", "tx-noterm"]`                                |                1.54 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "20%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                                       |                1.44 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                                |                1.62 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "30%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                                       |                1.43 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                                |                1.58 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "40%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                                       |                1.61 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.57 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "50%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq", "base", "Transpose"]`                             | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq", "base", "Vector"]`                                | 0.74 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq", "tx", "Matrix"]`                                  | 0.75 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq", "tx", "Transpose"]`                               | 0.80 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |                1.05 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.06 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.06 (5%) :x: |    1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                                        | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "Base"]`                                 |                1.15 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |                1.10 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |                1.12 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "Base"]`                                   |                1.10 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |                1.07 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |                1.11 (5%) :x: |    1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |                1.06 (5%) :x: |    1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |                1.12 (5%) :x: |    1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |                1.13 (5%) :x: |    1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |                1.09 (5%) :x: |    1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |                1.18 (5%) :x: |    1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |                1.11 (5%) :x: |    1.00 (1%)  |

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
Julia Version 1.6.2
Commit 1b93d53fc4 (2021-07-14 15:36 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1039-azure #42~20.04.1-Ubuntu SMP Thu Jul 15 14:11:07 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       6106 s          2 s        238 s       5502 s          0 s
       #2  2095 MHz       5680 s          1 s        266 s       5904 s          0 s
       
  Memory: 6.790924072265625 GB (2558.30078125 MB free)
  Uptime: 1191.0 sec
  Load Avg:  1.28  1.33  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.6.2
Commit 1b93d53fc4 (2021-07-14 15:36 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1039-azure #42~20.04.1-Ubuntu SMP Thu Jul 15 14:11:07 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       9763 s          2 s        357 s       5907 s          0 s
       #2  2095 MHz       7385 s          1 s        323 s       8315 s          0 s
       
  Memory: 6.790924072265625 GB (2822.23046875 MB free)
  Uptime: 1611.0 sec
  Load Avg:  1.25  1.34  1.07
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 10 Aug 2021 - 0:53
* Package commit: a89ac9
* Julia commit: 1b93d5
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                 | time            | GC time   | memory           | allocations |
|--------------------------------------------------------------------|----------------:|----------:|-----------------:|------------:|
| `["findfirst", "0%", "base"]`                                      |   2.900 ns (5%) |           |                  |             |
| `["findfirst", "0%", "tx"]`                                        |   5.458 μs (5%) |           |    3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 600.436 μs (5%) |           |   17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                    |  92.193 ns (5%) |           |   176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                     | 169.510 μs (5%) |           |                  |             |
| `["findfirst", "10%", "tx"]`                                       | 179.911 μs (5%) |           |   13.28 KiB (1%) |         177 |
| `["findfirst", "10%", "tx-noterm"]`                                | 603.536 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                   |  68.404 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                     | 339.120 μs (5%) |           |                  |             |
| `["findfirst", "20%", "tx"]`                                       | 179.911 μs (5%) |           |   11.86 KiB (1%) |         160 |
| `["findfirst", "20%", "tx-noterm"]`                                | 600.836 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                   | 136.608 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                     | 508.630 μs (5%) |           |                  |             |
| `["findfirst", "30%", "tx"]`                                       | 200.912 μs (5%) |           |    9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                | 610.336 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                   | 204.012 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                     | 678.140 μs (5%) |           |                  |             |
| `["findfirst", "40%", "tx"]`                                       | 275.015 μs (5%) |           |   12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                | 615.037 μs (5%) |           |   17.44 KiB (1%) |         252 |
| `["findfirst", "40%", "tx-seq"]`                                   | 272.116 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                     | 847.751 μs (5%) |           |                  |             |
| `["findfirst", "50%", "tx"]`                                       | 380.823 μs (5%) |           |   16.89 KiB (1%) |         238 |
| `["findfirst", "50%", "tx-noterm"]`                                | 607.336 μs (5%) |           |   17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                   | 340.220 μs (5%) |           |   192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 304.418 ms (5%) | 31.457 ms |  305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 245.280 ms (5%) | 30.236 ms |  305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   8.230 ms (5%) |           |                  |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.817 ms (5%) |           |                  |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   6.525 ms (5%) |           |   19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.471 ms (5%) |           |    9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                | 724.043 μs (5%) |           |                  |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.395 ms (5%) |           |                  |             |
| `["foreach_seq", "base", "Vector"]`                                | 721.343 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 733.544 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.163 ms (5%) |           |                  |             |
| `["foreach_seq", "tx", "Vector"]`                                  | 720.743 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  21.601 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  21.402 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  22.201 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  22.801 μs (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "man"]`                          |  90.914 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  90.943 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  89.869 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  94.228 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.060 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.060 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.678 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.678 μs (5%) |           |                  |             |
| `["mapi", "collatz", "base"]`                                      | 350.971 ms (5%) |           |    7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 297.801 ms (5%) | 19.397 ms |  189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.299 ms (5%) |           |   58.61 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.351 ms (5%) |           |   59.19 KiB (1%) |        1180 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.895 ms (5%) |           |                  |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.026 ms (5%) |           |    1.17 MiB (1%) |         296 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 727.742 μs (5%) |           |  946.94 KiB (1%) |         973 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 828.349 μs (5%) |           |    1.04 MiB (1%) |         992 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.979 ms (5%) |           |                  |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.528 ms (5%) |           |    1.17 MiB (1%) |         319 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.695 ms (5%) |           | 1005.03 KiB (1%) |        1825 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.363 ms (5%) |           |    1.37 MiB (1%) |        1870 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 128.608 μs (5%) |           |   160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 124.907 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 122.707 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 124.507 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                   |   6.654 ms (5%) |           |                  |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.908 ms (5%) |           |    1.17 MiB (1%) |         313 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.300 ms (5%) |           | 1015.12 KiB (1%) |        2007 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.092 ms (5%) |           |    1.38 MiB (1%) |        2041 |
| `["sort", "reversed", "Base"]`                                     | 752.745 μs (5%) |           |                  |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.298 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 907.455 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.398 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["sort", "sorted", "Base"]`                                       | 696.241 μs (5%) |           |                  |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |   1.046 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 871.852 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.186 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   4.859 ms (5%) |           |   832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   2.204 ms (5%) |           |   22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.459 ms (5%) |           |   65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.301 ms (5%) |           |    1.04 MiB (1%) |         619 |

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
Julia Version 1.6.2
Commit 1b93d53fc4 (2021-07-14 15:36 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1039-azure #42~20.04.1-Ubuntu SMP Thu Jul 15 14:11:07 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       6106 s          2 s        238 s       5502 s          0 s
       #2  2095 MHz       5680 s          1 s        266 s       5904 s          0 s
       
  Memory: 6.790924072265625 GB (2558.30078125 MB free)
  Uptime: 1191.0 sec
  Load Avg:  1.28  1.33  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 10 Aug 2021 - 1:0
* Package commit: dd3d4e
* Julia commit: 1b93d5
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                 | time            | GC time   | memory           | allocations |
|--------------------------------------------------------------------|----------------:|----------:|-----------------:|------------:|
| `["findfirst", "0%", "base"]`                                      |   2.900 ns (5%) |           |                  |             |
| `["findfirst", "0%", "tx"]`                                        |   4.572 μs (5%) |           |    3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 380.023 μs (5%) |           |   17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                    |  91.048 ns (5%) |           |   176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                     | 169.510 μs (5%) |           |                  |             |
| `["findfirst", "10%", "tx"]`                                       | 140.009 μs (5%) |           |   13.30 KiB (1%) |         177 |
| `["findfirst", "10%", "tx-noterm"]`                                | 382.023 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                   | 101.906 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                     | 339.120 μs (5%) |           |                  |             |
| `["findfirst", "20%", "tx"]`                                       | 139.109 μs (5%) |           |    9.62 KiB (1%) |         134 |
| `["findfirst", "20%", "tx-noterm"]`                                | 388.923 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                   | 203.712 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                     | 508.730 μs (5%) |           |                  |             |
| `["findfirst", "30%", "tx"]`                                       | 140.008 μs (5%) |           |    9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                | 377.823 μs (5%) |           |   17.44 KiB (1%) |         252 |
| `["findfirst", "30%", "tx-seq"]`                                   | 305.518 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                     | 678.141 μs (5%) |           |                  |             |
| `["findfirst", "40%", "tx"]`                                       | 192.711 μs (5%) |           |   12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                | 388.824 μs (5%) |           |   17.44 KiB (1%) |         252 |
| `["findfirst", "40%", "tx-seq"]`                                   | 407.224 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                     | 847.750 μs (5%) |           |                  |             |
| `["findfirst", "50%", "tx"]`                                       | 237.015 μs (5%) |           |   16.86 KiB (1%) |         237 |
| `["findfirst", "50%", "tx-noterm"]`                                | 386.523 μs (5%) |           |   17.59 KiB (1%) |         260 |
| `["findfirst", "50%", "tx-seq"]`                                   | 508.930 μs (5%) |           |   192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 310.104 ms (5%) | 28.349 ms |  305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 249.096 ms (5%) | 26.969 ms |  305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   8.664 ms (5%) |           |                  |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.861 ms (5%) |           |                  |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   6.580 ms (5%) |           |   19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.442 ms (5%) |           |    9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                | 721.243 μs (5%) |           |                  |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.545 ms (5%) |           |                  |             |
| `["foreach_seq", "base", "Vector"]`                                | 970.158 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 978.058 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.459 ms (5%) |           |                  |             |
| `["foreach_seq", "tx", "Vector"]`                                  | 725.943 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  21.701 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  21.702 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  21.301 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  21.702 μs (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "man"]`                          |  90.914 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.000 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.000 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.600 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.600 μs (5%) |           |                  |             |
| `["mapi", "collatz", "base"]`                                      | 341.171 ms (5%) |           |    7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 325.881 ms (5%) | 22.766 ms |  189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.242 ms (5%) |           |   58.61 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.285 ms (5%) |           |   58.61 KiB (1%) |        1170 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.526 ms (5%) |           |                  |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.762 ms (5%) |           |    1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 726.744 μs (5%) |           |  946.94 KiB (1%) |         973 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 736.744 μs (5%) |           |    1.04 MiB (1%) |         992 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.371 ms (5%) |           |                  |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.190 ms (5%) |           |    1.17 MiB (1%) |         318 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.680 ms (5%) |           | 1005.03 KiB (1%) |        1825 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.936 ms (5%) |           |    1.37 MiB (1%) |        1870 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 128.508 μs (5%) |           |   160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 123.807 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 121.607 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 123.908 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                   |   6.663 ms (5%) |           |                  |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.624 ms (5%) |           |    1.17 MiB (1%) |         312 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.441 ms (5%) |           | 1015.12 KiB (1%) |        2007 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.664 ms (5%) |           |    1.38 MiB (1%) |        2041 |
| `["sort", "reversed", "Base"]`                                     | 748.244 μs (5%) |           |                  |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.153 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 917.655 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.277 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["sort", "sorted", "Base"]`                                       | 695.641 μs (5%) |           |                  |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 889.053 μs (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 898.954 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.066 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   4.859 ms (5%) |           |   832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   2.296 ms (5%) |           |   22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.412 ms (5%) |           |   65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.387 ms (5%) |           |    1.04 MiB (1%) |         619 |

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
Julia Version 1.6.2
Commit 1b93d53fc4 (2021-07-14 15:36 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1039-azure #42~20.04.1-Ubuntu SMP Thu Jul 15 14:11:07 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       9763 s          2 s        357 s       5907 s          0 s
       #2  2095 MHz       7385 s          1 s        323 s       8315 s          0 s
       
  Memory: 6.790924072265625 GB (2822.23046875 MB free)
  Uptime: 1611.0 sec
  Load Avg:  1.25  1.34  1.07
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
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
    CPU MHz:                         2095.176
    BogoMIPS:                        4190.35
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2 MiB
    L3 cache:                        35.8 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
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
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

