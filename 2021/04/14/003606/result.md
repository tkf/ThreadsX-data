# Benchmark result

* Pull request commit: [`9131d70b79a6fa4492015cd04bc14c121df830d1`](https://github.com/tkf/ThreadsX.jl/commit/9131d70b79a6fa4492015cd04bc14c121df830d1)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 14 Apr 2021 - 00:27
    - Baseline: 14 Apr 2021 - 00:35
* Package commits:
    - Target: 764883
    - Baseline: 3ff826
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
| `["findfirst", "0%", "base"]`                                      | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx"]`                                        | 0.88 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["findfirst", "0%", "tx-noterm"]`                                 |               16.54 (5%) :x: |                2.06 (1%) :x: |
| `["findfirst", "0%", "tx-seq"]`                                    | 0.67 (5%) :white_check_mark: | 0.71 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx"]`                                       |                2.73 (5%) :x: |                2.26 (1%) :x: |
| `["findfirst", "10%", "tx-noterm"]`                                |                2.08 (5%) :x: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx-seq"]`                                   | 0.87 (5%) :white_check_mark: | 0.72 (1%) :white_check_mark: |
| `["findfirst", "20%", "tx"]`                                       |                1.56 (5%) :x: |                1.31 (1%) :x: |
| `["findfirst", "20%", "tx-noterm"]`                                |                2.19 (5%) :x: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "20%", "tx-seq"]`                                   |                1.14 (5%) :x: | 0.72 (1%) :white_check_mark: |
| `["findfirst", "30%", "base"]`                                     | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                                       |                1.26 (5%) :x: |                1.39 (1%) :x: |
| `["findfirst", "30%", "tx-noterm"]`                                |                1.86 (5%) :x: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "30%", "tx-seq"]`                                   | 0.87 (5%) :white_check_mark: | 0.72 (1%) :white_check_mark: |
| `["findfirst", "40%", "base"]`                                     |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                                       |                   1.03 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx-noterm"]`                                |                1.72 (5%) :x: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx-seq"]`                                   | 0.94 (5%) :white_check_mark: | 0.72 (1%) :white_check_mark: |
| `["findfirst", "50%", "base"]`                                     | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                                       |                1.16 (5%) :x: |                1.42 (1%) :x: |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.28 (5%) :x: | 0.62 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx-seq"]`                                   | 0.86 (5%) :white_check_mark: | 0.72 (1%) :white_check_mark: |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Vector"]`                                |                1.33 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Matrix"]`                                  | 0.58 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Vector"]`                                  | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |            56969.48 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |            51116.63 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |            56766.02 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.28 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.28 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "collatz", "base"]`                                      | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                                        | 0.94 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["mapi", "consume-100us", "tx"]`                                  |                   1.00 (5%)  |                1.02 (1%) :x: |
| `["sort", "F64 (narrow)", "Base"]`                                 |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "Base"]`                                   |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "Base"]`                                 | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   |                1.08 (5%) :x: | 0.59 (1%) :white_check_mark: |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   |                   0.96 (5%)  | 0.59 (1%) :white_check_mark: |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             |                1.09 (5%) :x: | 0.59 (1%) :white_check_mark: |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |                   0.96 (5%)  | 0.55 (1%) :white_check_mark: |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |                   0.97 (5%)  | 0.98 (1%) :white_check_mark: |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      56374 s          9 s       2799 s      45407 s          0 s
       #2  2095 MHz      74008 s         16 s       2775 s      28004 s          0 s
       
  Memory: 6.791343688964844 GB (2436.4609375 MB free)
  Uptime: 1053.0 sec
  Load Avg:  1.22314453125  1.2919921875  0.92578125
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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      79632 s          9 s       3464 s      65927 s          0 s
       #2  2095 MHz     108082 s         16 s       3672 s      37496 s          0 s
       
  Memory: 6.791343688964844 GB (2758.328125 MB free)
  Uptime: 1499.0 sec
  Load Avg:  1.287109375  1.3369140625  1.0869140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 14 Apr 2021 - 0:27
* Package commit: 764883
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
| `["findfirst", "0%", "base"]`                                      |   4.100 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  23.900 μs (5%) |           |  11.77 KiB (1%) |         218 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 410.208 μs (5%) |           |  24.72 KiB (1%) |         246 |
| `["findfirst", "0%", "tx-seq"]`                                    | 176.063 ns (5%) |           |  400 bytes (1%) |          13 |
| `["findfirst", "10%", "base"]`                                     | 116.802 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       | 225.505 μs (5%) |           |  32.61 KiB (1%) |         608 |
| `["findfirst", "10%", "tx-noterm"]`                                | 449.709 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "10%", "tx-seq"]`                                   | 102.002 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "20%", "base"]`                                     | 233.704 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 223.105 μs (5%) |           |  28.02 KiB (1%) |         523 |
| `["findfirst", "20%", "tx-noterm"]`                                | 456.910 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "20%", "tx-seq"]`                                   | 234.404 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "30%", "base"]`                                     | 289.706 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 254.205 μs (5%) |           |  39.53 KiB (1%) |         737 |
| `["findfirst", "30%", "tx-noterm"]`                                | 459.209 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "30%", "tx-seq"]`                                   | 305.906 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "40%", "base"]`                                     | 467.309 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 284.606 μs (5%) |           |  35.03 KiB (1%) |         655 |
| `["findfirst", "40%", "tx-noterm"]`                                | 472.810 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "40%", "tx-seq"]`                                   | 439.509 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "50%", "base"]`                                     | 584.111 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 364.707 μs (5%) |           |  53.56 KiB (1%) |        1001 |
| `["findfirst", "50%", "tx-noterm"]`                                | 470.509 μs (5%) |           |  24.91 KiB (1%) |         258 |
| `["findfirst", "50%", "tx-seq"]`                                   | 540.011 μs (5%) |           |  416 bytes (1%) |          14 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 318.288 ms (5%) | 30.296 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 254.234 ms (5%) | 30.573 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   9.572 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   7.211 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   4.741 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.637 ms (5%) |           |  12.78 KiB (1%) |         126 |
| `["foreach_seq", "base", "Matrix"]`                                |   1.140 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.460 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                |   1.171 ms (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 689.414 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.355 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 774.715 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  24.201 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  24.501 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  27.001 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  24.400 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  56.722 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  56.969 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  51.117 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  56.766 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.280 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.280 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   3.087 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   3.325 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 372.771 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 234.638 ms (5%) |  3.575 ms | 157.49 MiB (1%) |     2016682 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.186 ms (5%) |           |  59.34 KiB (1%) |        1115 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.324 ms (5%) |           |  59.97 KiB (1%) |        1132 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   3.485 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.485 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 710.414 μs (5%) |           | 965.13 KiB (1%) |        1227 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 712.515 μs (5%) |           |   1.02 MiB (1%) |        1247 |
| `["sort", "F64 (wide)", "Base"]`                                   |   8.646 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   6.646 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.415 ms (5%) |           |   1.01 MiB (1%) |        2149 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.292 ms (5%) |           |   1.39 MiB (1%) |        2197 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 133.603 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 133.003 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 129.303 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 136.402 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (wide)", "Base"]`                                   |   8.693 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   5.827 ms (5%) |           |   1.19 MiB (1%) |         549 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   4.121 ms (5%) |           |   1.01 MiB (1%) |        2232 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.974 ms (5%) |           |   1.40 MiB (1%) |        2269 |
| `["sort", "reversed", "Base"]`                                     |   1.140 ms (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.501 ms (5%) |           |   1.18 MiB (1%) |         430 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.082 ms (5%) |           | 998.42 KiB (1%) |        1867 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.590 ms (5%) |           |   1.36 MiB (1%) |        1899 |
| `["sort", "sorted", "Base"]`                                       |   1.013 ms (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |   1.112 ms (5%) |           |   1.18 MiB (1%) |         427 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |   1.064 ms (5%) |           | 998.41 KiB (1%) |        1866 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.324 ms (5%) |           |   1.36 MiB (1%) |        1896 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |  11.075 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   5.740 ms (5%) |           |  28.06 KiB (1%) |         368 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |  10.063 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   6.055 ms (5%) |           |   1.05 MiB (1%) |         672 |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      56374 s          9 s       2799 s      45407 s          0 s
       #2  2095 MHz      74008 s         16 s       2775 s      28004 s          0 s
       
  Memory: 6.791343688964844 GB (2436.4609375 MB free)
  Uptime: 1053.0 sec
  Load Avg:  1.22314453125  1.2919921875  0.92578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 14 Apr 2021 - 0:35
* Package commit: 3ff826
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
| `["findfirst", "0%", "base"]`                                      |   4.400 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  27.201 μs (5%) |           |  11.98 KiB (1%) |         220 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  24.801 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 262.343 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     | 116.802 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  82.702 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 216.704 μs (5%) |           |  33.00 KiB (1%) |         609 |
| `["findfirst", "10%", "tx-seq"]`                                   | 117.202 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 233.804 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 142.703 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 208.904 μs (5%) |           |  33.09 KiB (1%) |         615 |
| `["findfirst", "20%", "tx-seq"]`                                   | 204.904 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 350.512 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 201.404 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 246.305 μs (5%) |           |  28.42 KiB (1%) |         529 |
| `["findfirst", "30%", "tx-seq"]`                                   | 351.375 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 429.109 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 275.705 μs (5%) |           |  35.41 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-noterm"]`                                | 275.406 μs (5%) |           |  35.41 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-seq"]`                                   | 468.010 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 630.812 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 314.006 μs (5%) |           |  37.84 KiB (1%) |         707 |
| `["findfirst", "50%", "tx-noterm"]`                                | 366.508 μs (5%) |           |  40.20 KiB (1%) |         753 |
| `["findfirst", "50%", "tx-seq"]`                                   | 625.017 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 315.947 ms (5%) | 27.945 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 251.444 ms (5%) | 27.835 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  10.113 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   7.135 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   4.911 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.758 ms (5%) |           |  12.78 KiB (1%) |         126 |
| `["foreach_seq", "base", "Matrix"]`                                |   1.186 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.446 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 877.717 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  |   1.179 ms (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.362 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 834.317 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  24.301 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  24.500 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  29.100 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  24.401 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  57.029 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.000 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.000 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   3.100 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   3.100 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 401.831 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 249.721 ms (5%) |  5.194 ms | 159.57 MiB (1%) |     2016682 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.189 ms (5%) |           |  58.45 KiB (1%) |        1098 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.328 ms (5%) |           |  59.91 KiB (1%) |        1130 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.994 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.577 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 701.514 μs (5%) |           | 965.11 KiB (1%) |        1226 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 711.014 μs (5%) |           |   1.02 MiB (1%) |        1248 |
| `["sort", "F64 (wide)", "Base"]`                                   |   7.802 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   6.764 ms (5%) |           |   1.19 MiB (1%) |         563 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.438 ms (5%) |           |   1.01 MiB (1%) |        2147 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.265 ms (5%) |           |   1.39 MiB (1%) |        2197 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 146.603 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 123.103 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 134.703 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 125.502 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   8.738 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   5.631 ms (5%) |           |   1.19 MiB (1%) |         555 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   4.099 ms (5%) |           |   1.01 MiB (1%) |        2238 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.895 ms (5%) |           |   1.40 MiB (1%) |        2273 |
| `["sort", "reversed", "Base"]`                                     |   1.104 ms (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.443 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.072 ms (5%) |           | 998.70 KiB (1%) |        1868 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.616 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["sort", "sorted", "Base"]`                                       |   1.061 ms (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |   1.027 ms (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |   1.032 ms (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.231 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |  10.976 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   5.957 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |  10.031 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   6.271 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      79632 s          9 s       3464 s      65927 s          0 s
       #2  2095 MHz     108082 s         16 s       3672 s      37496 s          0 s
       
  Memory: 6.791343688964844 GB (2758.328125 MB free)
  Uptime: 1499.0 sec
  Load Avg:  1.287109375  1.3369140625  1.0869140625
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

