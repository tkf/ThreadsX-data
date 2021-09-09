# Benchmark result

* Pull request commit: [`f96c76a3c2b6fbb0e5f19a30619e5e460419ce69`](https://github.com/tkf/ThreadsX.jl/commit/f96c76a3c2b6fbb0e5f19a30619e5e460419ce69)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Sep 2021 - 00:54
    - Baseline: 9 Sep 2021 - 01:01
* Package commits:
    - Target: ab0ce1
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
| `["findfirst", "0%", "base"]`                                      | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx"]`                                        | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                                       | 0.79 (5%) :white_check_mark: |                1.06 (1%) :x: |
| `["findfirst", "20%", "tx"]`                                       |                   1.01 (5%)  | 0.84 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx-noterm"]`                                | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                                       |                   0.96 (5%)  | 0.82 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx-noterm"]`                                | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "base", "A .= B .+ B'"]`                              | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "base", "A .= B .+ C"]`                               | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ C"]`                          | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "tx", "A .= B .+ B'"]`                                | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "tx", "A .= B .+ C"]`                                 | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Transpose"]`                               | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.34 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.33 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                                        | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapi", "consume-100us", "tx"]`                                  |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |                1.10 (5%) :x: |                   1.00 (1%)  |
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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1040-azure #43~20.04.1-Ubuntu SMP Mon Aug 2 22:06:11 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       6955 s          2 s        312 s       2362 s          0 s
       #2  2294 MHz       4812 s          1 s        234 s       4598 s          0 s
       
  Memory: 6.790924072265625 GB (2437.44140625 MB free)
  Uptime: 971.0 sec
  Load Avg:  1.23  1.27  0.9
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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1040-azure #43~20.04.1-Ubuntu SMP Mon Aug 2 22:06:11 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       8985 s          2 s        381 s       4472 s          0 s
       #2  2294 MHz       8179 s          1 s        343 s       5338 s          0 s
       
  Memory: 6.790924072265625 GB (2817.03515625 MB free)
  Uptime: 1393.0 sec
  Load Avg:  1.25  1.33  1.07
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 9 Sep 2021 - 0:54
* Package commit: ab0ce1
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
| `["findfirst", "0%", "base"]`                                      |   2.500 ns (5%) |           |                  |             |
| `["findfirst", "0%", "tx"]`                                        |   4.000 μs (5%) |           |    3.88 KiB (1%) |          47 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 340.002 μs (5%) |           |   17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                    |  83.369 ns (5%) |           |   176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                     |  59.000 μs (5%) |           |                  |             |
| `["findfirst", "10%", "tx"]`                                       | 104.501 μs (5%) |           |   11.70 KiB (1%) |         156 |
| `["findfirst", "10%", "tx-noterm"]`                                | 343.202 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                   |  59.300 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                     | 117.401 μs (5%) |           |                  |             |
| `["findfirst", "20%", "tx"]`                                       | 128.501 μs (5%) |           |    8.05 KiB (1%) |         112 |
| `["findfirst", "20%", "tx-noterm"]`                                | 340.302 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                   | 117.301 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                     | 175.801 μs (5%) |           |                  |             |
| `["findfirst", "30%", "tx"]`                                       | 129.101 μs (5%) |           |    9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                | 344.002 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                   | 176.101 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                     | 234.301 μs (5%) |           |                  |             |
| `["findfirst", "40%", "tx"]`                                       | 165.701 μs (5%) |           |   12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                | 345.702 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                   | 234.401 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                     | 292.802 μs (5%) |           |                  |             |
| `["findfirst", "50%", "tx"]`                                       | 215.901 μs (5%) |           |   13.86 KiB (1%) |         200 |
| `["findfirst", "50%", "tx-noterm"]`                                | 349.802 μs (5%) |           |   17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                   | 292.602 μs (5%) |           |   192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 413.693 ms (5%) | 30.542 ms |  305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 256.522 ms (5%) | 31.342 ms |  305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  15.145 ms (5%) |           |                  |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   9.121 ms (5%) |           |                  |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   9.284 ms (5%) |           |   19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   4.272 ms (5%) |           |    9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                | 559.604 μs (5%) |           |                  |             |
| `["foreach_seq", "base", "Transpose"]`                             |   1.730 ms (5%) |           |                  |             |
| `["foreach_seq", "base", "Vector"]`                                | 559.903 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 563.303 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Transpose"]`                               | 870.505 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Vector"]`                                  | 559.404 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  20.100 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  20.300 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  20.300 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  20.200 μs (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "man"]`                          | 102.447 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 102.028 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 101.911 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 104.269 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   2.140 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   2.133 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.689 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.600 μs (5%) |           |                  |             |
| `["mapi", "collatz", "base"]`                                      | 253.110 ms (5%) |           |    7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 255.086 ms (5%) | 28.228 ms |  189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.388 ms (5%) |           |   58.61 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.420 ms (5%) |           |   58.61 KiB (1%) |        1170 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.045 ms (5%) |           |                  |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.364 ms (5%) |           |    1.17 MiB (1%) |         296 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 943.705 μs (5%) |           |  946.94 KiB (1%) |         973 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 970.105 μs (5%) |           |    1.04 MiB (1%) |         992 |
| `["sort", "F64 (wide)", "Base"]`                                   |   4.966 ms (5%) |           |                  |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.289 ms (5%) |           |    1.17 MiB (1%) |         319 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.375 ms (5%) |           | 1005.03 KiB (1%) |        1825 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.991 ms (5%) |           |    1.37 MiB (1%) |        1870 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 125.001 μs (5%) |           |   160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 128.200 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 128.001 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 128.001 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                   |   4.883 ms (5%) |           |                  |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   3.949 ms (5%) |           |    1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.024 ms (5%) |           | 1015.12 KiB (1%) |        2007 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.472 ms (5%) |           |    1.38 MiB (1%) |        2041 |
| `["sort", "reversed", "Base"]`                                     | 625.503 μs (5%) |           |                  |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.123 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 939.899 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.350 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["sort", "sorted", "Base"]`                                       | 590.206 μs (5%) |           |                  |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 877.905 μs (5%) |           |    1.17 MiB (1%) |         267 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 934.106 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.097 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   4.716 ms (5%) |           |   832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   2.334 ms (5%) |           |   22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.018 ms (5%) |           |   65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.276 ms (5%) |           |    1.04 MiB (1%) |         619 |

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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1040-azure #43~20.04.1-Ubuntu SMP Mon Aug 2 22:06:11 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       6955 s          2 s        312 s       2362 s          0 s
       #2  2294 MHz       4812 s          1 s        234 s       4598 s          0 s
       
  Memory: 6.790924072265625 GB (2437.44140625 MB free)
  Uptime: 971.0 sec
  Load Avg:  1.23  1.27  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 9 Sep 2021 - 1:1
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
| `["findfirst", "0%", "base"]`                                      |   3.000 ns (5%) |           |                  |             |
| `["findfirst", "0%", "tx"]`                                        |   4.400 μs (5%) |           |    3.88 KiB (1%) |          47 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 342.102 μs (5%) |           |   17.27 KiB (1%) |         243 |
| `["findfirst", "0%", "tx-seq"]`                                    |  85.912 ns (5%) |           |   176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                     |  59.101 μs (5%) |           |                  |             |
| `["findfirst", "10%", "tx"]`                                       | 131.901 μs (5%) |           |   11.06 KiB (1%) |         149 |
| `["findfirst", "10%", "tx-noterm"]`                                | 357.202 μs (5%) |           |   17.44 KiB (1%) |         252 |
| `["findfirst", "10%", "tx-seq"]`                                   |  59.400 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                     | 117.801 μs (5%) |           |                  |             |
| `["findfirst", "20%", "tx"]`                                       | 126.902 μs (5%) |           |    9.62 KiB (1%) |         134 |
| `["findfirst", "20%", "tx-noterm"]`                                | 356.902 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                   | 117.701 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                     | 175.801 μs (5%) |           |                  |             |
| `["findfirst", "30%", "tx"]`                                       | 127.101 μs (5%) |           |    9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                | 338.900 μs (5%) |           |   17.44 KiB (1%) |         252 |
| `["findfirst", "30%", "tx-seq"]`                                   | 176.101 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                     | 234.601 μs (5%) |           |                  |             |
| `["findfirst", "40%", "tx"]`                                       | 169.900 μs (5%) |           |   12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                | 367.800 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                   | 234.601 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                     | 292.702 μs (5%) |           |                  |             |
| `["findfirst", "50%", "tx"]`                                       | 225.601 μs (5%) |           |   16.86 KiB (1%) |         237 |
| `["findfirst", "50%", "tx-noterm"]`                                | 368.702 μs (5%) |           |   17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                   | 292.902 μs (5%) |           |   192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 437.549 ms (5%) | 45.998 ms |  305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 282.993 ms (5%) | 35.527 ms |  305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  16.406 ms (5%) |           |                  |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   9.790 ms (5%) |           |                  |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |  10.124 ms (5%) |           |   19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   4.607 ms (5%) |           |    9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                | 559.703 μs (5%) |           |                  |             |
| `["foreach_seq", "base", "Transpose"]`                             |   1.731 ms (5%) |           |                  |             |
| `["foreach_seq", "base", "Vector"]`                                | 560.103 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 563.503 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Transpose"]`                               | 918.804 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Vector"]`                                  | 560.202 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  19.801 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  21.901 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  20.200 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  20.800 μs (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "man"]`                          | 104.576 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.600 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.600 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.500 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.500 μs (5%) |           |                  |             |
| `["mapi", "collatz", "base"]`                                      | 259.666 ms (5%) |           |    7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 277.478 ms (5%) | 30.870 ms |  189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.272 ms (5%) |           |   58.61 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.348 ms (5%) |           |   58.61 KiB (1%) |        1170 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.043 ms (5%) |           |                  |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.289 ms (5%) |           |    1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 951.105 μs (5%) |           |  946.94 KiB (1%) |         973 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 965.506 μs (5%) |           |    1.04 MiB (1%) |         992 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.012 ms (5%) |           |                  |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.205 ms (5%) |           |    1.17 MiB (1%) |         318 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.522 ms (5%) |           | 1005.03 KiB (1%) |        1825 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.272 ms (5%) |           |    1.37 MiB (1%) |        1870 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 125.701 μs (5%) |           |   160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 128.701 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 128.701 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 128.501 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                   |   4.914 ms (5%) |           |                  |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   3.949 ms (5%) |           |    1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   2.901 ms (5%) |           | 1015.12 KiB (1%) |        2007 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.502 ms (5%) |           |    1.38 MiB (1%) |        2041 |
| `["sort", "reversed", "Base"]`                                     | 625.404 μs (5%) |           |                  |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.121 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 930.906 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.301 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["sort", "sorted", "Base"]`                                       | 590.004 μs (5%) |           |                  |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 895.905 μs (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 927.106 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.103 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   4.518 ms (5%) |           |   832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   2.157 ms (5%) |           |   22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   6.380 ms (5%) |           |   65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   3.939 ms (5%) |           |    1.04 MiB (1%) |         619 |

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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1040-azure #43~20.04.1-Ubuntu SMP Mon Aug 2 22:06:11 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       8985 s          2 s        381 s       4472 s          0 s
       #2  2294 MHz       8179 s          1 s        343 s       5338 s          0 s
       
  Memory: 6.790924072265625 GB (2817.03515625 MB free)
  Uptime: 1393.0 sec
  Load Avg:  1.25  1.33  1.07
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
    CPU MHz:                         2294.683
    BogoMIPS:                        4589.36
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

