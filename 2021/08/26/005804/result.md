# Benchmark result

* Pull request commit: [`5c2fe0093befa33799736a83ffa1bcbfb0ae9b00`](https://github.com/tkf/ThreadsX.jl/commit/5c2fe0093befa33799736a83ffa1bcbfb0ae9b00)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 26 Aug 2021 - 00:50
    - Baseline: 26 Aug 2021 - 00:57
* Package commits:
    - Target: 2ddaad
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

| ID                                                                 | time ratio                   | memory ratio                 |
|--------------------------------------------------------------------|------------------------------|------------------------------|
| `["findfirst", "0%", "base"]`                                      | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx"]`                                        |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx-seq"]`                                    | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                                       |                1.27 (5%) :x: | 0.81 (1%) :white_check_mark: |
| `["findfirst", "20%", "base"]`                                     |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                                       |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx-noterm"]`                                |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "30%", "base"]`                                     | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                                       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-seq"]`                                   | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "base"]`                                     | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                                       |                   1.02 (5%)  |                1.23 (1%) :x: |
| `["findfirst", "50%", "tx-noterm"]`                                | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "tx", "A .= B .+ C"]`                                 |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Transpose"]`                               |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "man"]`                          | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.46 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.31 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "consume-100us", "tx"]`                                  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "Base"]`                                   | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sort", "reversed", "Base"]`                                     | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       4628 s          2 s        243 s       5322 s          0 s
       #2  2294 MHz       7621 s          1 s        316 s       2289 s          0 s
       
  Memory: 6.790924072265625 GB (2567.5390625 MB free)
  Uptime: 1030.0 sec
  Load Avg:  1.17  1.25  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.6.2
Commit 1b93d53fc4 (2021-07-14 15:36 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1039-azure #42~20.04.1-Ubuntu SMP Thu Jul 15 14:11:07 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       6653 s          2 s        317 s       7607 s          0 s
       #2  2294 MHz      11229 s          1 s        429 s       2961 s          0 s
       
  Memory: 6.790924072265625 GB (2690.40234375 MB free)
  Uptime: 1470.0 sec
  Load Avg:  1.27  1.4  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 26 Aug 2021 - 0:50
* Package commit: 2ddaad
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
| `["findfirst", "0%", "base"]`                                      |   3.300 ns (5%) |           |                  |             |
| `["findfirst", "0%", "tx"]`                                        |   5.483 μs (5%) |           |    3.90 KiB (1%) |          47 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 412.203 μs (5%) |           |   17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                    |  95.159 ns (5%) |           |   176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                     |  69.100 μs (5%) |           |                  |             |
| `["findfirst", "10%", "tx"]`                                       | 150.501 μs (5%) |           |    9.47 KiB (1%) |         127 |
| `["findfirst", "10%", "tx-noterm"]`                                | 417.503 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                   |  68.700 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                     | 141.201 μs (5%) |           |                  |             |
| `["findfirst", "20%", "tx"]`                                       | 150.501 μs (5%) |           |    9.58 KiB (1%) |         132 |
| `["findfirst", "20%", "tx-noterm"]`                                | 421.903 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                   | 136.700 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                     | 198.401 μs (5%) |           |                  |             |
| `["findfirst", "30%", "tx"]`                                       | 155.801 μs (5%) |           |    9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                | 414.703 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                   | 198.301 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                     | 272.602 μs (5%) |           |                  |             |
| `["findfirst", "40%", "tx"]`                                       | 199.201 μs (5%) |           |   12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                | 409.703 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                   | 264.202 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                     | 310.402 μs (5%) |           |                  |             |
| `["findfirst", "50%", "tx"]`                                       | 281.101 μs (5%) |           |   16.09 KiB (1%) |         227 |
| `["findfirst", "50%", "tx-noterm"]`                                | 410.604 μs (5%) |           |   17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                   | 340.103 μs (5%) |           |   192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 462.044 ms (5%) | 35.007 ms |  305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 303.178 ms (5%) | 36.497 ms |  305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  20.190 ms (5%) |           |                  |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |  10.396 ms (5%) |           |                  |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |  12.083 ms (5%) |           |   19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   5.026 ms (5%) |           |    9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                | 651.105 μs (5%) |           |                  |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.117 ms (5%) |           |                  |             |
| `["foreach_seq", "base", "Vector"]`                                | 630.404 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 628.504 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.022 ms (5%) |           |                  |             |
| `["foreach_seq", "tx", "Vector"]`                                  | 630.304 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  24.500 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  23.100 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  23.900 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  23.700 μs (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "man"]`                          | 101.866 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 103.869 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 103.960 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 104.840 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   2.489 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   2.489 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   3.138 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   3.125 μs (5%) |           |                  |             |
| `["mapi", "collatz", "base"]`                                      | 317.090 ms (5%) |           |    7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 293.134 ms (5%) | 21.193 ms |  189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.469 ms (5%) |           |   58.61 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.571 ms (5%) |           |   58.61 KiB (1%) |        1170 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.510 ms (5%) |           |                  |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.044 ms (5%) |           |    1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   |   1.101 ms (5%) |           |  946.94 KiB (1%) |         973 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |   1.196 ms (5%) |           |    1.04 MiB (1%) |         992 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.298 ms (5%) |           |                  |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.582 ms (5%) |           |    1.17 MiB (1%) |         317 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.349 ms (5%) |           | 1005.03 KiB (1%) |        1825 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.990 ms (5%) |           |    1.37 MiB (1%) |        1870 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 141.801 μs (5%) |           |   160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 143.101 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 140.701 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 146.201 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.848 ms (5%) |           |                  |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.946 ms (5%) |           |    1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.771 ms (5%) |           | 1015.12 KiB (1%) |        2007 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.653 ms (5%) |           |    1.38 MiB (1%) |        2041 |
| `["sort", "reversed", "Base"]`                                     | 687.205 μs (5%) |           |                  |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.456 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.160 ms (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.639 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["sort", "sorted", "Base"]`                                       | 700.105 μs (5%) |           |                  |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |   1.075 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |   1.154 ms (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.388 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   5.584 ms (5%) |           |   832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   2.700 ms (5%) |           |   22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.125 ms (5%) |           |   65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.045 ms (5%) |           |    1.04 MiB (1%) |         619 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       4628 s          2 s        243 s       5322 s          0 s
       #2  2294 MHz       7621 s          1 s        316 s       2289 s          0 s
       
  Memory: 6.790924072265625 GB (2567.5390625 MB free)
  Uptime: 1030.0 sec
  Load Avg:  1.17  1.25  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 26 Aug 2021 - 0:57
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
| `["findfirst", "0%", "base"]`                                      |   3.500 ns (5%) |           |                  |             |
| `["findfirst", "0%", "tx"]`                                        |   5.033 μs (5%) |           |    3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 403.600 μs (5%) |           |   17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                    | 103.158 ns (5%) |           |   176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                     |  69.201 μs (5%) |           |                  |             |
| `["findfirst", "10%", "tx"]`                                       | 118.301 μs (5%) |           |   11.69 KiB (1%) |         154 |
| `["findfirst", "10%", "tx-noterm"]`                                | 418.804 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                   |  69.001 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                     | 128.801 μs (5%) |           |                  |             |
| `["findfirst", "20%", "tx"]`                                       | 141.801 μs (5%) |           |    9.58 KiB (1%) |         132 |
| `["findfirst", "20%", "tx-noterm"]`                                | 384.403 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                   | 132.501 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                     | 211.600 μs (5%) |           |                  |             |
| `["findfirst", "30%", "tx"]`                                       | 150.000 μs (5%) |           |    9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                | 419.400 μs (5%) |           |   17.44 KiB (1%) |         252 |
| `["findfirst", "30%", "tx-seq"]`                                   | 205.000 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                     | 264.103 μs (5%) |           |                  |             |
| `["findfirst", "40%", "tx"]`                                       | 210.609 μs (5%) |           |   12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                | 413.106 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                   | 279.703 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                     | 329.700 μs (5%) |           |                  |             |
| `["findfirst", "50%", "tx"]`                                       | 275.603 μs (5%) |           |   13.12 KiB (1%) |         191 |
| `["findfirst", "50%", "tx-noterm"]`                                | 458.404 μs (5%) |           |   17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                   | 340.100 μs (5%) |           |   192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 467.677 ms (5%) | 34.321 ms |  305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 311.030 ms (5%) | 34.739 ms |  305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  19.797 ms (5%) |           |                  |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |  10.010 ms (5%) |           |                  |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |  12.207 ms (5%) |           |   19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   4.625 ms (5%) |           |    9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                | 630.904 μs (5%) |           |                  |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.053 ms (5%) |           |                  |             |
| `["foreach_seq", "base", "Vector"]`                                | 629.904 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 654.305 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Transpose"]`                               | 967.407 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Vector"]`                                  | 660.505 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  23.800 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  24.100 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  27.500 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  23.100 μs (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "man"]`                          | 117.124 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.700 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.900 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.900 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   3.000 μs (5%) |           |                  |             |
| `["mapi", "collatz", "base"]`                                      | 313.403 ms (5%) |           |    7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 307.601 ms (5%) | 32.915 ms |  189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.371 ms (5%) |           |   58.61 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.441 ms (5%) |           |   58.61 KiB (1%) |        1170 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.476 ms (5%) |           |                  |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.970 ms (5%) |           |    1.17 MiB (1%) |         296 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   |   1.209 ms (5%) |           |  946.94 KiB (1%) |         973 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |   1.212 ms (5%) |           |    1.04 MiB (1%) |         992 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.407 ms (5%) |           |                  |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.331 ms (5%) |           |    1.17 MiB (1%) |         319 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.265 ms (5%) |           | 1005.03 KiB (1%) |        1825 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.145 ms (5%) |           |    1.37 MiB (1%) |        1870 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 142.801 μs (5%) |           |   160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 142.201 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 145.301 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 141.901 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                   |   6.533 ms (5%) |           |                  |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.913 ms (5%) |           |    1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.749 ms (5%) |           | 1015.12 KiB (1%) |        2007 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.366 ms (5%) |           |    1.38 MiB (1%) |        2041 |
| `["sort", "reversed", "Base"]`                                     | 770.005 μs (5%) |           |                  |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.341 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.196 ms (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.605 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["sort", "sorted", "Base"]`                                       | 690.005 μs (5%) |           |                  |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |   1.048 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |   1.173 ms (5%) |           |  985.50 KiB (1%) |        1659 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.357 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   5.697 ms (5%) |           |   832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   2.852 ms (5%) |           |   22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.318 ms (5%) |           |   65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.190 ms (5%) |           |    1.04 MiB (1%) |         619 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       6653 s          2 s        317 s       7607 s          0 s
       #2  2294 MHz      11229 s          1 s        429 s       2961 s          0 s
       
  Memory: 6.790924072265625 GB (2690.40234375 MB free)
  Uptime: 1470.0 sec
  Load Avg:  1.27  1.4  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, broadwell)
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
    Model:                           79
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:                        1
    CPU MHz:                         2294.687
    BogoMIPS:                        4589.37
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
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
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

