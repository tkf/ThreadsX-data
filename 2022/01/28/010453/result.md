# Benchmark result

* Pull request commit: [`863c9ce855c582486734b9a9f43e8804530e5d02`](https://github.com/tkf/ThreadsX.jl/commit/863c9ce855c582486734b9a9f43e8804530e5d02)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 28 Jan 2022 - 00:56
    - Baseline: 28 Jan 2022 - 01:03
* Package commits:
    - Target: 14e735
    - Baseline: e05b14
* Julia commits:
    - Target: 905826
    - Baseline: 905826
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
| `["findfirst", "0%", "base"]`                          | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx-noterm"]`                     | 0.69 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "base"]`                         | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                           | 0.67 (5%) :white_check_mark: |                1.13 (1%) :x: |
| `["findfirst", "10%", "tx-noterm"]`                    | 0.64 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx-seq"]`                       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "20%", "base"]`                         | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                           | 0.66 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["findfirst", "20%", "tx-noterm"]`                    | 0.65 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                           | 0.71 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                    | 0.68 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                           | 0.69 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                    | 0.66 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                           | 0.70 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx-noterm"]`                    | 0.70 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ B'"]`             |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "man"]`           |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                            | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "Base"]`                       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "Base"]`                     | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.MergeSort"]`           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "base"]`            | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "tx"]`              | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |

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
Julia Version 1.6.5
Commit 9058264a69 (2021-12-19 12:30 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       6814 s          1 s        319 s       3988 s          0 s
       #2  2095 MHz       4956 s          1 s        307 s       5868 s          0 s
       
  Memory: 6.788978576660156 GB (2650.7109375 MB free)
  Uptime: 1122.5 sec
  Load Avg:  1.15  1.22  0.87
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.6.5
Commit 9058264a69 (2021-12-19 12:30 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       9921 s          1 s        448 s       5125 s          0 s
       #2  2095 MHz       7417 s          1 s        373 s       7717 s          0 s
       
  Memory: 6.788978576660156 GB (2785.63671875 MB free)
  Uptime: 1562.33 sec
  Load Avg:  1.2  1.29  1.05
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 28 Jan 2022 - 0:56
* Package commit: 14e735
* Julia commit: 905826
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
| `["findfirst", "0%", "base"]`                                        |   3.300 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   5.100 μs (5%) |           |   3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 464.703 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      | 106.285 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       | 194.701 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 160.601 μs (5%) |           |  12.55 KiB (1%) |         168 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 445.602 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     | 117.200 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 389.402 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 162.601 μs (5%) |           |   9.56 KiB (1%) |         131 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 445.603 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 234.101 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 584.004 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 165.101 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 434.403 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 351.002 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 778.705 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 209.701 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 441.603 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 467.703 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 973.406 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 290.602 μs (5%) |           |  16.86 KiB (1%) |         237 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 446.903 μs (5%) |           |  17.59 KiB (1%) |         260 |
| `["findfirst", "50%", "tx-seq"]`                                     | 584.603 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 359.698 ms (5%) | 40.026 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 307.369 ms (5%) | 40.085 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |  10.971 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   7.557 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   4.777 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   3.685 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  | 844.407 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   2.742 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 845.509 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 854.909 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 |   1.646 ms (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 845.309 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  27.500 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  27.600 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  26.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  27.001 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            | 104.377 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         | 104.650 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          | 104.866 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           | 104.804 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    |   1.220 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` |   1.220 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   3.075 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   3.075 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 332.751 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 310.240 ms (5%) | 26.113 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.237 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.307 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   2.932 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   3.239 ms (5%) |           |   1.17 MiB (1%) |         296 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 795.106 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 835.805 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   7.424 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   6.215 ms (5%) |           |   1.17 MiB (1%) |         319 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   4.252 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.763 ms (5%) |           |   1.35 MiB (1%) |        1582 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 145.700 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 140.700 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 140.501 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 140.301 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   8.286 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   5.865 ms (5%) |           |   1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   4.047 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.938 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 863.105 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.463 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         |   1.005 ms (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.646 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 802.805 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           |   1.215 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           |   1.007 ms (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     |   1.344 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   5.688 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   2.543 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   8.530 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   5.107 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
Julia Version 1.6.5
Commit 9058264a69 (2021-12-19 12:30 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       6814 s          1 s        319 s       3988 s          0 s
       #2  2095 MHz       4956 s          1 s        307 s       5868 s          0 s
       
  Memory: 6.788978576660156 GB (2650.7109375 MB free)
  Uptime: 1122.5 sec
  Load Avg:  1.15  1.22  0.87
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 28 Jan 2022 - 1:3
* Package commit: e05b14
* Julia commit: 905826
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
| `["findfirst", "0%", "base"]`                                        |   3.600 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   5.250 μs (5%) |           |   3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 674.407 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      | 110.294 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       | 210.302 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 238.402 μs (5%) |           |  11.06 KiB (1%) |         150 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 693.107 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     | 126.401 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 421.304 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 245.303 μs (5%) |           |  11.14 KiB (1%) |         152 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 680.907 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 235.503 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 584.906 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 231.202 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 635.807 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 351.603 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 780.008 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 305.603 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 673.207 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 468.305 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 973.411 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 417.205 μs (5%) |           |  16.86 KiB (1%) |         237 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 636.807 μs (5%) |           |  17.59 KiB (1%) |         260 |
| `["findfirst", "50%", "tx-seq"]`                                     | 584.506 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 367.817 ms (5%) | 42.057 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 321.956 ms (5%) | 42.046 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |  10.363 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   7.387 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   4.630 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   3.681 ms (5%) |           |   9.08 KiB (1%) |         132 |
| `["foreach_seq", "base", "Matrix"]`                                  | 835.609 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   2.874 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 837.009 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 847.901 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 |   1.647 ms (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 848.709 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  25.700 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  26.201 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  27.200 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  26.201 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            | 104.377 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    |   1.300 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` |   1.200 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   3.300 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   3.300 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 336.521 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 328.751 ms (5%) | 30.982 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.232 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.355 ms (5%) |           |  58.75 KiB (1%) |        1176 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   3.068 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   3.376 ms (5%) |           |   1.17 MiB (1%) |         296 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 839.509 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 852.810 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   7.821 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   6.313 ms (5%) |           |   1.17 MiB (1%) |         317 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   4.315 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.869 ms (5%) |           |   1.35 MiB (1%) |        1582 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 153.402 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 148.302 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 144.701 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 145.502 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   8.270 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   5.906 ms (5%) |           |   1.17 MiB (1%) |         312 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   4.067 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.976 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 859.209 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.549 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         |   1.038 ms (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.631 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 808.709 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           |   1.206 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           |   1.012 ms (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     |   1.390 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   6.032 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   2.734 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   8.943 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   5.152 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
Julia Version 1.6.5
Commit 9058264a69 (2021-12-19 12:30 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       9921 s          1 s        448 s       5125 s          0 s
       #2  2095 MHz       7417 s          1 s        373 s       7717 s          0 s
       
  Memory: 6.788978576660156 GB (2785.63671875 MB free)
  Uptime: 1562.33 sec
  Load Avg:  1.2  1.29  1.05
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
    CPU MHz:                         2095.080
    BogoMIPS:                        4190.16
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2 MiB
    L3 cache:                        35.8 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
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

