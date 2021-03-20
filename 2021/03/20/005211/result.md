# Benchmark result

* Pull request commit: [`b404f77dce9c37b2fe22cf98403b41fdf6990a9e`](https://github.com/tkf/ThreadsX.jl/commit/b404f77dce9c37b2fe22cf98403b41fdf6990a9e)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 20 Mar 2021 - 00:43
    - Baseline: 20 Mar 2021 - 00:51
* Package commits:
    - Target: da358c
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
| `["findfirst", "0%", "base"]`                                      | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx"]`                                        | 0.85 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["findfirst", "0%", "tx-noterm"]`                                 |               17.66 (5%) :x: |                2.06 (1%) :x: |
| `["findfirst", "0%", "tx-seq"]`                                    | 0.71 (5%) :white_check_mark: | 0.71 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx"]`                                       |                2.50 (5%) :x: |                1.62 (1%) :x: |
| `["findfirst", "10%", "tx-noterm"]`                                |                2.03 (5%) :x: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx-seq"]`                                   |                   0.97 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "20%", "tx"]`                                       |                1.44 (5%) :x: |                1.09 (1%) :x: |
| `["findfirst", "20%", "tx-noterm"]`                                |                1.87 (5%) :x: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "20%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "30%", "base"]`                                     | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                                       |                1.08 (5%) :x: | 0.99 (1%) :white_check_mark: |
| `["findfirst", "30%", "tx-noterm"]`                                |                1.79 (5%) :x: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "30%", "tx-seq"]`                                   |                   0.97 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "40%", "base"]`                                     | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                                       |                   1.03 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx-noterm"]`                                |                1.54 (5%) :x: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx-seq"]`                                   | 0.94 (5%) :white_check_mark: | 0.72 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx"]`                                       |                1.10 (5%) :x: |                1.05 (1%) :x: |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.19 (5%) :x: | 0.62 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx-seq"]`                                   | 0.94 (5%) :white_check_mark: | 0.72 (1%) :white_check_mark: |
| `["foreach_seq_double", "cartesian", "man"]`                       |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   |                   1.02 (5%)  | 0.59 (1%) :white_check_mark: |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   |                   1.01 (5%)  | 0.59 (1%) :white_check_mark: |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             |                1.08 (5%) :x: | 0.59 (1%) :white_check_mark: |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |                   1.00 (5%)  | 0.55 (1%) :white_check_mark: |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |                   0.98 (5%)  | 0.98 (1%) :white_check_mark: |

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
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      51150 s         19 s       2570 s      65132 s          0 s
       #2  2294 MHz      82482 s          6 s       3697 s      32377 s          0 s
       
  Memory: 6.7913818359375 GB (2445.94921875 MB free)
  Uptime: 1204.0 sec
  Load Avg:  1.35595703125  1.41943359375  1.01123046875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      78544 s         19 s       3466 s      81647 s          0 s
       #2  2294 MHz     112570 s          6 s       4769 s      46068 s          0 s
       
  Memory: 6.7913818359375 GB (2617.03125 MB free)
  Uptime: 1654.0 sec
  Load Avg:  1.27587890625  1.34716796875  1.11865234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 20 Mar 2021 - 0:43
* Package commit: da358c
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
| `["findfirst", "0%", "tx"]`                                        |  23.600 μs (5%) |           |  11.77 KiB (1%) |         218 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 386.703 μs (5%) |           |  24.70 KiB (1%) |         245 |
| `["findfirst", "0%", "tx-seq"]`                                    | 166.304 ns (5%) |           |  400 bytes (1%) |          13 |
| `["findfirst", "10%", "base"]`                                     |  65.101 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       | 195.601 μs (5%) |           |  23.42 KiB (1%) |         439 |
| `["findfirst", "10%", "tx-noterm"]`                                | 388.502 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "10%", "tx-seq"]`                                   |  63.100 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "20%", "base"]`                                     | 124.900 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 202.401 μs (5%) |           |  23.44 KiB (1%) |         440 |
| `["findfirst", "20%", "tx-noterm"]`                                | 384.102 μs (5%) |           |  24.80 KiB (1%) |         251 |
| `["findfirst", "20%", "tx-seq"]`                                   | 125.601 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "30%", "base"]`                                     | 177.002 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 202.202 μs (5%) |           |  28.05 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 404.103 μs (5%) |           |  24.80 KiB (1%) |         251 |
| `["findfirst", "30%", "tx-seq"]`                                   | 186.701 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "40%", "base"]`                                     | 235.002 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 266.602 μs (5%) |           |  35.02 KiB (1%) |         654 |
| `["findfirst", "40%", "tx-noterm"]`                                | 399.302 μs (5%) |           |  24.80 KiB (1%) |         251 |
| `["findfirst", "40%", "tx-seq"]`                                   | 234.902 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "50%", "base"]`                                     | 301.602 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 326.102 μs (5%) |           |  39.81 KiB (1%) |         752 |
| `["findfirst", "50%", "tx-noterm"]`                                | 389.802 μs (5%) |           |  24.88 KiB (1%) |         256 |
| `["findfirst", "50%", "tx-seq"]`                                   | 302.002 μs (5%) |           |  416 bytes (1%) |          14 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 435.535 ms (5%) | 34.405 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 268.573 ms (5%) | 35.982 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  20.552 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |  10.914 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   9.667 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   5.517 ms (5%) |           |  12.78 KiB (1%) |         126 |
| `["foreach_seq", "base", "Matrix"]`                                | 577.303 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.067 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 611.804 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 597.804 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               | 935.306 μs (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 593.703 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  23.600 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  22.800 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  22.400 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  21.700 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          | 104.090 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 104.995 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 105.281 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 104.269 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   2.122 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   2.122 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.800 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.856 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 293.580 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 198.371 ms (5%) |  4.692 ms | 166.54 MiB (1%) |     2016662 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.190 ms (5%) |           |  58.55 KiB (1%) |        1105 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.332 ms (5%) |           |  58.72 KiB (1%) |        1108 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.285 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.711 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   |   1.560 ms (5%) |           | 965.09 KiB (1%) |        1225 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |   1.641 ms (5%) |           |   1.02 MiB (1%) |        1244 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.930 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.952 ms (5%) |           |   1.19 MiB (1%) |         563 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   5.117 ms (5%) |           |   1.01 MiB (1%) |        2147 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   6.082 ms (5%) |           |   1.39 MiB (1%) |        2194 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 134.401 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 135.601 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 140.801 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 141.401 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.779 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.136 ms (5%) |           |   1.19 MiB (1%) |         548 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   4.294 ms (5%) |           |   1.01 MiB (1%) |        2229 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.965 ms (5%) |           |   1.39 MiB (1%) |        2266 |
| `["sort", "reversed", "Base"]`                                     | 696.204 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.265 ms (5%) |           |   1.18 MiB (1%) |         430 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.136 ms (5%) |           | 998.42 KiB (1%) |        1867 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.562 ms (5%) |           |   1.36 MiB (1%) |        1897 |
| `["sort", "sorted", "Base"]`                                       | 661.804 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 887.405 μs (5%) |           |   1.18 MiB (1%) |         425 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |   1.184 ms (5%) |           | 998.42 KiB (1%) |        1867 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.309 ms (5%) |           |   1.36 MiB (1%) |        1897 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   9.491 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   5.027 ms (5%) |           |  28.06 KiB (1%) |         368 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.711 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.305 ms (5%) |           |   1.05 MiB (1%) |         672 |

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
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      51150 s         19 s       2570 s      65132 s          0 s
       #2  2294 MHz      82482 s          6 s       3697 s      32377 s          0 s
       
  Memory: 6.7913818359375 GB (2445.94921875 MB free)
  Uptime: 1204.0 sec
  Load Avg:  1.35595703125  1.41943359375  1.01123046875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 20 Mar 2021 - 0:51
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
| `["findfirst", "0%", "base"]`                                      |   3.500 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  27.800 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  21.900 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 232.971 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  63.100 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  78.301 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 191.002 μs (5%) |           |  35.39 KiB (1%) |         658 |
| `["findfirst", "10%", "tx-seq"]`                                   |  65.101 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 124.801 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 140.201 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 205.702 μs (5%) |           |  28.42 KiB (1%) |         529 |
| `["findfirst", "20%", "tx-seq"]`                                   | 125.301 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 192.401 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 186.802 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 226.102 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 192.600 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 248.501 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 258.502 μs (5%) |           |  35.39 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-noterm"]`                                | 259.501 μs (5%) |           |  35.44 KiB (1%) |         658 |
| `["findfirst", "40%", "tx-seq"]`                                   | 248.702 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 310.403 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 295.201 μs (5%) |           |  37.83 KiB (1%) |         706 |
| `["findfirst", "50%", "tx-noterm"]`                                | 326.902 μs (5%) |           |  40.23 KiB (1%) |         755 |
| `["findfirst", "50%", "tx-seq"]`                                   | 320.000 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 442.913 ms (5%) | 31.365 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 265.449 ms (5%) | 30.962 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  20.963 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |  10.825 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   9.496 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   5.546 ms (5%) |           |  12.75 KiB (1%) |         124 |
| `["foreach_seq", "base", "Matrix"]`                                | 593.903 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.007 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 630.604 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 580.303 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               | 937.706 μs (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 611.704 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  21.900 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  22.900 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  22.100 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  22.200 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          | 103.865 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.800 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.800 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.800 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.900 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 296.429 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 201.763 ms (5%) |  5.404 ms | 165.97 MiB (1%) |     2016651 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.194 ms (5%) |           |  58.86 KiB (1%) |        1112 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.305 ms (5%) |           |  59.13 KiB (1%) |        1116 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.353 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.744 ms (5%) |           |   1.19 MiB (1%) |         533 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   |   1.574 ms (5%) |           | 965.09 KiB (1%) |        1225 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |   1.659 ms (5%) |           |   1.02 MiB (1%) |        1246 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.916 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.004 ms (5%) |           |   1.19 MiB (1%) |         563 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   5.185 ms (5%) |           |   1.01 MiB (1%) |        2146 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   6.011 ms (5%) |           |   1.39 MiB (1%) |        2195 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 129.801 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 132.801 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 139.201 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 131.200 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.669 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.304 ms (5%) |           |   1.19 MiB (1%) |         553 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   4.222 ms (5%) |           |   1.01 MiB (1%) |        2237 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.016 ms (5%) |           |   1.40 MiB (1%) |        2270 |
| `["sort", "reversed", "Base"]`                                     | 696.004 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.248 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.168 ms (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.629 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["sort", "sorted", "Base"]`                                       | 644.903 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 906.604 μs (5%) |           |   1.18 MiB (1%) |         430 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |   1.216 ms (5%) |           | 998.77 KiB (1%) |        1872 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.330 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   9.377 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   5.003 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.613 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.410 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      78544 s         19 s       3466 s      81647 s          0 s
       #2  2294 MHz     112570 s          6 s       4769 s      46068 s          0 s
       
  Memory: 6.7913818359375 GB (2617.03125 MB free)
  Uptime: 1654.0 sec
  Load Avg:  1.27587890625  1.34716796875  1.11865234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
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
    Vulnerability Itlb multihit:     KVM: Vulnerable
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

