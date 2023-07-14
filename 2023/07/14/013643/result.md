# Benchmark result

* Pull request commit: [`b83c74b7bffffd5177da8ce240036fc83e9a3178`](https://github.com/tkf/ThreadsX.jl/commit/b83c74b7bffffd5177da8ce240036fc83e9a3178)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 14 Jul 2023 - 01:28
    - Baseline: 14 Jul 2023 - 01:35
* Package commits:
    - Target: 9aba45
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

| ID                                                     | time ratio                   | memory ratio  |
|--------------------------------------------------------|------------------------------|---------------|
| `["findfirst", "0%", "tx"]`                            |                1.10 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "10%", "base"]`                         |                1.10 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                           | 0.95 (5%) :white_check_mark: | 1.09 (1%) :x: |
| `["findfirst", "10%", "tx-seq"]`                       |                1.12 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                    |                1.08 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "30%", "tx-seq"]`                       |                1.06 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "40%", "base"]`                         | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                           |                1.07 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                           |                   1.05 (5%)  | 1.22 (1%) :x: |
| `["foreach_seq", "base", "Matrix"]`                    |                1.06 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "man"]`           |                1.12 (5%) :x: |    1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                            | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`       |                1.08 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`       |                1.09 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]` |                1.08 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`         |                1.10 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`         |                1.05 (5%) :x: |    1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`       |                1.06 (5%) :x: |    1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]` |                1.07 (5%) :x: |    1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`         |                1.08 (5%) :x: |    1.00 (1%)  |
| `["sort", "reversed", "Base"]`                         |                1.08 (5%) :x: |    1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.QuickSort"]`             |                1.10 (5%) :x: |    1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "base"]`            |                1.13 (5%) :x: |    1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "tx"]`              |                1.09 (5%) :x: |    1.00 (1%)  |

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
  uname: Linux 5.15.0-1041-azure #48-Ubuntu SMP Tue Jun 20 20:34:08 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       5396 s          0 s        312 s       4039 s          0 s
       #2  2294 MHz       6802 s          0 s        390 s       2560 s          0 s
       
  Memory: 6.769481658935547 GB (2604.171875 MB free)
  Uptime: 985.86 sec
  Load Avg:  1.25  1.31  0.96
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.6.7
Commit 3b76b25b64 (2022-07-19 15:11 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1041-azure #48-Ubuntu SMP Tue Jun 20 20:34:08 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       8385 s          0 s        434 s       5179 s          0 s
       #2  2294 MHz       9179 s          0 s        484 s       4343 s          0 s
       
  Memory: 6.769481658935547 GB (3090.4375 MB free)
  Uptime: 1412.86 sec
  Load Avg:  1.17  1.3  1.09
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 14 Jul 2023 - 1:28
* Package commit: 9aba45
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
| `["findfirst", "0%", "base"]`                                        |   2.999 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   5.667 μs (5%) |           |   3.90 KiB (1%) |          47 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 379.600 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  90.319 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       |  67.199 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 137.400 μs (5%) |           |  10.28 KiB (1%) |         139 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 377.799 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     |  66.600 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 117.900 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 144.099 μs (5%) |           |   9.58 KiB (1%) |         132 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 402.199 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 121.400 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 176.800 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 141.200 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 396.800 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 186.400 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 234.699 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 187.396 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 384.499 μs (5%) |           |  17.44 KiB (1%) |         252 |
| `["findfirst", "40%", "tx-seq"]`                                     | 234.599 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 293.100 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 261.299 μs (5%) |           |  16.86 KiB (1%) |         237 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 393.800 μs (5%) |           |  17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                     | 297.500 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 494.146 ms (5%) | 43.270 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 324.079 ms (5%) | 43.347 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |  20.600 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |  11.055 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   9.153 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   5.358 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  | 593.700 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   1.871 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 561.298 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 581.299 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 | 936.196 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 561.398 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  22.500 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  22.900 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  20.900 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  21.800 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            | 102.455 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         | 103.842 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          | 112.242 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           | 103.939 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    |   2.133 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` |   2.400 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   2.678 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   2.833 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 285.362 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 276.243 ms (5%) | 23.258 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.260 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.004 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.300 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   2.375 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   2.862 ms (5%) |           |   1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     |   1.089 ms (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               |   1.155 ms (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   5.700 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   5.550 ms (5%) |           |   1.17 MiB (1%) |         319 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   3.889 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.781 ms (5%) |           |   1.35 MiB (1%) |        1582 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 126.300 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 135.000 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 136.400 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 138.700 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   5.654 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   4.538 ms (5%) |           |   1.17 MiB (1%) |         312 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   3.241 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   3.891 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 702.199 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.235 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         |   1.003 ms (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.436 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 611.299 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           | 980.299 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           |   1.111 ms (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     |   1.193 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   5.599 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   2.651 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   7.371 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   4.523 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
  uname: Linux 5.15.0-1041-azure #48-Ubuntu SMP Tue Jun 20 20:34:08 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       5396 s          0 s        312 s       4039 s          0 s
       #2  2294 MHz       6802 s          0 s        390 s       2560 s          0 s
       
  Memory: 6.769481658935547 GB (2604.171875 MB free)
  Uptime: 985.86 sec
  Load Avg:  1.25  1.31  0.96
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 14 Jul 2023 - 1:35
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
| `["findfirst", "0%", "base"]`                                        |   2.900 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   5.150 μs (5%) |           |   3.90 KiB (1%) |          47 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 390.200 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  89.149 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       |  61.300 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 144.700 μs (5%) |           |   9.47 KiB (1%) |         127 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 386.000 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     |  59.500 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 121.800 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 143.599 μs (5%) |           |   9.56 KiB (1%) |         131 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 396.099 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 118.200 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 176.400 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 139.300 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 366.999 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 176.299 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 255.900 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 175.700 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 381.999 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 234.800 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 293.100 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 249.399 μs (5%) |           |  13.83 KiB (1%) |         199 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 379.699 μs (5%) |           |  17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                     | 293.000 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 475.482 ms (5%) | 40.177 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 309.171 ms (5%) | 39.584 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |  20.974 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |  11.076 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   8.984 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   5.442 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  | 560.997 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   1.927 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 561.097 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 564.698 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 | 932.596 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 561.098 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  20.000 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  20.200 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  20.000 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  21.600 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            | 104.588 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         |  99.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          |  99.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           |  99.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    |   1.600 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` |   1.600 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   2.500 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   2.500 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 293.450 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 307.189 ms (5%) | 28.383 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.216 ms (5%) |           |  58.72 KiB (1%) |        1174 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.002 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.325 ms (5%) |           |  58.72 KiB (1%) |        1178 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   2.289 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   2.654 ms (5%) |           |   1.17 MiB (1%) |         296 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     |   1.002 ms (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               |   1.072 ms (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   5.587 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   5.038 ms (5%) |           |   1.17 MiB (1%) |         318 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   3.695 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.713 ms (5%) |           |   1.35 MiB (1%) |        1582 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 126.000 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 128.700 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 128.900 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 129.400 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   5.474 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   4.194 ms (5%) |           |   1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   3.140 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   3.770 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 652.897 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.247 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         |   1.024 ms (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.512 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 606.198 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           | 940.194 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           |   1.012 ms (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     |   1.183 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   4.971 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   2.435 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   7.142 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   4.328 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
  uname: Linux 5.15.0-1041-azure #48-Ubuntu SMP Tue Jun 20 20:34:08 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       8385 s          0 s        434 s       5179 s          0 s
       #2  2294 MHz       9179 s          0 s        484 s       4343 s          0 s
       
  Memory: 6.769481658935547 GB (3090.4375 MB free)
  Uptime: 1412.86 sec
  Load Avg:  1.17  1.3  1.09
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
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    CPU family:                      6
    Model:                           79
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        1
    BogoMIPS:                        4589.36
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        512 KiB (2 instances)
    L3 cache:                        50 MiB (1 instance)
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

