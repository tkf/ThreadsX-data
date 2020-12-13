# Benchmark result

* Pull request commit: [`d31187c6c0900762af029479954e47907c335163`](https://github.com/tkf/ThreadsX.jl/commit/d31187c6c0900762af029479954e47907c335163)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 13 Dec 2020 - 00:45
    - Baseline: 13 Dec 2020 - 00:53
* Package commits:
    - Target: b0dcba
    - Baseline: 819e90
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
| `["findfirst", "0%", "base"]`                                      | 0.68 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx"]`                                        |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx-noterm"]`                                 | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx-noterm"]`                                |                   1.02 (5%)  | 0.90 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx-seq"]`                                   | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "20%", "base"]`                                     |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                                       |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx-noterm"]`                                |                   1.00 (5%)  |                1.78 (1%) :x: |
| `["findfirst", "30%", "base"]`                                     | 0.75 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                                       |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-seq"]`                                   | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "base"]`                                     |                1.33 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                                       |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-seq"]`                                   |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "base"]`                                     |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx-seq"]`                                   |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["foreach", "tx", "A .= B .+ B'"]`                                |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Matrix"]`                                | 0.60 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Matrix"]`                                  | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Vector"]`                                  |                1.28 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "man"]`                       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      | 0.75 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       | 0.79 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "man"]`                          |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |            56726.07 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |            45209.18 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |            43735.98 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                                        |                   1.01 (5%)  | 0.95 (1%) :white_check_mark: |
| `["sort", "F64 (narrow)", "Base"]`                                 | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "reversed", "Base"]`                                     | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "sorted", "Base"]`                                       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      54438 s          0 s       2810 s      44415 s          0 s
       #2  2095 MHz      70218 s          0 s       3092 s      28251 s          0 s
       
  Memory: 6.791393280029297 GB (2485.73046875 MB free)
  Uptime: 1034.0 sec
  Load Avg:  1.27880859375  1.3447265625  0.96533203125
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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      75430 s          0 s       3709 s      66042 s          0 s
       #2  2095 MHz     105097 s          0 s       3761 s      36218 s          0 s
       
  Memory: 6.791393280029297 GB (2952.96875 MB free)
  Uptime: 1470.0 sec
  Load Avg:  1.29638671875  1.32373046875  1.0888671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 13 Dec 2020 - 0:45
* Package commit: b0dcba
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
| `["findfirst", "0%", "tx"]`                                        |  28.001 μs (5%) |           |  11.98 KiB (1%) |         220 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  23.501 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 252.447 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     | 101.704 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  76.804 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 207.509 μs (5%) |           |  39.86 KiB (1%) |         734 |
| `["findfirst", "10%", "tx-seq"]`                                   | 102.104 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 233.609 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 146.906 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 222.109 μs (5%) |           |  42.25 KiB (1%) |         779 |
| `["findfirst", "20%", "tx-seq"]`                                   | 234.409 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 263.011 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 196.309 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 252.111 μs (5%) |           |  28.42 KiB (1%) |         529 |
| `["findfirst", "30%", "tx-seq"]`                                   | 263.712 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 467.219 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 271.511 μs (5%) |           |  35.41 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-noterm"]`                                | 280.712 μs (5%) |           |  35.45 KiB (1%) |         659 |
| `["findfirst", "40%", "tx-seq"]`                                   | 408.017 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 563.925 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 283.212 μs (5%) |           |  37.86 KiB (1%) |         708 |
| `["findfirst", "50%", "tx-noterm"]`                                | 342.414 μs (5%) |           |  54.08 KiB (1%) |        1004 |
| `["findfirst", "50%", "tx-seq"]`                                   | 555.324 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 304.090 ms (5%) | 30.147 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 249.420 ms (5%) | 30.247 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   9.287 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.793 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   4.521 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.482 ms (5%) |           |  12.77 KiB (1%) |         125 |
| `["foreach_seq", "base", "Matrix"]`                                | 665.475 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.293 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 793.988 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 977.904 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.310 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 970.403 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  22.002 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  24.603 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  23.202 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  20.702 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  58.373 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  56.726 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  45.209 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  43.736 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.190 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.090 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   3.075 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   3.075 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 403.047 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 250.121 ms (5%) |  6.422 ms | 156.85 MiB (1%) |     2016683 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.178 ms (5%) |           |  58.66 KiB (1%) |        1109 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.296 ms (5%) |           |  59.55 KiB (1%) |        1120 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.666 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.369 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 671.624 μs (5%) |           | 965.13 KiB (1%) |        1227 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 693.225 μs (5%) |           |   1.02 MiB (1%) |        1249 |
| `["sort", "F64 (wide)", "Base"]`                                   |   7.221 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   6.573 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.179 ms (5%) |           |   1.01 MiB (1%) |        2148 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.062 ms (5%) |           |   1.39 MiB (1%) |        2198 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 144.005 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 123.505 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 122.804 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 132.705 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   8.338 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   5.428 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.606 ms (5%) |           |   1.01 MiB (1%) |        2238 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.754 ms (5%) |           |   1.40 MiB (1%) |        2272 |
| `["sort", "reversed", "Base"]`                                     | 997.333 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.379 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.005 ms (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.597 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["sort", "sorted", "Base"]`                                       | 910.915 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 979.521 μs (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 989.023 μs (5%) |           | 998.72 KiB (1%) |        1869 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.179 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |  10.619 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   5.709 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   9.735 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.837 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      54438 s          0 s       2810 s      44415 s          0 s
       #2  2095 MHz      70218 s          0 s       3092 s      28251 s          0 s
       
  Memory: 6.791393280029297 GB (2485.73046875 MB free)
  Uptime: 1034.0 sec
  Load Avg:  1.27880859375  1.3447265625  0.96533203125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 13 Dec 2020 - 0:53
* Package commit: 819e90
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
| `["findfirst", "0%", "tx"]`                                        |  26.002 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  25.102 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 252.456 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     | 101.807 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  76.406 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 203.015 μs (5%) |           |  44.52 KiB (1%) |         819 |
| `["findfirst", "10%", "tx-seq"]`                                   | 117.308 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 203.515 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 136.110 μs (5%) |           |  21.44 KiB (1%) |         400 |
| `["findfirst", "20%", "tx-noterm"]`                                | 221.316 μs (5%) |           |  23.77 KiB (1%) |         443 |
| `["findfirst", "20%", "tx-seq"]`                                   | 234.317 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 350.428 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 180.915 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 240.119 μs (5%) |           |  28.42 KiB (1%) |         529 |
| `["findfirst", "30%", "tx-seq"]`                                   | 306.025 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 350.526 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 236.618 μs (5%) |           |  35.41 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-noterm"]`                                | 275.121 μs (5%) |           |  35.47 KiB (1%) |         660 |
| `["findfirst", "40%", "tx-seq"]`                                   | 378.529 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 508.740 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 291.822 μs (5%) |           |  37.86 KiB (1%) |         708 |
| `["findfirst", "50%", "tx-noterm"]`                                | 303.724 μs (5%) |           |  54.08 KiB (1%) |        1004 |
| `["findfirst", "50%", "tx-seq"]`                                   | 506.440 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 309.412 ms (5%) | 27.799 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 242.006 ms (5%) | 26.769 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   8.315 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.631 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   4.290 ms (5%) |           |  25.92 KiB (1%) |         359 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.417 ms (5%) |           |  12.75 KiB (1%) |         124 |
| `["foreach_seq", "base", "Matrix"]`                                |   1.114 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.412 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 834.248 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  |   1.131 ms (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.306 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 755.543 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  23.701 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  24.301 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  30.801 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  26.302 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  49.799 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.000 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.000 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   3.000 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   3.000 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 397.717 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 247.191 ms (5%) |  7.192 ms | 165.13 MiB (1%) |     2016650 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.181 ms (5%) |           |  58.39 KiB (1%) |        1097 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.002 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.252 ms (5%) |           |  59.20 KiB (1%) |        1116 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.867 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.468 ms (5%) |           |   1.19 MiB (1%) |         534 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 661.642 μs (5%) |           | 965.11 KiB (1%) |        1226 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 724.445 μs (5%) |           |   1.02 MiB (1%) |        1248 |
| `["sort", "F64 (wide)", "Base"]`                                   |   7.427 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   6.467 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.387 ms (5%) |           |   1.01 MiB (1%) |        2148 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.244 ms (5%) |           |   1.39 MiB (1%) |        2198 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 149.309 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 141.309 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 133.109 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 137.409 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   8.490 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   5.638 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   4.127 ms (5%) |           |   1.01 MiB (1%) |        2237 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.943 ms (5%) |           |   1.40 MiB (1%) |        2273 |
| `["sort", "reversed", "Base"]`                                     |   1.063 ms (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.429 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.061 ms (5%) |           | 998.73 KiB (1%) |        1870 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.655 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["sort", "sorted", "Base"]`                                       |   1.010 ms (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |   1.009 ms (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 965.857 μs (5%) |           | 998.77 KiB (1%) |        1872 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.180 ms (5%) |           |   1.36 MiB (1%) |        1902 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |  10.873 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   6.105 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |  10.019 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   6.263 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      75430 s          0 s       3709 s      66042 s          0 s
       #2  2095 MHz     105097 s          0 s       3761 s      36218 s          0 s
       
  Memory: 6.791393280029297 GB (2952.96875 MB free)
  Uptime: 1470.0 sec
  Load Avg:  1.29638671875  1.32373046875  1.0888671875
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

    Architecture:        x86_64
    CPU op-mode(s):      32-bit, 64-bit
    Byte Order:          Little Endian
    CPU(s):              2
    On-line CPU(s) list: 0,1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    NUMA node(s):        1
    Vendor ID:           GenuineIntel
    CPU family:          6
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:            4
    CPU MHz:             2095.226
    BogoMIPS:            4190.45
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

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

