# Benchmark result

* Pull request commit: [`13f632a1bc2880a07fd39fb144787181ab4c0ae6`](https://github.com/tkf/ThreadsX.jl/commit/13f632a1bc2880a07fd39fb144787181ab4c0ae6)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 May 2023 - 01:08
    - Baseline: 6 May 2023 - 01:14
* Package commits:
    - Target: b7f778
    - Baseline: d40e1b
* Julia commits:
    - Target: 3b76b2
    - Baseline: 3b76b2
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

| ID                                                     | time ratio                   | memory ratio                 |
|--------------------------------------------------------|------------------------------|------------------------------|
| `["findfirst", "0%", "tx"]`                            | 0.77 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx-noterm"]`                     | 0.68 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "base"]`                         |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                           | 0.49 (5%) :white_check_mark: | 0.77 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx-noterm"]`                    | 0.68 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "20%", "base"]`                         | 0.69 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                           | 0.67 (5%) :white_check_mark: |                1.19 (1%) :x: |
| `["findfirst", "20%", "tx-noterm"]`                    | 0.68 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "base"]`                         | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                           | 0.71 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                    | 0.68 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "base"]`                         |                1.49 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                           | 0.69 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                    | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "base"]`                         | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                           | 0.70 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx-noterm"]`                    | 0.69 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                            | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |

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
- `["foreach_seq_double", "linear"]`
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
Julia Version 1.6.7
Commit 3b76b25b64 (2022-07-19 15:11 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5407 s          0 s        303 s       4124 s          0 s
       #2  2793 MHz       5903 s          0 s        283 s       3625 s          0 s
       
  Memory: 6.781208038330078 GB (2702.42578125 MB free)
  Uptime: 990.3 sec
  Load Avg:  1.19  1.26  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, icelake-server)
```

### Baseline
```
Julia Version 1.6.7
Commit 3b76b25b64 (2022-07-19 15:11 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7258 s          0 s        348 s       6115 s          0 s
       #2  2793 MHz       9178 s          0 s        392 s       4132 s          0 s
       
  Memory: 6.781208038330078 GB (3030.12109375 MB free)
  Uptime: 1380.46 sec
  Load Avg:  1.27  1.34  1.07
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 6 May 2023 - 1:8
* Package commit: b7f778
* Julia commit: 3b76b2
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                   | time            | GC time   | memory          | allocations |
|----------------------------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["findfirst", "0%", "base"]`                                        |   2.600 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   4.467 μs (5%) |           |   3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 454.400 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  91.755 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       | 126.100 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 106.900 μs (5%) |           |  10.28 KiB (1%) |         139 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 454.503 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     |  84.200 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 173.600 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 154.600 μs (5%) |           |  14.11 KiB (1%) |         187 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 453.900 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 168.700 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 253.700 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 166.099 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 452.497 μs (5%) |           |  17.44 KiB (1%) |         252 |
| `["findfirst", "30%", "tx-seq"]`                                     | 252.900 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 504.598 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 205.000 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 449.702 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 336.901 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 421.800 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 285.100 μs (5%) |           |  16.86 KiB (1%) |         237 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 459.700 μs (5%) |           |  17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                     | 421.000 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 267.322 ms (5%) | 37.301 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 243.358 ms (5%) | 36.988 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |   7.267 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   5.733 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   3.663 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   2.974 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  | 691.701 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   1.787 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 803.801 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 718.200 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 | 981.401 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 691.901 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  20.700 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  20.400 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  20.500 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  20.700 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            |  80.352 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         |  79.855 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          |  79.959 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           |  79.855 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    |   1.130 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` |   1.140 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   3.200 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   3.212 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 334.903 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 268.728 ms (5%) | 19.027 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.201 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.230 ms (5%) |           |  58.72 KiB (1%) |        1173 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   3.011 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   3.186 ms (5%) |           |   1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 688.201 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 769.801 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   7.905 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   6.512 ms (5%) |           |   1.17 MiB (1%) |         319 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   3.893 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.720 ms (5%) |           |   1.35 MiB (1%) |        1582 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 139.400 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 132.200 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 132.900 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 132.400 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   7.743 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   5.349 ms (5%) |           |   1.17 MiB (1%) |         312 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   3.686 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.296 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 838.001 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.145 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         | 827.701 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.248 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 823.001 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           | 875.701 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           | 817.901 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     | 981.902 μs (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   4.848 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   2.357 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   7.862 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   4.543 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
- `["foreach_seq_sum_many", :(:nvecs => 8)]`
- `["foreach_seq_sum_many", :(:nvecs => 8), "tx"]`
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
Julia Version 1.6.7
Commit 3b76b25b64 (2022-07-19 15:11 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5407 s          0 s        303 s       4124 s          0 s
       #2  2793 MHz       5903 s          0 s        283 s       3625 s          0 s
       
  Memory: 6.781208038330078 GB (2702.42578125 MB free)
  Uptime: 990.3 sec
  Load Avg:  1.19  1.26  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 6 May 2023 - 1:14
* Package commit: d40e1b
* Julia commit: 3b76b2
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                   | time            | GC time   | memory          | allocations |
|----------------------------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["findfirst", "0%", "base"]`                                        |   2.600 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   5.800 μs (5%) |           |   3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 670.601 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  88.831 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       |  84.100 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 217.800 μs (5%) |           |  13.28 KiB (1%) |         177 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 669.501 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     |  84.200 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 252.300 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 232.400 μs (5%) |           |  11.89 KiB (1%) |         162 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 670.301 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 168.900 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 378.400 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 232.400 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 664.700 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 252.900 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 337.700 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 298.500 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 666.801 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 337.000 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 630.700 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 405.100 μs (5%) |           |  16.86 KiB (1%) |         237 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 662.600 μs (5%) |           |  17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                     | 421.100 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 272.964 ms (5%) | 34.829 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 245.981 ms (5%) | 34.214 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |   7.104 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   5.626 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   3.654 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   2.908 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  | 691.700 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   1.808 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 803.401 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 718.400 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 | 984.100 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 691.800 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  20.800 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  20.600 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  20.800 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  20.800 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            |  80.248 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    |   1.100 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` |   1.100 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   3.200 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   3.200 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 336.771 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 286.067 ms (5%) | 21.948 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.196 ms (5%) |           |  58.72 KiB (1%) |        1173 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.242 ms (5%) |           |  59.16 KiB (1%) |        1177 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   2.983 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   3.146 ms (5%) |           |   1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 674.101 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 764.900 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   7.913 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   6.475 ms (5%) |           |   1.17 MiB (1%) |         319 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   3.853 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.708 ms (5%) |           |   1.35 MiB (1%) |        1583 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 140.201 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 132.400 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 132.200 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 131.900 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   7.776 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   5.312 ms (5%) |           |   1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   3.590 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.256 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 839.200 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.162 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         | 837.401 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.263 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 820.300 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           | 862.800 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           | 818.701 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     | 974.501 μs (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   4.872 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   2.311 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   7.848 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   4.566 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
- `["foreach_seq_sum_many", :(:nvecs => 8)]`
- `["foreach_seq_sum_many", :(:nvecs => 8), "tx"]`
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
Julia Version 1.6.7
Commit 3b76b25b64 (2022-07-19 15:11 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7258 s          0 s        348 s       6115 s          0 s
       #2  2793 MHz       9178 s          0 s        392 s       4132 s          0 s
       
  Memory: 6.781208038330078 GB (3030.12109375 MB free)
  Uptime: 1380.46 sec
  Load Avg:  1.27  1.34  1.07
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, icelake-server)
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
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz
    CPU family:                      6
    Model:                           106
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        6
    BogoMIPS:                        5586.87
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       96 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2.5 MiB (2 instances)
    L3 cache:                        48 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Not affected
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :UnknownIntel                                           |
| Model              | Family: 0x06, Model: 0x6a, Stepping: 0x06, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (48, 1280, 49152) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

