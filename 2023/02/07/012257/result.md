# Benchmark result

* Pull request commit: [`34201ac937140d5589c1af73fa591566630a24a1`](https://github.com/tkf/ThreadsX.jl/commit/34201ac937140d5589c1af73fa591566630a24a1)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 7 Feb 2023 - 01:15
    - Baseline: 7 Feb 2023 - 01:22
* Package commits:
    - Target: e89f6c
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
| `["findfirst", "0%", "tx"]`                            |                1.09 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "0%", "tx-noterm"]`                     | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                           | 0.77 (5%) :white_check_mark: | 1.20 (1%) :x: |
| `["findfirst", "10%", "tx-noterm"]`                    | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                           | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "20%", "tx-noterm"]`                    | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                    | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                           | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                    | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                           | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "50%", "tx-noterm"]`                    | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach", "base", "A .= B .+ B'"]`                  | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach", "base", "A .= B .+ C"]`                   | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ B'"]`             |                1.12 (5%) :x: |    1.00 (1%)  |
| `["foreach", "tx", "A .= B .+ B'"]`                    |                1.12 (5%) :x: |    1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                            | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "Base"]`                     |                1.19 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`       |                1.15 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]` |                1.12 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "Base"]`                       |                1.08 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`         |                1.09 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`   |                1.10 (5%) :x: |    1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`         |                1.08 (5%) :x: |    1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`   |                1.12 (5%) :x: |    1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.MergeSort"]`           |                1.12 (5%) :x: |    1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`     |                1.08 (5%) :x: |    1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.MergeSort"]`             |                1.18 (5%) :x: |    1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`       |                1.15 (5%) :x: |    1.00 (1%)  |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1031-azure #38-Ubuntu SMP Mon Jan 9 12:49:59 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       6138 s          0 s        290 s       4393 s          0 s
       #2  2593 MHz       5565 s          0 s        322 s       4932 s          0 s
       
  Memory: 6.781219482421875 GB (2616.1875 MB free)
  Uptime: 1090.47 sec
  Load Avg:  1.29  1.28  0.92
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.6.7
Commit 3b76b25b64 (2022-07-19 15:11 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1031-azure #38-Ubuntu SMP Mon Jan 9 12:49:59 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       9657 s          0 s        408 s       4936 s          0 s
       #2  2593 MHz       7438 s          0 s        375 s       7174 s          0 s
       
  Memory: 6.781219482421875 GB (2909.33984375 MB free)
  Uptime: 1509.37 sec
  Load Avg:  1.19  1.28  1.05
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 7 Feb 2023 - 1:15
* Package commit: e89f6c
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
| `["findfirst", "0%", "base"]`                                        |   3.000 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   4.650 μs (5%) |           |   3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 568.307 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  94.955 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       | 175.200 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 165.401 μs (5%) |           |  13.23 KiB (1%) |         175 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 568.906 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     | 105.201 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 350.404 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 189.602 μs (5%) |           |  11.91 KiB (1%) |         162 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 564.306 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 210.603 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 525.605 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 201.602 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 560.899 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 315.697 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 700.808 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 258.503 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 565.807 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 420.806 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 875.909 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 338.305 μs (5%) |           |  16.89 KiB (1%) |         238 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 569.706 μs (5%) |           |  17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                     | 525.905 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 319.862 ms (5%) | 40.185 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 258.730 ms (5%) | 40.439 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |  11.468 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   8.419 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   5.689 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   4.255 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  |   1.003 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   2.561 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 750.615 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    |   1.011 ms (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 |   1.170 ms (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 750.315 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  22.200 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  21.701 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  21.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  21.700 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            |  93.909 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         |  94.236 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          |  95.590 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           |  94.236 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    |   1.090 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` |   1.090 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   2.767 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   2.767 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 288.739 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 254.066 ms (5%) | 18.655 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.200 ms (5%) |           |  58.72 KiB (1%) |        1173 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.236 ms (5%) |           |  58.94 KiB (1%) |        1180 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   3.088 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   3.273 ms (5%) |           |   1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 729.557 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 823.120 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   7.030 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   5.837 ms (5%) |           |   1.17 MiB (1%) |         317 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   3.591 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.416 ms (5%) |           |   1.35 MiB (1%) |        1582 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 131.500 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 127.901 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 129.302 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 129.201 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   7.079 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   5.020 ms (5%) |           |   1.17 MiB (1%) |         312 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   3.398 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.132 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 792.109 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.338 ms (5%) |           |   1.17 MiB (1%) |         269 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         | 914.314 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.429 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 734.514 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           |   1.112 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           | 875.217 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     |   1.203 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   5.020 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   2.273 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   7.394 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   4.299 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1031-azure #38-Ubuntu SMP Mon Jan 9 12:49:59 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       6138 s          0 s        290 s       4393 s          0 s
       #2  2593 MHz       5565 s          0 s        322 s       4932 s          0 s
       
  Memory: 6.781219482421875 GB (2616.1875 MB free)
  Uptime: 1090.47 sec
  Load Avg:  1.29  1.28  0.92
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 7 Feb 2023 - 1:22
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
| `["findfirst", "0%", "base"]`                                        |   3.000 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   4.283 μs (5%) |           |   3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 615.310 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  96.426 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       | 175.202 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 214.903 μs (5%) |           |  11.03 KiB (1%) |         149 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 629.012 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     | 105.301 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 350.707 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 225.103 μs (5%) |           |  11.89 KiB (1%) |         162 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 632.009 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 211.103 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 526.208 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 206.203 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 628.710 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 315.905 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 701.507 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 282.601 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 637.610 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 421.307 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 876.814 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 384.406 μs (5%) |           |  16.89 KiB (1%) |         238 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 630.609 μs (5%) |           |  17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                     | 526.408 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 344.907 ms (5%) | 38.793 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 273.311 ms (5%) | 38.918 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |  10.275 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   8.659 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   5.094 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   4.364 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  |   1.003 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   2.598 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 761.109 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    |   1.011 ms (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 |   1.169 ms (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 752.508 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  21.400 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  21.100 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  20.901 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  21.100 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            |  93.909 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    |   1.100 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` |   1.100 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   2.700 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   2.700 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 291.019 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 282.828 ms (5%) | 24.423 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.191 ms (5%) |           |  58.72 KiB (1%) |        1173 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.278 ms (5%) |           |  58.77 KiB (1%) |        1174 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   2.601 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   2.852 ms (5%) |           |   1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 725.310 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 737.509 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   6.482 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   5.349 ms (5%) |           |   1.17 MiB (1%) |         319 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   3.583 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.019 ms (5%) |           |   1.35 MiB (1%) |        1582 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 133.702 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 131.902 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 135.601 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 130.502 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   7.092 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   4.661 ms (5%) |           |   1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   3.378 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   3.695 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 794.711 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.200 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         | 912.412 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.317 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 738.909 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           | 946.113 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           | 903.503 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     |   1.048 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   5.023 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   2.272 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   7.348 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   4.298 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1031-azure #38-Ubuntu SMP Mon Jan 9 12:49:59 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       9657 s          0 s        408 s       4936 s          0 s
       #2  2593 MHz       7438 s          0 s        375 s       7174 s          0 s
       
  Memory: 6.781219482421875 GB (2909.33984375 MB free)
  Uptime: 1509.37 sec
  Load Avg:  1.19  1.28  1.05
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
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    CPU family:                      6
    Model:                           85
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        7
    BogoMIPS:                        5187.81
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2 MiB (2 instances)
    L3 cache:                        35.8 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

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

