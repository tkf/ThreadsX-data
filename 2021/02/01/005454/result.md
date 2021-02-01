# Benchmark result

* Pull request commit: [`af749e7c289def0f2d5bead1648d1836c1e80850`](https://github.com/tkf/ThreadsX.jl/commit/af749e7c289def0f2d5bead1648d1836c1e80850)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 1 Feb 2021 - 00:47
    - Baseline: 1 Feb 2021 - 00:54
* Package commits:
    - Target: cc61ff
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
| `["findfirst", "0%", "base"]`                                      | 0.73 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx"]`                                        | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx-noterm"]`                                 | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                                       |                1.33 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx-noterm"]`                                |                   1.03 (5%)  | 0.94 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                                       |                1.32 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx-noterm"]`                                |                1.23 (5%) :x: |                1.28 (1%) :x: |
| `["findfirst", "20%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                                       |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                                |                1.41 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                                       |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                                |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                                       |                1.23 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.23 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx-seq"]`                                   | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "base", "A .= B .+ B'"]`                              |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["foreach", "base", "A .= B .+ C"]`                               |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["foreach", "tx", "A .= B .+ B'"]`                                |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Matrix"]`                                | 0.64 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Transpose"]`                             | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Matrix"]`                                  | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Transpose"]`                               | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Vector"]`                                  |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "man"]`                       | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "man"]`                          | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |            43670.72 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |            45099.09 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |            43739.39 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "collatz", "base"]`                                      | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                                        | 0.86 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["mapi", "consume-100us", "tx"]`                                  |                   1.00 (5%)  |                1.02 (1%) :x: |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "Base"]`                                   | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 20.04.1 LTS
  uname: Linux 5.4.0-1036-azure #38-Ubuntu SMP Wed Jan 6 18:26:25 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      68891 s          9 s       2528 s      24795 s          0 s
       #2  2095 MHz      52433 s         10 s       2927 s      41431 s          0 s
       
  Memory: 6.791378021240234 GB (2699.55078125 MB free)
  Uptime: 978.0 sec
  Load Avg:  1.31298828125  1.33056640625  0.94287109375
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
      Ubuntu 20.04.1 LTS
  uname: Linux 5.4.0-1036-azure #38-Ubuntu SMP Wed Jan 6 18:26:25 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      98871 s          9 s       3550 s      34956 s          0 s
       #2  2095 MHz      75428 s         10 s       3657 s      58854 s          0 s
       
  Memory: 6.791378021240234 GB (2946.42578125 MB free)
  Uptime: 1390.0 sec
  Load Avg:  1.2919921875  1.37890625  1.10986328125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 1 Feb 2021 - 0:47
* Package commit: cc61ff
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
| `["findfirst", "0%", "tx"]`                                        |  20.001 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  19.302 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 186.942 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  87.605 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  88.506 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 193.213 μs (5%) |           |  42.14 KiB (1%) |         774 |
| `["findfirst", "10%", "tx-seq"]`                                   |  58.903 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 175.211 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 141.109 μs (5%) |           |  21.44 KiB (1%) |         400 |
| `["findfirst", "20%", "tx-noterm"]`                                | 213.714 μs (5%) |           |  42.25 KiB (1%) |         779 |
| `["findfirst", "20%", "tx-seq"]`                                   | 118.107 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 262.917 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 200.113 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 238.015 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 176.511 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 350.422 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 270.418 μs (5%) |           |  35.41 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-noterm"]`                                | 258.517 μs (5%) |           |  35.44 KiB (1%) |         658 |
| `["findfirst", "40%", "tx-seq"]`                                   | 234.815 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 438.028 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 305.920 μs (5%) |           |  37.86 KiB (1%) |         708 |
| `["findfirst", "50%", "tx-noterm"]`                                | 346.523 μs (5%) |           |  54.08 KiB (1%) |        1004 |
| `["findfirst", "50%", "tx-seq"]`                                   | 293.119 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 283.239 ms (5%) | 25.524 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 242.089 ms (5%) | 28.468 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   6.925 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.268 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   4.076 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.275 ms (5%) |           |  12.78 KiB (1%) |         126 |
| `["foreach_seq", "base", "Matrix"]`                                | 625.641 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   1.804 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 621.440 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 842.054 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.051 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 835.554 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  17.901 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  17.701 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  21.701 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  16.901 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  43.739 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  43.671 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  45.099 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  43.739 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 927.833 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 939.357 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.311 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.300 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 286.258 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 186.477 ms (5%) | 12.293 ms | 155.84 MiB (1%) |     2016677 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.183 ms (5%) |           |  59.56 KiB (1%) |        1121 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.257 ms (5%) |           |  59.81 KiB (1%) |        1127 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.150 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.901 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 589.338 μs (5%) |           | 965.16 KiB (1%) |        1229 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 601.839 μs (5%) |           |   1.02 MiB (1%) |        1248 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.448 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.812 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.188 ms (5%) |           |   1.01 MiB (1%) |        2146 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.998 ms (5%) |           |   1.39 MiB (1%) |        2196 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 117.108 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 107.607 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 105.507 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 104.106 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   6.113 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.614 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.359 ms (5%) |           |   1.01 MiB (1%) |        2237 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.052 ms (5%) |           |   1.40 MiB (1%) |        2272 |
| `["sort", "reversed", "Base"]`                                     | 793.752 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.260 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 873.657 μs (5%) |           | 998.77 KiB (1%) |        1872 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.413 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["sort", "sorted", "Base"]`                                       | 761.950 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 867.856 μs (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 871.257 μs (5%) |           | 998.77 KiB (1%) |        1872 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.048 ms (5%) |           |   1.36 MiB (1%) |        1902 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   7.846 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.891 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.007 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.550 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
      Ubuntu 20.04.1 LTS
  uname: Linux 5.4.0-1036-azure #38-Ubuntu SMP Wed Jan 6 18:26:25 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      68891 s          9 s       2528 s      24795 s          0 s
       #2  2095 MHz      52433 s         10 s       2927 s      41431 s          0 s
       
  Memory: 6.791378021240234 GB (2699.55078125 MB free)
  Uptime: 978.0 sec
  Load Avg:  1.31298828125  1.33056640625  0.94287109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 1 Feb 2021 - 0:54
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
| `["findfirst", "0%", "base"]`                                      |   3.000 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  22.601 μs (5%) |           |  11.98 KiB (1%) |         220 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  21.102 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 193.166 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  87.605 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  66.504 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 187.112 μs (5%) |           |  44.63 KiB (1%) |         826 |
| `["findfirst", "10%", "tx-seq"]`                                   |  87.905 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 175.411 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 106.807 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 173.811 μs (5%) |           |  33.05 KiB (1%) |         612 |
| `["findfirst", "20%", "tx-seq"]`                                   | 175.811 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 262.917 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 171.712 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 169.211 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 263.417 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 350.422 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 231.115 μs (5%) |           |  35.39 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-noterm"]`                                | 237.716 μs (5%) |           |  35.45 KiB (1%) |         659 |
| `["findfirst", "40%", "tx-seq"]`                                   | 351.022 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 438.028 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 247.716 μs (5%) |           |  37.84 KiB (1%) |         707 |
| `["findfirst", "50%", "tx-noterm"]`                                | 282.518 μs (5%) |           |  54.08 KiB (1%) |        1004 |
| `["findfirst", "50%", "tx-seq"]`                                   | 438.528 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 268.214 ms (5%) | 24.636 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 211.745 ms (5%) | 23.072 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   6.822 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.151 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   3.681 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.173 ms (5%) |           |  12.77 KiB (1%) |         125 |
| `["foreach_seq", "base", "Matrix"]`                                | 970.163 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.058 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 625.841 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 977.663 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.170 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 721.347 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  19.401 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  19.001 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  21.902 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  19.601 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  49.296 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 800.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 800.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.300 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.300 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 345.580 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 217.732 ms (5%) |  5.854 ms | 161.51 MiB (1%) |     2016653 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.179 ms (5%) |           |  58.47 KiB (1%) |        1100 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.231 ms (5%) |           |  59.72 KiB (1%) |        1129 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.137 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.902 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 595.338 μs (5%) |           | 965.14 KiB (1%) |        1228 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 610.639 μs (5%) |           |   1.02 MiB (1%) |        1248 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.397 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.777 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.602 ms (5%) |           |   1.01 MiB (1%) |        2148 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.332 ms (5%) |           |   1.39 MiB (1%) |        2197 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 112.207 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 104.307 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 104.407 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 104.106 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   7.114 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.652 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.348 ms (5%) |           |   1.01 MiB (1%) |        2238 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.052 ms (5%) |           |   1.40 MiB (1%) |        2272 |
| `["sort", "reversed", "Base"]`                                     | 799.352 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.230 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 901.258 μs (5%) |           | 998.72 KiB (1%) |        1869 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.405 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["sort", "sorted", "Base"]`                                       | 758.349 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 868.856 μs (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 864.956 μs (5%) |           | 998.77 KiB (1%) |        1872 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.038 ms (5%) |           |   1.36 MiB (1%) |        1902 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   8.218 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.939 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.075 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.409 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
      Ubuntu 20.04.1 LTS
  uname: Linux 5.4.0-1036-azure #38-Ubuntu SMP Wed Jan 6 18:26:25 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      98871 s          9 s       3550 s      34956 s          0 s
       #2  2095 MHz      75428 s         10 s       3657 s      58854 s          0 s
       
  Memory: 6.791378021240234 GB (2946.42578125 MB free)
  Uptime: 1390.0 sec
  Load Avg:  1.2919921875  1.37890625  1.10986328125
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
    CPU MHz:                         2095.196
    BogoMIPS:                        4190.39
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

