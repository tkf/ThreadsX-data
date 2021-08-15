# Benchmark result

* Pull request commit: [`900b56e11cd984f0573b9187710141121c64d4f0`](https://github.com/tkf/ThreadsX.jl/commit/900b56e11cd984f0573b9187710141121c64d4f0)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 15 Aug 2021 - 00:51
    - Baseline: 15 Aug 2021 - 00:58
* Package commits:
    - Target: 479be2
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
| `["findfirst", "0%", "base"]`                                      | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "0%", "tx"]`                                        |                1.10 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "0%", "tx-noterm"]`                                 |                1.43 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                                       |                1.56 (5%) :x: | 1.13 (1%) :x: |
| `["findfirst", "10%", "tx-noterm"]`                                |                1.50 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                                       |                1.53 (5%) :x: | 1.23 (1%) :x: |
| `["findfirst", "20%", "tx-noterm"]`                                |                1.49 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                                       |                1.47 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                                |                1.45 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                                       |                1.40 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                                |                1.43 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                                       |                1.38 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.45 (5%) :x: |    1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ C"]`                          | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach", "tx", "A .= B .+ B'"]`                                | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach", "tx", "A .= B .+ C"]`                                 | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq", "base", "Transpose"]`                             | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq", "base", "Vector"]`                                | 0.75 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq", "tx", "Matrix"]`                                  | 0.75 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq", "tx", "Transpose"]`                               | 0.79 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |                1.05 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.10 (5%) :x: |    1.00 (1%)  |
| `["mapi", "collatz", "base"]`                                      | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                                        | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["mapi", "consume-100us", "tx"]`                                  |                1.06 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "Base"]`                                 |                1.15 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |                1.14 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |                1.06 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "Base"]`                                   |                1.10 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |                1.09 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |                1.13 (5%) :x: |    1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   |                1.06 (5%) :x: |    1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   |                1.06 (5%) :x: |    1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |                1.06 (5%) :x: |    1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |                1.15 (5%) :x: |    1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |                1.11 (5%) :x: |    1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |                1.10 (5%) :x: |    1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |                1.16 (5%) :x: |    1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |                1.08 (5%) :x: |    1.00 (1%)  |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7410 s          2 s        262 s       1842 s          0 s
       #2  2593 MHz       4409 s          0 s        220 s       4896 s          0 s
       
  Memory: 6.790924072265625 GB (2566.4453125 MB free)
  Uptime: 957.0 sec
  Load Avg:  1.19  1.23  0.88
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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      11221 s          2 s        378 s       2084 s          0 s
       #2  2593 MHz       5909 s          0 s        275 s       7502 s          0 s
       
  Memory: 6.790924072265625 GB (2673.40234375 MB free)
  Uptime: 1375.0 sec
  Load Avg:  1.29  1.37  1.09
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 15 Aug 2021 - 0:51
* Package commit: 479be2
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
| `["findfirst", "0%", "base"]`                                      |   2.700 ns (5%) |           |                  |             |
| `["findfirst", "0%", "tx"]`                                        |   5.867 μs (5%) |           |    3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 558.203 μs (5%) |           |   17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                    |  99.896 ns (5%) |           |   176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                     | 175.201 μs (5%) |           |                  |             |
| `["findfirst", "10%", "tx"]`                                       | 160.801 μs (5%) |           |   13.22 KiB (1%) |         174 |
| `["findfirst", "10%", "tx-noterm"]`                                | 566.304 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                   | 105.300 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                     | 350.402 μs (5%) |           |                  |             |
| `["findfirst", "20%", "tx"]`                                       | 199.901 μs (5%) |           |   11.86 KiB (1%) |         161 |
| `["findfirst", "20%", "tx-noterm"]`                                | 562.204 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                   | 210.501 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                     | 525.603 μs (5%) |           |                  |             |
| `["findfirst", "30%", "tx"]`                                       | 199.602 μs (5%) |           |    9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                | 559.104 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                   | 315.602 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                     | 700.804 μs (5%) |           |                  |             |
| `["findfirst", "40%", "tx"]`                                       | 250.200 μs (5%) |           |   12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                | 558.504 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                   | 420.701 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                     | 876.005 μs (5%) |           |                  |             |
| `["findfirst", "50%", "tx"]`                                       | 343.002 μs (5%) |           |   16.86 KiB (1%) |         237 |
| `["findfirst", "50%", "tx-noterm"]`                                | 565.804 μs (5%) |           |   17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                   | 525.903 μs (5%) |           |   192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 304.970 ms (5%) | 30.544 ms |  305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 243.828 ms (5%) | 30.327 ms |  305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  10.123 ms (5%) |           |                  |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   8.287 ms (5%) |           |                  |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   7.781 ms (5%) |           |   19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   4.192 ms (5%) |           |    9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                | 749.909 μs (5%) |           |                  |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.122 ms (5%) |           |                  |             |
| `["foreach_seq", "base", "Vector"]`                                | 750.209 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 758.909 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.165 ms (5%) |           |                  |             |
| `["foreach_seq", "tx", "Vector"]`                                  | 750.209 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  23.700 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  23.400 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  23.100 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  22.900 μs (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "man"]`                          |  93.921 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  93.909 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  92.873 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  97.372 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.100 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.080 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.767 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.767 μs (5%) |           |                  |             |
| `["mapi", "collatz", "base"]`                                      | 288.581 ms (5%) |           |    7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 252.878 ms (5%) | 18.157 ms |  189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.308 ms (5%) |           |   58.75 KiB (1%) |        1177 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.343 ms (5%) |           |   58.75 KiB (1%) |        1180 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.987 ms (5%) |           |                  |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.227 ms (5%) |           |    1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 742.008 μs (5%) |           |  946.94 KiB (1%) |         973 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 809.810 μs (5%) |           |    1.04 MiB (1%) |         992 |
| `["sort", "F64 (wide)", "Base"]`                                   |   7.212 ms (5%) |           |                  |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.791 ms (5%) |           |    1.17 MiB (1%) |         318 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.745 ms (5%) |           | 1005.03 KiB (1%) |        1825 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.513 ms (5%) |           |    1.37 MiB (1%) |        1870 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 132.802 μs (5%) |           |   160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 127.001 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 128.002 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 127.801 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                   |   6.881 ms (5%) |           |                  |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.991 ms (5%) |           |    1.17 MiB (1%) |         312 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.401 ms (5%) |           | 1015.12 KiB (1%) |        2007 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.218 ms (5%) |           |    1.38 MiB (1%) |        2041 |
| `["sort", "reversed", "Base"]`                                     | 781.309 μs (5%) |           |                  |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.336 ms (5%) |           |    1.17 MiB (1%) |         269 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 920.711 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.462 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["sort", "sorted", "Base"]`                                       | 723.409 μs (5%) |           |                  |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |   1.085 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 914.910 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.236 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   5.020 ms (5%) |           |   832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   2.271 ms (5%) |           |   22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.664 ms (5%) |           |   65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.446 ms (5%) |           |    1.04 MiB (1%) |         619 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7410 s          2 s        262 s       1842 s          0 s
       #2  2593 MHz       4409 s          0 s        220 s       4896 s          0 s
       
  Memory: 6.790924072265625 GB (2566.4453125 MB free)
  Uptime: 957.0 sec
  Load Avg:  1.19  1.23  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 15 Aug 2021 - 0:58
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
| `["findfirst", "0%", "tx"]`                                        |   5.333 μs (5%) |           |    3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 390.805 μs (5%) |           |   17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                    |  95.494 ns (5%) |           |   176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                     | 175.202 μs (5%) |           |                  |             |
| `["findfirst", "10%", "tx"]`                                       | 103.201 μs (5%) |           |   11.72 KiB (1%) |         155 |
| `["findfirst", "10%", "tx-noterm"]`                                | 377.604 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                   | 105.301 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                     | 350.404 μs (5%) |           |                  |             |
| `["findfirst", "20%", "tx"]`                                       | 130.802 μs (5%) |           |    9.66 KiB (1%) |         135 |
| `["findfirst", "20%", "tx-noterm"]`                                | 376.105 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                   | 210.602 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                     | 525.606 μs (5%) |           |                  |             |
| `["findfirst", "30%", "tx"]`                                       | 136.002 μs (5%) |           |    9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                | 385.405 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                   | 315.703 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                     | 700.808 μs (5%) |           |                  |             |
| `["findfirst", "40%", "tx"]`                                       | 179.303 μs (5%) |           |   12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                | 390.205 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                   | 420.805 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                     | 876.010 μs (5%) |           |                  |             |
| `["findfirst", "50%", "tx"]`                                       | 248.003 μs (5%) |           |   16.86 KiB (1%) |         237 |
| `["findfirst", "50%", "tx-noterm"]`                                | 390.804 μs (5%) |           |   17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                   | 525.807 μs (5%) |           |   192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 311.478 ms (5%) | 28.263 ms |  305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 244.370 ms (5%) | 28.077 ms |  305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  11.122 ms (5%) |           |                  |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   8.868 ms (5%) |           |                  |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   8.431 ms (5%) |           |   19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   4.568 ms (5%) |           |    9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                | 749.909 μs (5%) |           |                  |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.507 ms (5%) |           |                  |             |
| `["foreach_seq", "base", "Vector"]`                                |   1.002 ms (5%) |           |                  |             |
| `["foreach_seq", "tx", "Matrix"]`                                  |   1.011 ms (5%) |           |                  |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.481 ms (5%) |           |                  |             |
| `["foreach_seq", "tx", "Vector"]`                                  | 750.109 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  23.400 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  22.201 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  22.700 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  22.700 μs (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "man"]`                          |  93.921 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.000 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.100 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.700 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.700 μs (5%) |           |                  |             |
| `["mapi", "collatz", "base"]`                                      | 332.926 ms (5%) |           |    7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 297.582 ms (5%) | 28.623 ms |  189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.235 ms (5%) |           |   58.75 KiB (1%) |        1175 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.270 ms (5%) |           |   58.70 KiB (1%) |        1172 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.609 ms (5%) |           |                  |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.833 ms (5%) |           |    1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 749.709 μs (5%) |           |  946.94 KiB (1%) |         973 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 760.409 μs (5%) |           |    1.04 MiB (1%) |         992 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.574 ms (5%) |           |                  |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.309 ms (5%) |           |    1.17 MiB (1%) |         320 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.598 ms (5%) |           | 1005.03 KiB (1%) |        1825 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.987 ms (5%) |           |    1.37 MiB (1%) |        1870 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 130.702 μs (5%) |           |   160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 119.901 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 120.302 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 125.101 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                   |   6.879 ms (5%) |           |                  |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.688 ms (5%) |           |    1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.462 ms (5%) |           | 1015.12 KiB (1%) |        2007 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.671 ms (5%) |           |    1.38 MiB (1%) |        2041 |
| `["sort", "reversed", "Base"]`                                     | 781.909 μs (5%) |           |                  |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.199 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 952.112 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.333 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["sort", "sorted", "Base"]`                                       | 725.608 μs (5%) |           |                  |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 937.411 μs (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 929.711 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.141 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   5.021 ms (5%) |           |   832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   2.371 ms (5%) |           |   22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.661 ms (5%) |           |   65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.516 ms (5%) |           |    1.04 MiB (1%) |         619 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      11221 s          2 s        378 s       2084 s          0 s
       #2  2593 MHz       5909 s          0 s        275 s       7502 s          0 s
       
  Memory: 6.790924072265625 GB (2673.40234375 MB free)
  Uptime: 1375.0 sec
  Load Avg:  1.29  1.37  1.09
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
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    Stepping:                        7
    CPU MHz:                         2593.906
    BogoMIPS:                        5187.81
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
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
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

