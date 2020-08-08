# Benchmark result

* Pull request commit: [`fa4fe92ef57f12aa811254a30b804df0c915a7c9`](https://github.com/tkf/ThreadsX.jl/commit/fa4fe92ef57f12aa811254a30b804df0c915a7c9)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 8 Aug 2020 - 00:33
    - Baseline: 8 Aug 2020 - 00:39
* Package commits:
    - Target: 5c553b
    - Baseline: c9954c
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

| ID                                                                 | time ratio                   | memory ratio  |
|--------------------------------------------------------------------|------------------------------|---------------|
| `["findfirst", "0%", "tx"]`                                        | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "10%", "tx-noterm"]`                                |                1.10 (5%) :x: | 1.05 (1%) :x: |
| `["findfirst", "10%", "tx-seq"]`                                   |                1.50 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "20%", "tx-noterm"]`                                |                1.06 (5%) :x: | 1.14 (1%) :x: |
| `["findfirst", "20%", "tx-seq"]`                                   |                1.49 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                                |                1.11 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "30%", "tx-seq"]`                                   |                1.49 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                                |                1.27 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "40%", "tx-seq"]`                                   |                1.50 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.12 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "50%", "tx-seq"]`                                   |                1.50 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |            43636.36 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |            45500.51 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |            43636.36 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.33 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.33 (5%) :x: |    1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |                1.05 (5%) :x: |    1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |                1.06 (5%) :x: |    1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |                1.05 (5%) :x: |    1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |                1.19 (5%) :x: |    1.00 (1%)  |

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
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      45298 s          0 s       2166 s      39612 s          0 s
       #2  2095 MHz      59062 s          0 s       3000 s      24718 s          0 s
       
  Memory: 6.764881134033203 GB (1859.890625 MB free)
  Uptime: 888.0 sec
  Load Avg:  1.33349609375  1.3251953125  0.86767578125
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
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      73807 s          0 s       3119 s      44454 s          0 s
       #2  2095 MHz      75746 s          0 s       3539 s      41868 s          0 s
       
  Memory: 6.764881134033203 GB (2217.7421875 MB free)
  Uptime: 1233.0 sec
  Load Avg:  1.3671875  1.3955078125  1.05126953125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 8 Aug 2020 - 0:33
* Package commit: 5c553b
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
| `["findfirst", "0%", "tx"]`                                        |  19.401 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  17.900 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 184.528 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  87.600 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  75.701 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 223.202 μs (5%) |           |  44.52 KiB (1%) |         820 |
| `["findfirst", "10%", "tx-seq"]`                                   |  87.900 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 175.301 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 143.901 μs (5%) |           |  21.41 KiB (1%) |         398 |
| `["findfirst", "20%", "tx-noterm"]`                                | 220.602 μs (5%) |           |  37.72 KiB (1%) |         701 |
| `["findfirst", "20%", "tx-seq"]`                                   | 175.901 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 262.803 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 193.602 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 249.802 μs (5%) |           |  28.39 KiB (1%) |         527 |
| `["findfirst", "30%", "tx-seq"]`                                   | 263.503 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 350.403 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 264.103 μs (5%) |           |  35.39 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-noterm"]`                                | 310.703 μs (5%) |           |  35.47 KiB (1%) |         660 |
| `["findfirst", "40%", "tx-seq"]`                                   | 351.103 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 438.004 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 307.403 μs (5%) |           |  37.81 KiB (1%) |         705 |
| `["findfirst", "50%", "tx-noterm"]`                                | 386.504 μs (5%) |           |  54.08 KiB (1%) |        1004 |
| `["findfirst", "50%", "tx-seq"]`                                   | 438.604 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 237.955 ms (5%) | 19.196 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 181.348 ms (5%) | 28.875 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   6.755 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   5.816 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   3.692 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.119 ms (5%) |           |  12.77 KiB (1%) |         125 |
| `["foreach_seq", "base", "Matrix"]`                                | 621.104 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   1.759 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 621.204 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 624.403 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.031 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 625.603 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  17.000 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  17.200 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  20.600 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  16.800 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  43.434 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  43.636 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  45.501 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  43.636 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 930.233 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 927.907 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.300 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.300 μs (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.128 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.309 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 498.103 μs (5%) |           | 965.13 KiB (1%) |        1227 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 513.203 μs (5%) |           |   1.02 MiB (1%) |        1248 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.382 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.312 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   2.865 ms (5%) |           |   1.01 MiB (1%) |        2148 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.323 ms (5%) |           |   1.39 MiB (1%) |        2197 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 111.400 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 101.101 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 101.801 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 101.700 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.362 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   3.643 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   2.679 ms (5%) |           |   1.01 MiB (1%) |        2236 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.161 ms (5%) |           |   1.40 MiB (1%) |        2270 |
| `["sort", "reversed", "Base"]`                                     | 589.504 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.009 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 748.805 μs (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.157 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["sort", "sorted", "Base"]`                                       | 562.504 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 746.805 μs (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 748.605 μs (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   | 890.805 μs (5%) |           |   1.36 MiB (1%) |        1899 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   7.871 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.847 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.147 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.352 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      45298 s          0 s       2166 s      39612 s          0 s
       #2  2095 MHz      59062 s          0 s       3000 s      24718 s          0 s
       
  Memory: 6.764881134033203 GB (1859.890625 MB free)
  Uptime: 888.0 sec
  Load Avg:  1.33349609375  1.3251953125  0.86767578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 8 Aug 2020 - 0:39
* Package commit: c9954c
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
| `["findfirst", "0%", "tx"]`                                        |  20.600 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  18.300 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 186.133 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  87.601 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  76.001 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 203.104 μs (5%) |           |  42.27 KiB (1%) |         781 |
| `["findfirst", "10%", "tx-seq"]`                                   |  58.601 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 175.303 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 139.803 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 207.303 μs (5%) |           |  33.05 KiB (1%) |         612 |
| `["findfirst", "20%", "tx-seq"]`                                   | 118.002 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 262.901 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 195.001 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 224.901 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 176.401 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 350.401 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 263.905 μs (5%) |           |  35.39 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-noterm"]`                                | 244.805 μs (5%) |           |  35.44 KiB (1%) |         658 |
| `["findfirst", "40%", "tx-seq"]`                                   | 234.702 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 438.002 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 304.702 μs (5%) |           |  37.86 KiB (1%) |         708 |
| `["findfirst", "50%", "tx-noterm"]`                                | 344.502 μs (5%) |           |  54.08 KiB (1%) |        1004 |
| `["findfirst", "50%", "tx-seq"]`                                   | 293.301 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 243.841 ms (5%) | 17.909 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 187.202 ms (5%) | 26.841 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   6.633 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   5.942 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   3.571 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.030 ms (5%) |           |  12.75 KiB (1%) |         124 |
| `["foreach_seq", "base", "Matrix"]`                                | 621.607 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   1.769 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 625.707 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 625.007 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.026 ms (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 621.207 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  17.500 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  17.100 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  20.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  17.000 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          |  44.444 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   | 700.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` | 700.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.300 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.300 μs (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.128 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.288 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 495.206 μs (5%) |           | 965.14 KiB (1%) |        1228 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 504.206 μs (5%) |           |   1.02 MiB (1%) |        1245 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.382 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.298 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   2.890 ms (5%) |           |   1.01 MiB (1%) |        2145 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.314 ms (5%) |           |   1.39 MiB (1%) |        2196 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 110.102 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 101.101 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 102.902 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 103.501 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.363 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   3.569 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   2.652 ms (5%) |           |   1.01 MiB (1%) |        2236 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   3.094 ms (5%) |           |   1.40 MiB (1%) |        2272 |
| `["sort", "reversed", "Base"]`                                     | 588.307 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       | 958.812 μs (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 756.210 μs (5%) |           | 998.73 KiB (1%) |        1870 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.088 ms (5%) |           |   1.36 MiB (1%) |        1902 |
| `["sort", "sorted", "Base"]`                                       | 558.707 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 710.609 μs (5%) |           |   1.18 MiB (1%) |         432 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 741.910 μs (5%) |           | 998.77 KiB (1%) |        1872 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   | 857.410 μs (5%) |           |   1.36 MiB (1%) |        1904 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   7.893 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.075 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.165 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.262 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      73807 s          0 s       3119 s      44454 s          0 s
       #2  2095 MHz      75746 s          0 s       3539 s      41868 s          0 s
       
  Memory: 6.764881134033203 GB (2217.7421875 MB free)
  Uptime: 1233.0 sec
  Load Avg:  1.3671875  1.3955078125  1.05126953125
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
    CPU MHz:             2095.078
    BogoMIPS:            4190.15
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

