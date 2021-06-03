# Benchmark result

* Pull request commit: [`25db588998fd9fb8b1231334475f7bd2501dd5f1`](https://github.com/tkf/ThreadsX.jl/commit/25db588998fd9fb8b1231334475f7bd2501dd5f1)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Jun 2021 - 01:54
    - Baseline: 3 Jun 2021 - 02:01
* Package commits:
    - Target: 3afff2
    - Baseline: dd3d4e
* Julia commits:
    - Target: 6aaede
    - Baseline: 6aaede
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
| `["findfirst", "0%", "base"]`                                      |                1.20 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "0%", "tx"]`                                        |                1.15 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                                       |                   1.00 (5%)  | 1.13 (1%) :x: |
| `["foreach", "tx", "A .= B .+ B'"]`                                | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq", "base", "Matrix"]`                                | 0.75 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq", "base", "Transpose"]`                             |                1.08 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq", "base", "Vector"]`                                |                1.34 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq", "tx", "Matrix"]`                                  |                1.33 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq", "tx", "Transpose"]`                               |                1.27 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq", "tx", "Vector"]`                                  |                1.35 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "man"]`                       | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |                1.11 (5%) :x: |    1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["mapi", "collatz", "base"]`                                      |                1.21 (5%) :x: |    1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                                        |                1.05 (5%) :x: |    1.00 (1%)  |
| `["mapi", "consume-100us", "tx"]`                                  |                1.05 (5%) :x: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "Base"]`                                 | 0.83 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "Base"]`                                   | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   |                1.05 (5%) :x: |    1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |

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
Julia Version 1.6.1
Commit 6aaedecc44 (2021-04-23 05:59 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       6885 s          1 s        218 s       3385 s          0 s
       #2  2095 MHz       5067 s          1 s        264 s       5171 s          0 s
       
  Memory: 6.791339874267578 GB (2636.75 MB free)
  Uptime: 1056.0 sec
  Load Avg:  1.25  1.31  0.97
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.6.1
Commit 6aaedecc44 (2021-04-23 05:59 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       9288 s          1 s        283 s       5159 s          0 s
       #2  2095 MHz       8164 s          1 s        351 s       6222 s          0 s
       
  Memory: 6.791339874267578 GB (2920.140625 MB free)
  Uptime: 1482.0 sec
  Load Avg:  1.2  1.31  1.1
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 3 Jun 2021 - 1:54
* Package commit: 3afff2
* Julia commit: 6aaede
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                 | time            | GC time   | memory           | allocations |
|--------------------------------------------------------------------|----------------:|----------:|-----------------:|------------:|
| `["findfirst", "0%", "base"]`                                      |   3.600 ns (5%) |           |                  |             |
| `["findfirst", "0%", "tx"]`                                        |   5.584 μs (5%) |           |    3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 736.346 μs (5%) |           |   17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                    | 102.913 ns (5%) |           |   176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                     | 194.712 μs (5%) |           |                  |             |
| `["findfirst", "10%", "tx"]`                                       | 253.916 μs (5%) |           |   13.28 KiB (1%) |         177 |
| `["findfirst", "10%", "tx-noterm"]`                                | 723.945 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                   |  78.104 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                     | 389.324 μs (5%) |           |                  |             |
| `["findfirst", "20%", "tx"]`                                       | 262.016 μs (5%) |           |   11.91 KiB (1%) |         162 |
| `["findfirst", "20%", "tx-noterm"]`                                | 699.644 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                   | 157.010 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                     | 584.036 μs (5%) |           |                  |             |
| `["findfirst", "30%", "tx"]`                                       | 238.215 μs (5%) |           |    9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                | 718.645 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                   | 234.714 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                     | 778.748 μs (5%) |           |                  |             |
| `["findfirst", "40%", "tx"]`                                       | 324.320 μs (5%) |           |   12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                | 741.147 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                   | 312.520 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                     | 973.360 μs (5%) |           |                  |             |
| `["findfirst", "50%", "tx"]`                                       | 452.728 μs (5%) |           |   16.86 KiB (1%) |         237 |
| `["findfirst", "50%", "tx-noterm"]`                                | 731.846 μs (5%) |           |   17.59 KiB (1%) |         260 |
| `["findfirst", "50%", "tx-seq"]`                                   | 390.524 μs (5%) |           |   192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 343.606 ms (5%) | 31.207 ms |  305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 285.177 ms (5%) | 31.469 ms |  305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   8.198 ms (5%) |           |                  |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.803 ms (5%) |           |                  |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   6.825 ms (5%) |           |   19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.427 ms (5%) |           |    9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                | 833.452 μs (5%) |           |                  |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.902 ms (5%) |           |                  |             |
| `["foreach_seq", "base", "Vector"]`                                |   1.114 ms (5%) |           |                  |             |
| `["foreach_seq", "tx", "Matrix"]`                                  |   1.123 ms (5%) |           |                  |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.649 ms (5%) |           |                  |             |
| `["foreach_seq", "tx", "Vector"]`                                  |   1.114 ms (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  24.501 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  26.601 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  24.602 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  24.502 μs (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "man"]`                          | 104.382 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 104.382 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 103.682 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 104.382 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.240 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.200 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   3.075 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   3.075 μs (5%) |           |                  |             |
| `["mapi", "collatz", "base"]`                                      | 405.374 ms (5%) |           |    7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 327.334 ms (5%) | 16.836 ms |  189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.344 ms (5%) |           |   58.80 KiB (1%) |        1174 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.405 ms (5%) |           |   58.80 KiB (1%) |        1175 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.997 ms (5%) |           |                  |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.247 ms (5%) |           |    1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 834.852 μs (5%) |           |  946.94 KiB (1%) |         973 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 863.454 μs (5%) |           |    1.04 MiB (1%) |         992 |
| `["sort", "F64 (wide)", "Base"]`                                   |   7.521 ms (5%) |           |                  |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   6.205 ms (5%) |           |    1.17 MiB (1%) |         317 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.336 ms (5%) |           | 1005.03 KiB (1%) |        1825 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.755 ms (5%) |           |    1.37 MiB (1%) |        1870 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 142.709 μs (5%) |           |   160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 137.808 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 139.808 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 135.409 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                   |   7.612 ms (5%) |           |                  |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   5.389 ms (5%) |           |    1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   4.031 ms (5%) |           | 1015.12 KiB (1%) |        2007 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.358 ms (5%) |           |    1.38 MiB (1%) |        2041 |
| `["sort", "reversed", "Base"]`                                     | 864.154 μs (5%) |           |                  |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.355 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.044 ms (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.454 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["sort", "sorted", "Base"]`                                       | 834.152 μs (5%) |           |                  |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 989.362 μs (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |   1.030 ms (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.195 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   5.860 ms (5%) |           |   832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   2.536 ms (5%) |           |   22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.909 ms (5%) |           |   65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.221 ms (5%) |           |    1.04 MiB (1%) |         619 |

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
Julia Version 1.6.1
Commit 6aaedecc44 (2021-04-23 05:59 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       6885 s          1 s        218 s       3385 s          0 s
       #2  2095 MHz       5067 s          1 s        264 s       5171 s          0 s
       
  Memory: 6.791339874267578 GB (2636.75 MB free)
  Uptime: 1056.0 sec
  Load Avg:  1.25  1.31  0.97
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 3 Jun 2021 - 2:1
* Package commit: dd3d4e
* Julia commit: 6aaede
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                 | time            | GC time   | memory           | allocations |
|--------------------------------------------------------------------|----------------:|----------:|-----------------:|------------:|
| `["findfirst", "0%", "base"]`                                      |   3.000 ns (5%) |           |                  |             |
| `["findfirst", "0%", "tx"]`                                        |   4.867 μs (5%) |           |    3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 734.945 μs (5%) |           |   17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                    | 107.003 ns (5%) |           |   176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                     | 194.612 μs (5%) |           |                  |             |
| `["findfirst", "10%", "tx"]`                                       | 254.315 μs (5%) |           |   11.75 KiB (1%) |         156 |
| `["findfirst", "10%", "tx-noterm"]`                                | 705.844 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                   |  78.104 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                     | 389.324 μs (5%) |           |                  |             |
| `["findfirst", "20%", "tx"]`                                       | 259.316 μs (5%) |           |   11.89 KiB (1%) |         162 |
| `["findfirst", "20%", "tx-noterm"]`                                | 736.046 μs (5%) |           |   17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                   | 157.210 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                     | 584.036 μs (5%) |           |                  |             |
| `["findfirst", "30%", "tx"]`                                       | 228.914 μs (5%) |           |    9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                | 710.945 μs (5%) |           |   17.44 KiB (1%) |         252 |
| `["findfirst", "30%", "tx-seq"]`                                   | 234.714 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                     | 778.648 μs (5%) |           |                  |             |
| `["findfirst", "40%", "tx"]`                                       | 320.420 μs (5%) |           |   12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                | 718.845 μs (5%) |           |   17.44 KiB (1%) |         252 |
| `["findfirst", "40%", "tx-seq"]`                                   | 312.419 μs (5%) |           |   192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                     | 973.261 μs (5%) |           |                  |             |
| `["findfirst", "50%", "tx"]`                                       | 453.729 μs (5%) |           |   16.89 KiB (1%) |         238 |
| `["findfirst", "50%", "tx-noterm"]`                                | 724.045 μs (5%) |           |   17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                   | 390.424 μs (5%) |           |   192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 338.287 ms (5%) | 29.511 ms |  305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 281.418 ms (5%) | 29.192 ms |  305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |   8.275 ms (5%) |           |                  |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   6.734 ms (5%) |           |                  |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   7.312 ms (5%) |           |   19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   3.425 ms (5%) |           |    9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                |   1.114 ms (5%) |           |                  |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.680 ms (5%) |           |                  |             |
| `["foreach_seq", "base", "Vector"]`                                | 833.548 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 841.849 μs (5%) |           |                  |             |
| `["foreach_seq", "tx", "Transpose"]`                               |   1.293 ms (5%) |           |                  |             |
| `["foreach_seq", "tx", "Vector"]`                                  | 827.548 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  29.002 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  23.901 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  29.401 μs (5%) |           |                  |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  28.701 μs (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "man"]`                          | 104.381 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 100.000 ns (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.200 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.200 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   3.100 μs (5%) |           |                  |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   3.100 μs (5%) |           |                  |             |
| `["mapi", "collatz", "base"]`                                      | 334.630 ms (5%) |           |    7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 311.293 ms (5%) | 26.363 ms |  189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.277 ms (5%) |           |   58.75 KiB (1%) |        1175 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |   240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.303 ms (5%) |           |   58.70 KiB (1%) |        1172 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   3.613 ms (5%) |           |                  |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   3.836 ms (5%) |           |    1.17 MiB (1%) |         296 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   | 845.748 μs (5%) |           |  946.94 KiB (1%) |         973 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             | 927.953 μs (5%) |           |    1.04 MiB (1%) |         992 |
| `["sort", "F64 (wide)", "Base"]`                                   |   8.207 ms (5%) |           |                  |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   6.867 ms (5%) |           |    1.17 MiB (1%) |         320 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.302 ms (5%) |           | 1005.03 KiB (1%) |        1825 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.303 ms (5%) |           |    1.37 MiB (1%) |        1870 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 146.708 μs (5%) |           |   160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 140.406 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 133.007 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 145.009 μs (5%) |           |   704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                   |   7.536 ms (5%) |           |                  |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   5.923 ms (5%) |           |    1.17 MiB (1%) |         312 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.986 ms (5%) |           | 1015.12 KiB (1%) |        2007 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.973 ms (5%) |           |    1.38 MiB (1%) |        2041 |
| `["sort", "reversed", "Base"]`                                     | 869.351 μs (5%) |           |                  |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.475 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.045 ms (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.661 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["sort", "sorted", "Base"]`                                       | 835.449 μs (5%) |           |                  |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         |   1.155 ms (5%) |           |    1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 997.158 μs (5%) |           |  985.53 KiB (1%) |        1660 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.391 ms (5%) |           |    1.35 MiB (1%) |        1692 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   5.827 ms (5%) |           |   832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   2.791 ms (5%) |           |   22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.951 ms (5%) |           |   65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.296 ms (5%) |           |    1.04 MiB (1%) |         619 |

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
Julia Version 1.6.1
Commit 6aaedecc44 (2021-04-23 05:59 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       9288 s          1 s        283 s       5159 s          0 s
       #2  2095 MHz       8164 s          1 s        351 s       6222 s          0 s
       
  Memory: 6.791339874267578 GB (2920.140625 MB free)
  Uptime: 1482.0 sec
  Load Avg:  1.2  1.31  1.1
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
    CPU MHz:                         2095.170
    BogoMIPS:                        4190.34
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

