# Benchmark result

* Pull request commit: [`954b1b72e80caa6b510b06b6d78f1e14b3b5d565`](https://github.com/tkf/ThreadsX.jl/commit/954b1b72e80caa6b510b06b6d78f1e14b3b5d565)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 16 Feb 2021 - 00:41
    - Baseline: 16 Feb 2021 - 00:48
* Package commits:
    - Target: b51231
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
| `["findfirst", "0%", "tx"]`                                        |                   1.02 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "0%", "tx-noterm"]`                                 |               16.14 (5%) :x: |                2.06 (1%) :x: |
| `["findfirst", "0%", "tx-seq"]`                                    | 0.73 (5%) :white_check_mark: | 0.71 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx"]`                                       |                2.59 (5%) :x: |                2.26 (1%) :x: |
| `["findfirst", "10%", "tx-noterm"]`                                |                1.91 (5%) :x: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "20%", "tx"]`                                       |                1.38 (5%) :x: |                1.31 (1%) :x: |
| `["findfirst", "20%", "tx-noterm"]`                                |                2.00 (5%) :x: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "20%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "30%", "tx"]`                                       |                1.20 (5%) :x: | 0.99 (1%) :white_check_mark: |
| `["findfirst", "30%", "tx-noterm"]`                                |                1.93 (5%) :x: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "30%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx"]`                                       |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx-noterm"]`                                |                1.53 (5%) :x: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx"]`                                       |                   1.05 (5%)  |                1.23 (1%) :x: |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.24 (5%) :x: | 0.62 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["foreach", "base", "A .= B .+ C"]`                               | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.36 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.37 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                                        |                   0.95 (5%)  | 0.96 (1%) :white_check_mark: |
| `["sort", "F64 (narrow)", "Base"]`                                 |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   |                   0.99 (5%)  | 0.59 (1%) :white_check_mark: |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   |                   0.99 (5%)  | 0.59 (1%) :white_check_mark: |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             |                   1.00 (5%)  | 0.59 (1%) :white_check_mark: |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |                   0.99 (5%)  | 0.55 (1%) :white_check_mark: |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      60367 s         17 s       3398 s      39427 s          0 s
       #2  2397 MHz      70710 s          9 s       2608 s      29585 s          0 s
       
  Memory: 6.791374206542969 GB (2461.51171875 MB free)
  Uptime: 1044.0 sec
  Load Avg:  1.24853515625  1.322265625  0.966796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1039-azure #41-Ubuntu SMP Mon Jan 18 13:22:11 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      96555 s         17 s       4648 s      46047 s          0 s
       #2  2397 MHz      91320 s          9 s       3256 s      52372 s          0 s
       
  Memory: 6.791374206542969 GB (2860.66796875 MB free)
  Uptime: 1486.0 sec
  Load Avg:  1.25390625  1.3154296875  1.095703125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 16 Feb 2021 - 0:41
* Package commit: b51231
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
| `["findfirst", "0%", "base"]`                                      |   3.200 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  24.402 μs (5%) |           |  11.77 KiB (1%) |         218 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 382.417 μs (5%) |           |  24.70 KiB (1%) |         245 |
| `["findfirst", "0%", "tx-seq"]`                                    | 172.632 ns (5%) |           |  400 bytes (1%) |          13 |
| `["findfirst", "10%", "base"]`                                     |  68.303 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       | 193.009 μs (5%) |           |  32.63 KiB (1%) |         609 |
| `["findfirst", "10%", "tx-noterm"]`                                | 386.918 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "10%", "tx-seq"]`                                   |  68.503 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "20%", "base"]`                                     | 136.006 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 194.209 μs (5%) |           |  28.03 KiB (1%) |         524 |
| `["findfirst", "20%", "tx-noterm"]`                                | 388.117 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "20%", "tx-seq"]`                                   | 136.206 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "30%", "base"]`                                     | 204.009 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 223.810 μs (5%) |           |  28.05 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 393.218 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "30%", "tx-seq"]`                                   | 204.009 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "40%", "base"]`                                     | 271.312 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 257.212 μs (5%) |           |  34.98 KiB (1%) |         652 |
| `["findfirst", "40%", "tx-noterm"]`                                | 392.318 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "40%", "tx-seq"]`                                   | 272.112 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "50%", "base"]`                                     | 339.415 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 313.114 μs (5%) |           |  46.63 KiB (1%) |         874 |
| `["findfirst", "50%", "tx-noterm"]`                                | 400.118 μs (5%) |           |  24.91 KiB (1%) |         258 |
| `["findfirst", "50%", "tx-seq"]`                                   | 341.015 μs (5%) |           |  416 bytes (1%) |          14 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 456.509 ms (5%) | 39.471 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 251.960 ms (5%) | 40.115 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  66.232 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   8.335 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |  33.362 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   6.933 ms (5%) |           |  12.75 KiB (1%) |         124 |
| `["foreach_seq", "base", "Matrix"]`                                | 650.929 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   3.274 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 650.730 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 655.828 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   2.081 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 650.827 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  23.001 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  23.101 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  22.901 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  23.201 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  97.035 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  97.144 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 100.534 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  97.144 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   2.044 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   2.050 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.978 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.978 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 276.778 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 189.402 ms (5%) |  5.728 ms | 161.07 MiB (1%) |     2016659 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.242 ms (5%) |           |  58.50 KiB (1%) |        1103 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.371 ms (5%) |           |  58.91 KiB (1%) |        1113 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.409 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.624 ms (5%) |           |   1.19 MiB (1%) |         533 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   |   1.563 ms (5%) |           | 965.09 KiB (1%) |        1225 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |   1.568 ms (5%) |           |   1.02 MiB (1%) |        1245 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.684 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.901 ms (5%) |           |   1.19 MiB (1%) |         563 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.808 ms (5%) |           |   1.01 MiB (1%) |        2145 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.637 ms (5%) |           |   1.39 MiB (1%) |        2194 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 145.306 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 147.207 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 146.907 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 146.907 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.712 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.103 ms (5%) |           |   1.19 MiB (1%) |         548 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   4.045 ms (5%) |           |   1.01 MiB (1%) |        2231 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.697 ms (5%) |           |   1.39 MiB (1%) |        2266 |
| `["sort", "reversed", "Base"]`                                     | 764.035 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.194 ms (5%) |           |   1.18 MiB (1%) |         430 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.158 ms (5%) |           | 998.44 KiB (1%) |        1868 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.573 ms (5%) |           |   1.36 MiB (1%) |        1897 |
| `["sort", "sorted", "Base"]`                                       | 714.133 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 888.841 μs (5%) |           |   1.18 MiB (1%) |         426 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |   1.152 ms (5%) |           | 998.36 KiB (1%) |        1863 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.299 ms (5%) |           |   1.36 MiB (1%) |        1899 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   9.122 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.835 ms (5%) |           |  27.81 KiB (1%) |         352 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.522 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.156 ms (5%) |           |   1.04 MiB (1%) |         656 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      60367 s         17 s       3398 s      39427 s          0 s
       #2  2397 MHz      70710 s          9 s       2608 s      29585 s          0 s
       
  Memory: 6.791374206542969 GB (2461.51171875 MB free)
  Uptime: 1044.0 sec
  Load Avg:  1.24853515625  1.322265625  0.966796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 16 Feb 2021 - 0:48
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
| `["findfirst", "0%", "base"]`                                      |   3.200 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  24.001 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  23.701 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 237.260 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  68.304 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  74.503 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 202.409 μs (5%) |           |  33.05 KiB (1%) |         615 |
| `["findfirst", "10%", "tx-seq"]`                                   |  68.603 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 135.807 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 140.606 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 193.809 μs (5%) |           |  26.06 KiB (1%) |         486 |
| `["findfirst", "20%", "tx-seq"]`                                   | 136.306 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 204.009 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 186.108 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 203.410 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 204.109 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 271.612 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 266.112 μs (5%) |           |  35.39 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-noterm"]`                                | 255.911 μs (5%) |           |  35.41 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-seq"]`                                   | 271.912 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 339.415 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 298.213 μs (5%) |           |  37.84 KiB (1%) |         707 |
| `["findfirst", "50%", "tx-noterm"]`                                | 321.815 μs (5%) |           |  40.25 KiB (1%) |         756 |
| `["findfirst", "50%", "tx-seq"]`                                   | 341.315 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 457.405 ms (5%) | 37.205 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 265.459 ms (5%) | 56.286 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  66.558 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   8.073 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |  33.755 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   6.833 ms (5%) |           |  12.77 KiB (1%) |         125 |
| `["foreach_seq", "base", "Matrix"]`                                | 650.929 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   3.328 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 650.429 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 656.729 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   2.139 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 650.829 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  23.101 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  23.101 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  22.401 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  23.101 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  96.929 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.500 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.500 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.900 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.900 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 276.153 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 198.434 ms (5%) | 10.212 ms | 167.37 MiB (1%) |     2016640 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.209 ms (5%) |           |  58.88 KiB (1%) |        1111 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.344 ms (5%) |           |  58.39 KiB (1%) |        1101 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.265 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.633 ms (5%) |           |   1.19 MiB (1%) |         534 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   |   1.566 ms (5%) |           | 965.09 KiB (1%) |        1225 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |   1.570 ms (5%) |           |   1.02 MiB (1%) |        1245 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.632 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.911 ms (5%) |           |   1.19 MiB (1%) |         563 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.889 ms (5%) |           |   1.01 MiB (1%) |        2146 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   6.175 ms (5%) |           |   1.39 MiB (1%) |        2194 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 145.306 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 149.107 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 149.107 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 147.607 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.706 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.202 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   4.002 ms (5%) |           |   1.01 MiB (1%) |        2236 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.758 ms (5%) |           |   1.40 MiB (1%) |        2270 |
| `["sort", "reversed", "Base"]`                                     | 763.835 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.182 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.130 ms (5%) |           | 998.77 KiB (1%) |        1872 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.565 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["sort", "sorted", "Base"]`                                       | 713.932 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 886.641 μs (5%) |           |   1.18 MiB (1%) |         429 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |   1.163 ms (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.281 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   9.438 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.867 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.717 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.227 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      96555 s         17 s       4648 s      46047 s          0 s
       #2  2397 MHz      91320 s          9 s       3256 s      52372 s          0 s
       
  Memory: 6.791374206542969 GB (2860.66796875 MB free)
  Uptime: 1486.0 sec
  Load Avg:  1.25390625  1.3154296875  1.095703125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, haswell)
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
    Model:                           63
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    Stepping:                        2
    CPU MHz:                         2397.221
    BogoMIPS:                        4794.44
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        30 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Vulnerable
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Not affected
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

