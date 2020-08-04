# Benchmark result

* Pull request commit: [`035a9426bb8f919a532790f44ab6c5458d2b5f63`](https://github.com/tkf/ThreadsX.jl/commit/035a9426bb8f919a532790f44ab6c5458d2b5f63)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/149> (Run Aqua.test_stale_deps(ThreadsX))

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 Aug 2020 - 17:26
    - Baseline: 4 Aug 2020 - 17:32
* Package commits:
    - Target: 6b2907
    - Baseline: 9c609f
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
| `["findfirst", "0%", "base"]`                                      | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx"]`                                        |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx-seq"]`                                    | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "base"]`                                     | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                                       | 0.77 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx-noterm"]`                                | 0.80 (5%) :white_check_mark: | 0.78 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx-seq"]`                                   |                1.29 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                                       | 0.78 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx-noterm"]`                                | 0.77 (5%) :white_check_mark: |                1.16 (1%) :x: |
| `["findfirst", "20%", "tx-seq"]`                                   |                1.49 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "30%", "base"]`                                     | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                                       | 0.76 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                                | 0.66 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-seq"]`                                   |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                                       | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                                | 0.65 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-seq"]`                                   |                1.29 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                                       | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx-noterm"]`                                | 0.90 (5%) :white_check_mark: |                1.05 (1%) :x: |
| `["findfirst", "50%", "tx-seq"]`                                   |                1.74 (5%) :x: |                   1.00 (1%)  |
| `["foreach", "base", "A .= B .+ B'"]`                              |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Transpose"]`                             |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Matrix"]`                                  | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "man"]`                          |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |            56637.28 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |            59027.38 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |            44073.96 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "Base"]`                                 | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 0.79 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 0.79 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "base"]`                        | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      49406 s          0 s       2434 s      34354 s          0 s
       #2  2095 MHz      57430 s          0 s       3375 s      25105 s          0 s
       
  Memory: 6.764884948730469 GB (1799.74609375 MB free)
  Uptime: 886.0 sec
  Load Avg:  1.29833984375  1.3115234375  0.9072265625
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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      72450 s          0 s       3237 s      45661 s          0 s
       #2  2095 MHz      80922 s          0 s       4049 s      36096 s          0 s
       
  Memory: 6.764884948730469 GB (2146.03515625 MB free)
  Uptime: 1239.0 sec
  Load Avg:  1.251953125  1.31396484375  1.0419921875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 4 Aug 2020 - 17:26
* Package commit: 6b2907
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
| `["findfirst", "0%", "tx"]`                                        |  24.001 μs (5%) |           |  11.98 KiB (1%) |         220 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  20.300 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 190.973 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  87.603 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  58.502 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 163.704 μs (5%) |           |  32.98 KiB (1%) |         608 |
| `["findfirst", "10%", "tx-seq"]`                                   |  88.102 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 179.105 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 108.703 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 164.404 μs (5%) |           |  32.98 KiB (1%) |         611 |
| `["findfirst", "20%", "tx-seq"]`                                   | 175.804 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 177.006 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 151.504 μs (5%) |           |  28.36 KiB (1%) |         526 |
| `["findfirst", "30%", "tx-noterm"]`                                | 178.705 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 263.508 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 406.911 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 204.305 μs (5%) |           |  35.41 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-noterm"]`                                | 217.906 μs (5%) |           |  35.44 KiB (1%) |         658 |
| `["findfirst", "40%", "tx-seq"]`                                   | 351.109 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 452.914 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 272.808 μs (5%) |           |  37.86 KiB (1%) |         708 |
| `["findfirst", "50%", "tx-noterm"]`                                | 320.909 μs (5%) |           |  54.08 KiB (1%) |        1004 |
| `["findfirst", "50%", "tx-seq"]`                                   | 509.314 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 293.308 ms (5%) | 24.418 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 221.618 ms (5%) | 24.220 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   7.068 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.391 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   4.120 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.146 ms (5%) |           |  12.77 KiB (1%) |         125 |
| `["foreach_seq", "base", "Matrix"]`                                | 720.213 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.018 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 725.113 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 627.810 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.146 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 620.611 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  17.400 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  17.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  17.800 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  17.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  49.596 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  56.637 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  59.027 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  44.074 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 910.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 920.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.300 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.300 μs (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.132 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.370 ms (5%) |           |   1.19 MiB (1%) |         534 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 504.609 μs (5%) |           | 965.13 KiB (1%) |        1227 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 518.510 μs (5%) |           |   1.02 MiB (1%) |        1248 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.414 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.385 ms (5%) |           |   1.19 MiB (1%) |         562 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.411 ms (5%) |           |   1.01 MiB (1%) |        2149 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.321 ms (5%) |           |   1.39 MiB (1%) |        2198 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 128.803 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 106.802 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 106.502 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 104.802 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.373 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   3.736 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   2.684 ms (5%) |           |   1.01 MiB (1%) |        2236 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.279 ms (5%) |           |   1.40 MiB (1%) |        2273 |
| `["sort", "reversed", "Base"]`                                     | 598.011 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.285 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 921.417 μs (5%) |           | 998.77 KiB (1%) |        1872 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.450 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["sort", "sorted", "Base"]`                                       | 670.313 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 760.914 μs (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 750.114 μs (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   | 925.017 μs (5%) |           |   1.36 MiB (1%) |        1902 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   8.029 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.160 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.190 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.390 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      49406 s          0 s       2434 s      34354 s          0 s
       #2  2095 MHz      57430 s          0 s       3375 s      25105 s          0 s
       
  Memory: 6.764884948730469 GB (1799.74609375 MB free)
  Uptime: 886.0 sec
  Load Avg:  1.29833984375  1.3115234375  0.9072265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 4 Aug 2020 - 17:32
* Package commit: 9c609f
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
| `["findfirst", "0%", "base"]`                                      |   2.600 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  21.601 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  19.701 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 213.166 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     | 101.705 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  76.404 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 205.711 μs (5%) |           |  42.25 KiB (1%) |         780 |
| `["findfirst", "10%", "tx-seq"]`                                   |  68.103 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 175.309 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 139.507 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 212.310 μs (5%) |           |  28.44 KiB (1%) |         530 |
| `["findfirst", "20%", "tx-seq"]`                                   | 118.106 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 262.816 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 198.512 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 271.617 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 176.211 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 406.922 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 307.117 μs (5%) |           |  35.38 KiB (1%) |         655 |
| `["findfirst", "40%", "tx-noterm"]`                                | 334.418 μs (5%) |           |  35.42 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-seq"]`                                   | 272.315 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 438.025 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 305.017 μs (5%) |           |  37.84 KiB (1%) |         707 |
| `["findfirst", "50%", "tx-noterm"]`                                | 355.121 μs (5%) |           |  51.72 KiB (1%) |         960 |
| `["findfirst", "50%", "tx-seq"]`                                   | 293.117 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 253.755 ms (5%) | 17.727 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 224.341 ms (5%) | 30.337 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   7.248 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.207 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   4.084 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.272 ms (5%) |           |  12.73 KiB (1%) |         123 |
| `["foreach_seq", "base", "Matrix"]`                                | 721.425 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   1.798 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 726.225 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 730.324 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.151 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 625.421 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  17.201 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  17.001 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  18.501 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  17.500 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  43.726 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 900.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 800.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.300 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.300 μs (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.128 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.388 ms (5%) |           |   1.19 MiB (1%) |         534 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 501.221 μs (5%) |           | 965.13 KiB (1%) |        1227 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 517.821 μs (5%) |           |   1.02 MiB (1%) |        1248 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.409 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.959 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.151 ms (5%) |           |   1.01 MiB (1%) |        2147 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.615 ms (5%) |           |   1.39 MiB (1%) |        2197 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 142.306 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 132.006 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 135.006 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 132.806 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.541 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   3.669 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   2.912 ms (5%) |           |   1.01 MiB (1%) |        2237 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.418 ms (5%) |           |   1.40 MiB (1%) |        2272 |
| `["sort", "reversed", "Base"]`                                     | 591.323 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.134 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 799.031 μs (5%) |           | 998.70 KiB (1%) |        1868 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.257 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["sort", "sorted", "Base"]`                                       | 660.725 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 764.928 μs (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 845.332 μs (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   | 893.132 μs (5%) |           |   1.36 MiB (1%) |        1903 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   9.956 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.189 ms (5%) |           |  50.97 KiB (1%) |         881 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.179 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.423 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      72450 s          0 s       3237 s      45661 s          0 s
       #2  2095 MHz      80922 s          0 s       4049 s      36096 s          0 s
       
  Memory: 6.764884948730469 GB (2146.03515625 MB free)
  Uptime: 1239.0 sec
  Load Avg:  1.251953125  1.31396484375  1.0419921875
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
    CPU MHz:             2095.129
    BogoMIPS:            4190.25
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves
    

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
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

