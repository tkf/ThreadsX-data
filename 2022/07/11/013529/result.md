# Benchmark result

* Pull request commit: [`704f44e58691af699204dd721871761ab053e520`](https://github.com/tkf/ThreadsX.jl/commit/704f44e58691af699204dd721871761ab053e520)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 11 Jul 2022 - 01:28
    - Baseline: 11 Jul 2022 - 01:34
* Package commits:
    - Target: c4e839
    - Baseline: 8d4703
* Julia commits:
    - Target: b8708f
    - Baseline: b8708f
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

| ID                                                     | time ratio                   | memory ratio                 |
|--------------------------------------------------------|------------------------------|------------------------------|
| `["findfirst", "0%", "base"]`                          |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                           |                1.11 (5%) :x: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx-seq"]`                       |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "base"]`                         |                1.45 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                           |                   1.00 (5%)  |                1.25 (1%) :x: |
| `["findfirst", "20%", "tx-seq"]`                       |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-seq"]`                       |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "base"]`                         | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-seq"]`                       |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx-seq"]`                       |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Transpose"]`                   |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Vector"]`                      | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]` | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`   | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |

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
Julia Version 1.6.6
Commit b8708f954a (2022-03-28 07:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1031-azure #37~20.04.1-Ubuntu SMP Mon Jun 13 22:51:01 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5117 s          1 s        230 s       5255 s          0 s
       #2  2793 MHz       5953 s          1 s        289 s       4376 s          0 s
       
  Memory: 6.783607482910156 GB (2940.203125 MB free)
  Uptime: 1067.07 sec
  Load Avg:  1.27  1.29  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, icelake-server)
```

### Baseline
```
Julia Version 1.6.6
Commit b8708f954a (2022-03-28 07:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1031-azure #37~20.04.1-Ubuntu SMP Mon Jun 13 22:51:01 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7861 s          1 s        319 s       6223 s          0 s
       #2  2793 MHz       8201 s          1 s        353 s       5862 s          0 s
       
  Memory: 6.783607482910156 GB (3195.4296875 MB free)
  Uptime: 1447.85 sec
  Load Avg:  1.16  1.28  1.03
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 11 Jul 2022 - 1:28
* Package commit: c4e839
* Julia commit: b8708f
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
| `["findfirst", "0%", "base"]`                                        |   2.800 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   4.433 μs (5%) |           |   3.90 KiB (1%) |          47 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 450.800 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  91.536 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       | 126.099 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 129.100 μs (5%) |           |  10.98 KiB (1%) |         146 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 454.100 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     | 126.299 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 252.299 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 150.600 μs (5%) |           |  11.91 KiB (1%) |         162 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 454.300 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 252.599 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 253.500 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 161.000 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 452.700 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 378.800 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 337.600 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 205.500 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 452.300 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 504.799 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 420.600 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 280.700 μs (5%) |           |  16.86 KiB (1%) |         237 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 458.600 μs (5%) |           |  17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                     | 631.000 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 254.228 ms (5%) | 30.879 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 232.833 ms (5%) | 31.028 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |   6.990 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   5.627 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   3.553 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   2.870 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  | 700.499 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   1.810 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 810.899 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 725.200 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 | 970.490 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 700.401 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  20.600 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  20.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  20.500 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  20.500 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            |  80.351 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         |  79.752 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          |  79.648 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           |  79.649 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    |   1.140 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` |   1.130 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   3.212 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   3.200 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 329.032 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 261.036 ms (5%) | 14.715 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.195 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.221 ms (5%) |           |  58.72 KiB (1%) |        1173 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   2.974 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   3.098 ms (5%) |           |   1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 677.900 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 726.200 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   7.971 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   6.348 ms (5%) |           |   1.17 MiB (1%) |         319 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   3.913 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.623 ms (5%) |           |   1.35 MiB (1%) |        1583 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 134.700 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 135.300 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 135.000 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 135.100 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   7.883 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   5.602 ms (5%) |           |   1.17 MiB (1%) |         312 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   3.580 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.575 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 830.800 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.269 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         | 825.100 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.365 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 807.499 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           | 994.801 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           | 826.697 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     |   1.090 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   4.832 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   2.295 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   7.728 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   4.625 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
Julia Version 1.6.6
Commit b8708f954a (2022-03-28 07:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1031-azure #37~20.04.1-Ubuntu SMP Mon Jun 13 22:51:01 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5117 s          1 s        230 s       5255 s          0 s
       #2  2793 MHz       5953 s          1 s        289 s       4376 s          0 s
       
  Memory: 6.783607482910156 GB (2940.203125 MB free)
  Uptime: 1067.07 sec
  Load Avg:  1.27  1.29  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 11 Jul 2022 - 1:34
* Package commit: 8d4703
* Julia commit: b8708f
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
| `["findfirst", "0%", "base"]`                                        |   2.600 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   4.567 μs (5%) |           |   3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 449.600 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  89.655 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       | 126.100 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 116.500 μs (5%) |           |  11.72 KiB (1%) |         155 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 457.300 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     |  84.200 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 174.600 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 150.700 μs (5%) |           |   9.55 KiB (1%) |         130 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 455.300 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 168.700 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 253.700 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 162.700 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 453.300 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 253.000 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 504.600 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 208.400 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 451.100 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 337.000 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 421.800 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 268.200 μs (5%) |           |  16.86 KiB (1%) |         237 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 456.101 μs (5%) |           |  17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                     | 421.100 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 261.060 ms (5%) | 30.470 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 240.768 ms (5%) | 30.161 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |   6.903 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   5.423 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   3.606 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   2.870 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  | 691.200 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   1.765 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 801.900 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 722.500 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 | 845.700 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 802.900 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  20.600 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  20.400 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  20.500 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  20.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            |  80.248 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    |   1.100 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` |   1.100 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   3.200 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   3.200 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 329.402 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 274.287 ms (5%) | 19.081 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.193 ms (5%) |           |  58.67 KiB (1%) |        1172 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.218 ms (5%) |           |  58.78 KiB (1%) |        1173 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   2.978 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   3.193 ms (5%) |           |   1.17 MiB (1%) |         296 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 693.800 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 780.000 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   7.983 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   6.503 ms (5%) |           |   1.17 MiB (1%) |         319 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   3.864 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.903 ms (5%) |           |   1.35 MiB (1%) |        1583 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 137.100 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 135.900 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 136.400 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 136.600 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   7.883 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   5.616 ms (5%) |           |   1.17 MiB (1%) |         312 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   3.584 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.627 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 830.900 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.266 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         | 842.900 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.366 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 811.400 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           | 986.300 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           | 823.100 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     |   1.093 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   4.835 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   2.302 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   7.739 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   4.601 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
Julia Version 1.6.6
Commit b8708f954a (2022-03-28 07:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1031-azure #37~20.04.1-Ubuntu SMP Mon Jun 13 22:51:01 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7861 s          1 s        319 s       6223 s          0 s
       #2  2793 MHz       8201 s          1 s        353 s       5862 s          0 s
       
  Memory: 6.783607482910156 GB (3195.4296875 MB free)
  Uptime: 1447.85 sec
  Load Avg:  1.16  1.28  1.03
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, icelake-server)
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
    Model:                           106
    Model name:                      Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz
    Stepping:                        6
    CPU MHz:                         2793.438
    BogoMIPS:                        5586.87
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       96 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2.5 MiB
    L3 cache:                        48 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :UnknownIntel                                           |
| Model              | Family: 0x06, Model: 0x6a, Stepping: 0x06, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (48, 1280, 49152) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

