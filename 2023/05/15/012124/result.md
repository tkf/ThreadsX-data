# Benchmark result

* Pull request commit: [`e0211806e4ea90862415c08eec59af47f7f9bff6`](https://github.com/tkf/ThreadsX.jl/commit/e0211806e4ea90862415c08eec59af47f7f9bff6)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 15 May 2023 - 01:14
    - Baseline: 15 May 2023 - 01:20
* Package commits:
    - Target: 2e3f91
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
| `["findfirst", "0%", "base"]`                          |                1.08 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "0%", "tx-noterm"]`                     |                1.49 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "10%", "base"]`                         | 0.67 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                           |                1.94 (5%) :x: | 1.13 (1%) :x: |
| `["findfirst", "10%", "tx-noterm"]`                    |                1.48 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                           |                1.44 (5%) :x: | 1.27 (1%) :x: |
| `["findfirst", "20%", "tx-noterm"]`                    |                1.47 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "30%", "base"]`                         |                1.49 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                           |                1.45 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                    |                1.47 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                           |                1.42 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                    |                1.47 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "50%", "base"]`                         |                1.50 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                           |                1.36 (5%) :x: | 1.04 (1%) :x: |
| `["findfirst", "50%", "tx-noterm"]`                    |                1.48 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`       | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]` | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`   | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.MergeSort"]`             |                1.08 (5%) :x: |    1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`       |                1.07 (5%) :x: |    1.00 (1%)  |

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
  uname: Linux 5.15.0-1037-azure #44-Ubuntu SMP Thu Apr 20 13:19:31 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       6237 s          0 s        233 s       3993 s          0 s
       #2  2793 MHz       5239 s          0 s        294 s       4939 s          0 s
       
  Memory: 6.7812042236328125 GB (2849.1484375 MB free)
  Uptime: 1053.56 sec
  Load Avg:  1.15  1.26  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, icelake-server)
```

### Baseline
```
Julia Version 1.6.7
Commit 3b76b25b64 (2022-07-19 15:11 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1037-azure #44-Ubuntu SMP Thu Apr 20 13:19:31 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       8499 s          0 s        285 s       5530 s          0 s
       #2  2793 MHz       8013 s          0 s        397 s       5912 s          0 s
       
  Memory: 6.7812042236328125 GB (3079.1640625 MB free)
  Uptime: 1439.9 sec
  Load Avg:  1.28  1.33  1.07
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 15 May 2023 - 1:14
* Package commit: 2e3f91
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
| `["findfirst", "0%", "base"]`                                        |   2.800 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   4.486 μs (5%) |           |   3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 671.203 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  88.820 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       |  84.100 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 199.301 μs (5%) |           |  13.25 KiB (1%) |         176 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 670.903 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     |  84.200 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 170.101 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 217.001 μs (5%) |           |  14.11 KiB (1%) |         187 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 669.603 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 168.801 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 378.401 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 233.701 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 661.003 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 252.801 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 504.602 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 296.701 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 661.403 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 336.901 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 630.702 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 392.802 μs (5%) |           |  16.89 KiB (1%) |         238 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 669.402 μs (5%) |           |  17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                     | 420.901 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 264.118 ms (5%) | 37.217 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 241.415 ms (5%) | 37.254 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |   7.349 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   5.653 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   3.590 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   2.896 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  | 691.504 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   1.798 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 803.205 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 718.104 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 | 961.406 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 691.404 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  20.600 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  20.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  20.400 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  20.500 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            |  80.373 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         |  80.062 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          |  80.270 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           |  79.959 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    |   1.130 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` |   1.140 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   3.212 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   3.212 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 332.790 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 274.732 ms (5%) | 19.032 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.206 ms (5%) |           |  58.67 KiB (1%) |        1172 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.250 ms (5%) |           |  58.89 KiB (1%) |        1177 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   2.972 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   3.044 ms (5%) |           |   1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 682.104 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 714.604 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   7.886 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   6.353 ms (5%) |           |   1.17 MiB (1%) |         317 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   3.857 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.565 ms (5%) |           |   1.35 MiB (1%) |        1582 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 139.101 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 131.401 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 131.401 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 131.101 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   7.746 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   5.494 ms (5%) |           |   1.17 MiB (1%) |         312 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   3.580 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.435 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 835.705 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.217 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         | 820.004 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.318 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 819.905 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           | 927.605 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           | 806.705 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     |   1.040 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   4.872 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   2.320 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   7.859 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   4.583 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
  uname: Linux 5.15.0-1037-azure #44-Ubuntu SMP Thu Apr 20 13:19:31 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       6237 s          0 s        233 s       3993 s          0 s
       #2  2793 MHz       5239 s          0 s        294 s       4939 s          0 s
       
  Memory: 6.7812042236328125 GB (2849.1484375 MB free)
  Uptime: 1053.56 sec
  Load Avg:  1.15  1.26  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 15 May 2023 - 1:20
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
| `["findfirst", "0%", "base"]`                                        |   2.600 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   4.500 μs (5%) |           |   3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 451.103 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  91.537 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       | 126.100 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 102.900 μs (5%) |           |  11.69 KiB (1%) |         154 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 451.903 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     |  84.200 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 174.301 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 150.601 μs (5%) |           |  11.14 KiB (1%) |         152 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 456.302 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 168.901 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 253.601 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 161.701 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 449.803 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 252.702 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 504.603 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 209.401 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 449.303 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 336.902 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 421.803 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 289.802 μs (5%) |           |  16.17 KiB (1%) |         230 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 452.203 μs (5%) |           |  17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                     | 421.002 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 270.266 ms (5%) | 35.630 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 246.042 ms (5%) | 36.165 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |   7.113 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   5.759 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   3.705 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   2.886 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  | 691.205 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   1.767 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 803.106 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 718.004 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 | 954.806 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 691.404 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  20.601 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  20.100 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  20.400 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  20.500 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            |  80.269 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    |   1.100 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` |   1.100 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   3.200 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   3.200 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 329.941 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 287.636 ms (5%) | 20.610 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.212 ms (5%) |           |  58.67 KiB (1%) |        1172 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.245 ms (5%) |           |  59.00 KiB (1%) |        1176 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   2.975 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   3.217 ms (5%) |           |   1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 683.405 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 778.205 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   7.987 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   6.510 ms (5%) |           |   1.17 MiB (1%) |         319 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   3.902 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   5.110 ms (5%) |           |   1.35 MiB (1%) |        1582 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 139.501 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 133.601 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 132.301 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 133.701 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   7.757 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   5.320 ms (5%) |           |   1.17 MiB (1%) |         312 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   3.584 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.250 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 840.505 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.169 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         | 832.606 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.264 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 820.906 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           | 862.406 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           | 813.305 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     | 968.307 μs (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   4.839 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   2.328 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   7.751 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   4.547 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
  uname: Linux 5.15.0-1037-azure #44-Ubuntu SMP Thu Apr 20 13:19:31 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       8499 s          0 s        285 s       5530 s          0 s
       #2  2793 MHz       8013 s          0 s        397 s       5912 s          0 s
       
  Memory: 6.7812042236328125 GB (3079.1640625 MB free)
  Uptime: 1439.9 sec
  Load Avg:  1.28  1.33  1.07
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
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz
    CPU family:                      6
    Model:                           106
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        6
    BogoMIPS:                        5586.87
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       96 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2.5 MiB (2 instances)
    L3 cache:                        48 MiB (1 instance)
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

