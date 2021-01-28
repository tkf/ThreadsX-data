# Benchmark result

* Pull request commit: [`2c1bde9480385ba6bb98efe01a80045a279ac47d`](https://github.com/tkf/ThreadsX.jl/commit/2c1bde9480385ba6bb98efe01a80045a279ac47d)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 28 Jan 2021 - 00:46
    - Baseline: 28 Jan 2021 - 00:53
* Package commits:
    - Target: b41820
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
| `["findfirst", "0%", "tx"]`                                        |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                                       | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx-noterm"]`                                |                1.17 (5%) :x: |                1.11 (1%) :x: |
| `["findfirst", "20%", "base"]`                                     | 0.82 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx-noterm"]`                                |                   0.99 (5%)  |                1.17 (1%) :x: |
| `["findfirst", "20%", "tx-seq"]`                                   | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                                | 0.86 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx-noterm"]`                                |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Matrix"]`                                | 0.75 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Vector"]`                                  |                1.36 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |            51065.99 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |            52839.76 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |            51067.01 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "collatz", "base"]`                                      | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                                        | 0.91 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["sort", "reversed", "Base"]`                                     | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      69861 s         13 s       2759 s      27683 s          0 s
       #2  2593 MHz      51840 s          8 s       2477 s      46878 s          0 s
       
  Memory: 6.791378021240234 GB (2544.9296875 MB free)
  Uptime: 1022.0 sec
  Load Avg:  1.25  1.30810546875  0.9560546875
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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      90926 s         13 s       3220 s      47420 s          0 s
       #2  2593 MHz      84180 s          8 s       3471 s      54765 s          0 s
       
  Memory: 6.791378021240234 GB (2931.5546875 MB free)
  Uptime: 1435.0 sec
  Load Avg:  1.29833984375  1.35693359375  1.1025390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 28 Jan 2021 - 0:46
* Package commit: b41820
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
| `["findfirst", "0%", "base"]`                                      |   3.700 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  24.301 μs (5%) |           |  11.98 KiB (1%) |         220 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  20.800 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 235.354 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     | 105.401 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  57.901 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 176.902 μs (5%) |           |  46.86 KiB (1%) |         862 |
| `["findfirst", "10%", "tx-seq"]`                                   |  71.501 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 180.903 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 118.601 μs (5%) |           |  21.41 KiB (1%) |         398 |
| `["findfirst", "20%", "tx-noterm"]`                                | 186.602 μs (5%) |           |  33.09 KiB (1%) |         615 |
| `["findfirst", "20%", "tx-seq"]`                                   | 125.801 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 222.103 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 155.402 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 179.102 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 220.303 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 431.005 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 235.603 μs (5%) |           |  35.36 KiB (1%) |         654 |
| `["findfirst", "40%", "tx-noterm"]`                                | 257.403 μs (5%) |           |  35.45 KiB (1%) |         659 |
| `["findfirst", "40%", "tx-seq"]`                                   | 294.703 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 536.507 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 270.704 μs (5%) |           |  37.81 KiB (1%) |         705 |
| `["findfirst", "50%", "tx-noterm"]`                                | 331.505 μs (5%) |           |  54.05 KiB (1%) |        1002 |
| `["findfirst", "50%", "tx-seq"]`                                   | 364.804 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 287.845 ms (5%) | 30.308 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 220.956 ms (5%) | 30.658 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  10.218 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   7.975 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   5.454 ms (5%) |           |  25.92 KiB (1%) |         359 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   4.032 ms (5%) |           |  12.77 KiB (1%) |         125 |
| `["foreach_seq", "base", "Matrix"]`                                | 755.910 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.094 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 755.409 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  |   1.021 ms (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.201 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  |   1.013 ms (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  20.500 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  20.000 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  21.800 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  20.200 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  53.144 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  51.066 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  52.840 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  51.067 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.070 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.070 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.767 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.767 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 308.107 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 188.360 ms (5%) |  4.626 ms | 155.50 MiB (1%) |     2016666 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.170 ms (5%) |           |  59.58 KiB (1%) |        1122 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.274 ms (5%) |           |  59.59 KiB (1%) |        1121 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.600 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.873 ms (5%) |           |   1.19 MiB (1%) |         536 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 609.107 μs (5%) |           | 965.11 KiB (1%) |        1226 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 638.409 μs (5%) |           |   1.02 MiB (1%) |        1247 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.470 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.411 ms (5%) |           |   1.19 MiB (1%) |         563 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.573 ms (5%) |           |   1.01 MiB (1%) |        2149 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.236 ms (5%) |           |   1.39 MiB (1%) |        2195 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 134.902 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 125.601 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 126.202 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 125.502 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   7.330 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.766 ms (5%) |           |   1.19 MiB (1%) |         555 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.511 ms (5%) |           |   1.01 MiB (1%) |        2237 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.191 ms (5%) |           |   1.40 MiB (1%) |        2269 |
| `["sort", "reversed", "Base"]`                                     | 828.111 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.260 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 943.313 μs (5%) |           | 998.73 KiB (1%) |        1870 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.408 ms (5%) |           |   1.36 MiB (1%) |        1902 |
| `["sort", "sorted", "Base"]`                                       | 906.712 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 909.711 μs (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 916.812 μs (5%) |           | 998.73 KiB (1%) |        1870 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.117 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   9.420 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   5.019 ms (5%) |           |  51.00 KiB (1%) |         883 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.565 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.264 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      69861 s         13 s       2759 s      27683 s          0 s
       #2  2593 MHz      51840 s          8 s       2477 s      46878 s          0 s
       
  Memory: 6.791378021240234 GB (2544.9296875 MB free)
  Uptime: 1022.0 sec
  Load Avg:  1.25  1.30810546875  0.9560546875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 28 Jan 2021 - 0:53
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
| `["findfirst", "0%", "base"]`                                      |   3.700 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  22.501 μs (5%) |           |  11.98 KiB (1%) |         220 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  21.600 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 234.385 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     | 106.001 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  68.401 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 151.002 μs (5%) |           |  42.20 KiB (1%) |         777 |
| `["findfirst", "10%", "tx-seq"]`                                   |  71.501 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 219.703 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 115.701 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 188.602 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "20%", "tx-seq"]`                                   | 151.902 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 221.502 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 154.302 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 208.803 μs (5%) |           |  33.09 KiB (1%) |         615 |
| `["findfirst", "30%", "tx-seq"]`                                   | 222.603 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 426.805 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 237.803 μs (5%) |           |  35.41 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-noterm"]`                                | 244.003 μs (5%) |           |  35.42 KiB (1%) |         657 |
| `["findfirst", "40%", "tx-seq"]`                                   | 289.904 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 536.207 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 272.603 μs (5%) |           |  37.83 KiB (1%) |         706 |
| `["findfirst", "50%", "tx-noterm"]`                                | 302.404 μs (5%) |           |  54.08 KiB (1%) |        1004 |
| `["findfirst", "50%", "tx-seq"]`                                   | 362.904 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 293.417 ms (5%) | 27.604 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 222.412 ms (5%) | 27.673 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  10.679 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   7.963 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   5.682 ms (5%) |           |  25.95 KiB (1%) |         361 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   4.065 ms (5%) |           |  12.78 KiB (1%) |         126 |
| `["foreach_seq", "base", "Matrix"]`                                |   1.008 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.098 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 742.510 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  |   1.016 ms (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.182 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 744.010 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  20.200 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  20.100 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  22.800 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  20.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  51.015 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 900.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 900.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.700 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.700 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 334.664 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 207.918 ms (5%) |  4.974 ms | 160.73 MiB (1%) |     2016630 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.186 ms (5%) |           |  59.27 KiB (1%) |        1118 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.247 ms (5%) |           |  59.16 KiB (1%) |        1114 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.614 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.043 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 614.908 μs (5%) |           | 965.11 KiB (1%) |        1226 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 647.908 μs (5%) |           |   1.02 MiB (1%) |        1246 |
| `["sort", "F64 (wide)", "Base"]`                                   |   6.490 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   5.448 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   3.755 ms (5%) |           |   1.01 MiB (1%) |        2148 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.460 ms (5%) |           |   1.39 MiB (1%) |        2196 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 135.301 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 126.402 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 127.302 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 125.401 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   7.325 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.586 ms (5%) |           |   1.19 MiB (1%) |         555 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.337 ms (5%) |           |   1.01 MiB (1%) |        2236 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.826 ms (5%) |           |   1.40 MiB (1%) |        2266 |
| `["sort", "reversed", "Base"]`                                     | 960.213 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.262 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 963.612 μs (5%) |           | 998.73 KiB (1%) |        1870 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.459 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["sort", "sorted", "Base"]`                                       | 909.812 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 920.512 μs (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 947.212 μs (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.128 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   9.294 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   5.051 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.483 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.223 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      90926 s         13 s       3220 s      47420 s          0 s
       #2  2593 MHz      84180 s          8 s       3471 s      54765 s          0 s
       
  Memory: 6.791378021240234 GB (2931.5546875 MB free)
  Uptime: 1435.0 sec
  Load Avg:  1.29833984375  1.35693359375  1.1025390625
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
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    Stepping:                        7
    CPU MHz:                         2593.907
    BogoMIPS:                        5187.81
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
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
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

