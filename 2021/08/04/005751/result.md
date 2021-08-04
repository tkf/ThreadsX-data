# Benchmark result

* Pull request commit: [`2beca782bc08c831f9cf141fd92680ae1a6d0727`](https://github.com/tkf/ThreadsX.jl/commit/2beca782bc08c831f9cf141fd92680ae1a6d0727)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 Aug 2021 - 00:50
    - Baseline: 4 Aug 2021 - 00:57
* Package commits:
    - Target: f560fb
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
| `["findfirst", "0%", "base"]`                                      |                1.32 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx"]`                                        |                1.30 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx-noterm"]`                                 | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx-seq"]`                                    |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                                       |                   1.01 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "10%", "tx-noterm"]`                                |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                                       | 0.93 (5%) :white_check_mark: | 0.68 (1%) :white_check_mark: |
| `["findfirst", "20%", "tx-noterm"]`                                |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                                       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                                       | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "tx", "A .= B .+ B'"]`                                | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Transpose"]`                             | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Vector"]`                                | 0.75 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Matrix"]`                                  | 0.65 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Transpose"]`                               | 0.80 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Vector"]`                                  |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "man"]`                       |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "man"]`                          | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 0.78 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 0.77 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "collatz", "base"]`                                      |                1.28 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                                        |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "consume-100us", "tx"]`                                  |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (narrow)", "Base"]`                                 |                1.28 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "Base"]`                                   |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "Base"]`                                   | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |

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
       #1  2095 MHz       5416 s          1 s        236 s       7328 s          0 s
       #2  2095 MHz       6544 s          1 s        257 s       6187 s          0 s
       
  Memory: 6.790924072265625 GB (2557.59765625 MB free)
  Uptime: 1306.0 sec
  Load Avg:  1.28  1.32  0.93
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
       #1  2095 MHz       8444 s          1 s        301 s       8517 s          0 s
       #2  2095 MHz       9080 s          1 s        349 s       7837 s          0 s
       
  Memory: 6.790924072265625 GB (2915.6953125 MB free)
  Uptime: 1735.0 sec
  Load Avg:  1.23  1.33  1.09
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 4 Aug 2021 - 0:50
* Package commit: f560fb
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
| `["findfirst", "0%", "tx"]`                                        |   6.267 μs (5%) |           |    3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 542.536 μs (5%) |           |   17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                    |  93.696 ns (5%) |           |   176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                     | 146.009 μs (5%) |           |                  |             |
| `["findfirst", "10%", "tx"]`                                       | 189.513 μs (5%) |           |   13.23 KiB (1%) |         175 |
| `["findfirst", "10%", "tx-noterm"]`                                | 578.839 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                   |  59.004 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                     | 292.020 μs (5%) |           |                  |             |
| `["findfirst", "20%", "tx"]`                                       | 213.514 μs (5%) |           |    9.59 KiB (1%) |         132 |
| `["findfirst", "20%", "tx-noterm"]`                                | 628.241 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                   | 118.108 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                     | 438.029 μs (5%) |           |                  |             |
| `["findfirst", "30%", "tx"]`                                       | 197.413 μs (5%) |           |    9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                | 555.137 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                   | 176.411 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                     | 584.039 μs (5%) |           |                  |             |
| `["findfirst", "40%", "tx"]`                                       | 240.016 μs (5%) |           |   12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                | 576.738 μs (5%) |           |   17.44 KiB (1%) |         252 |
| `["findfirst", "40%", "tx-seq"]`                                   | 234.915 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                     | 729.948 μs (5%) |           |                  |             |
| `["findfirst", "50%", "tx"]`                                       | 418.228 μs (5%) |           |   16.89 KiB (1%) |         238 |
| `["findfirst", "50%", "tx-noterm"]`                                | 572.038 μs (5%) |           |   17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                   | 293.420 μs (5%) |           |   192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 330.652 ms (5%) | 32.018 ms |  305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 279.973 ms (5%) | 32.845 ms |  305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   7.852 ms (5%) |           |                  |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.880 ms (5%) |           |                  |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   6.384 ms (5%) |           |   19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.471 ms (5%) |           |    9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                | 625.842 μs (5%) |           |                  |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.061 ms (5%) |           |                  |             |
| `["foreach_seq", "base", "Vector"]`                                | 625.342 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 633.042 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.034 ms (5%) |           |                  |             |
| `["foreach_seq", "tx", "Vector"]`                                  | 725.946 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  23.001 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  22.601 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  20.901 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  24.901 μs (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "man"]`                          |  78.247 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  78.279 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  77.427 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  81.296 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 918.812 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 964.765 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.300 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.311 μs (5%) |           |                  |             |
| `["mapi", "collatz", "base"]`                                      | 394.105 ms (5%) |           |    7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 319.022 ms (5%) | 13.393 ms |  189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.319 ms (5%) |           |   58.80 KiB (1%) |        1174 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.398 ms (5%) |           |   58.61 KiB (1%) |        1170 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.817 ms (5%) |           |                  |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.343 ms (5%) |           |    1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 689.211 μs (5%) |           |  946.94 KiB (1%) |         973 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 771.251 μs (5%) |           |    1.04 MiB (1%) |         992 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.943 ms (5%) |           |                  |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.665 ms (5%) |           |    1.17 MiB (1%) |         317 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.027 ms (5%) |           | 1005.03 KiB (1%) |        1825 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.896 ms (5%) |           |    1.37 MiB (1%) |        1870 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 118.708 μs (5%) |           |   160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 114.008 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 111.508 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 112.108 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.952 ms (5%) |           |                  |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.963 ms (5%) |           |    1.17 MiB (1%) |         312 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.193 ms (5%) |           | 1015.12 KiB (1%) |        2007 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.420 ms (5%) |           |    1.38 MiB (1%) |        2041 |
| `["sort", "reversed", "Base"]`                                     | 643.842 μs (5%) |           |                  |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.202 ms (5%) |           |    1.17 MiB (1%) |         269 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 856.655 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.321 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["sort", "sorted", "Base"]`                                       | 599.240 μs (5%) |           |                  |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 968.464 μs (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 878.659 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.139 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   4.684 ms (5%) |           |   832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   2.186 ms (5%) |           |   22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.396 ms (5%) |           |   65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.231 ms (5%) |           |    1.04 MiB (1%) |         619 |

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
       #1  2095 MHz       5416 s          1 s        236 s       7328 s          0 s
       #2  2095 MHz       6544 s          1 s        257 s       6187 s          0 s
       
  Memory: 6.790924072265625 GB (2557.59765625 MB free)
  Uptime: 1306.0 sec
  Load Avg:  1.28  1.32  0.93
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 4 Aug 2021 - 0:57
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
| `["findfirst", "0%", "base"]`                                      |   2.200 ns (5%) |           |                  |             |
| `["findfirst", "0%", "tx"]`                                        |   4.817 μs (5%) |           |    3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 627.042 μs (5%) |           |   17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                    |  79.898 ns (5%) |           |   176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                     | 146.009 μs (5%) |           |                  |             |
| `["findfirst", "10%", "tx"]`                                       | 188.512 μs (5%) |           |   12.56 KiB (1%) |         169 |
| `["findfirst", "10%", "tx-noterm"]`                                | 536.736 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                   |  87.705 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                     | 292.020 μs (5%) |           |                  |             |
| `["findfirst", "20%", "tx"]`                                       | 228.916 μs (5%) |           |   14.11 KiB (1%) |         187 |
| `["findfirst", "20%", "tx-noterm"]`                                | 574.039 μs (5%) |           |   17.44 KiB (1%) |         252 |
| `["findfirst", "20%", "tx-seq"]`                                   | 175.512 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                     | 438.029 μs (5%) |           |                  |             |
| `["findfirst", "30%", "tx"]`                                       | 218.715 μs (5%) |           |    9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                | 566.739 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                   | 263.217 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                     | 584.039 μs (5%) |           |                  |             |
| `["findfirst", "40%", "tx"]`                                       | 282.119 μs (5%) |           |   12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                | 570.539 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                   | 350.723 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                     | 730.048 μs (5%) |           |                  |             |
| `["findfirst", "50%", "tx"]`                                       | 407.928 μs (5%) |           |   16.89 KiB (1%) |         238 |
| `["findfirst", "50%", "tx-noterm"]`                                | 571.038 μs (5%) |           |   17.59 KiB (1%) |         260 |
| `["findfirst", "50%", "tx-seq"]`                                   | 438.329 μs (5%) |           |   192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 317.668 ms (5%) | 27.920 ms |  305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 269.391 ms (5%) | 42.144 ms |  305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   8.292 ms (5%) |           |                  |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.593 ms (5%) |           |                  |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   6.727 ms (5%) |           |   19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.397 ms (5%) |           |    9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                | 625.744 μs (5%) |           |                  |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.314 ms (5%) |           |                  |             |
| `["foreach_seq", "base", "Vector"]`                                | 835.555 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 978.065 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.296 ms (5%) |           |                  |             |
| `["foreach_seq", "tx", "Vector"]`                                  | 629.642 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  21.202 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  20.701 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  20.602 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  23.602 μs (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "man"]`                          |  90.905 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 900.000 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 900.000 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.300 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.300 μs (5%) |           |                  |             |
| `["mapi", "collatz", "base"]`                                      | 306.845 ms (5%) |           |    7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 302.994 ms (5%) | 23.615 ms |  189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.209 ms (5%) |           |   58.61 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.002 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.275 ms (5%) |           |   58.97 KiB (1%) |        1179 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.198 ms (5%) |           |                  |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.232 ms (5%) |           |    1.17 MiB (1%) |         296 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 712.647 μs (5%) |           |  946.94 KiB (1%) |         973 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 837.156 μs (5%) |           |    1.04 MiB (1%) |         992 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.471 ms (5%) |           |                  |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.558 ms (5%) |           |    1.17 MiB (1%) |         318 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.901 ms (5%) |           | 1005.03 KiB (1%) |        1825 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.832 ms (5%) |           |    1.37 MiB (1%) |        1870 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 114.508 μs (5%) |           |   160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 111.407 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 112.107 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 111.207 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                   |   6.309 ms (5%) |           |                  |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.379 ms (5%) |           |    1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.552 ms (5%) |           | 1015.12 KiB (1%) |        2007 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.004 ms (5%) |           |    1.38 MiB (1%) |        2041 |
| `["sort", "reversed", "Base"]`                                     | 641.543 μs (5%) |           |                  |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.080 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 866.858 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.182 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["sort", "sorted", "Base"]`                                       | 601.242 μs (5%) |           |                  |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 840.060 μs (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 919.064 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.056 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   4.545 ms (5%) |           |   832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   2.364 ms (5%) |           |   22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.683 ms (5%) |           |   65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.110 ms (5%) |           |    1.04 MiB (1%) |         619 |

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
       #1  2095 MHz       8444 s          1 s        301 s       8517 s          0 s
       #2  2095 MHz       9080 s          1 s        349 s       7837 s          0 s
       
  Memory: 6.790924072265625 GB (2915.6953125 MB free)
  Uptime: 1735.0 sec
  Load Avg:  1.23  1.33  1.09
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
    CPU MHz:                         2095.198
    BogoMIPS:                        4190.39
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

