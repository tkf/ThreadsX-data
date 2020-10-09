# Benchmark result

* Pull request commit: [`9825866040f4213025073a207de35f01029b41df`](https://github.com/tkf/ThreadsX.jl/commit/9825866040f4213025073a207de35f01029b41df)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/162> (Add ThreadsX.mapi)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Oct 2020 - 00:28
    - Baseline: 9 Oct 2020 - 00:34
* Package commits:
    - Target: 78c3d1
    - Baseline: b36e77
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
| `["findfirst", "0%", "base"]`                                      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx-noterm"]`                                 | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx-seq"]`                                    |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                                       |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx-noterm"]`                                |                   1.04 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx-seq"]`                                   |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx-noterm"]`                                |                   1.05 (5%)  | 0.89 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx-noterm"]`                                |                   1.01 (5%)  | 0.90 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx-seq"]`                                   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["foreach", "base", "A .= B .+ C"]`                               |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["foreach", "tx", "A .= B .+ C"]`                                 | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.49 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.54 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "Base"]`                                   |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |                1.08 (5%) :x: |                   1.00 (1%)  |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1026-azure #26~18.04.1-Ubuntu SMP Thu Sep 10 16:19:25 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      56738 s          0 s       2899 s      35165 s          0 s
       #2  2294 MHz      56153 s          0 s       2826 s      35667 s          0 s
       
  Memory: 6.791393280029297 GB (2347.96875 MB free)
  Uptime: 964.0 sec
  Load Avg:  1.2392578125  1.27880859375  0.8779296875
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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1026-azure #26~18.04.1-Ubuntu SMP Thu Sep 10 16:19:25 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      81380 s          0 s       3508 s      46209 s          0 s
       #2  2294 MHz      79333 s          0 s       3611 s      48048 s          0 s
       
  Memory: 6.791393280029297 GB (2761.67578125 MB free)
  Uptime: 1329.0 sec
  Load Avg:  1.2744140625  1.32421875  1.0400390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 9 Oct 2020 - 0:28
* Package commit: 78c3d1
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
| `["findfirst", "0%", "base"]`                                      |   2.999 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  22.000 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  19.900 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 217.663 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  59.599 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  72.799 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 173.598 μs (5%) |           |  23.77 KiB (1%) |         443 |
| `["findfirst", "10%", "tx-seq"]`                                   |  62.999 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 117.599 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 124.199 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 184.898 μs (5%) |           |  37.64 KiB (1%) |         697 |
| `["findfirst", "20%", "tx-seq"]`                                   | 117.999 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 175.497 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 169.598 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 197.698 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 176.397 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 234.597 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 233.597 μs (5%) |           |  35.39 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-noterm"]`                                | 238.897 μs (5%) |           |  35.44 KiB (1%) |         658 |
| `["findfirst", "40%", "tx-seq"]`                                   | 235.097 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 292.997 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 285.497 μs (5%) |           |  37.86 KiB (1%) |         708 |
| `["findfirst", "50%", "tx-noterm"]`                                | 302.397 μs (5%) |           |  42.48 KiB (1%) |         794 |
| `["findfirst", "50%", "tx-seq"]`                                   | 310.196 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 416.856 ms (5%) | 41.823 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 250.063 ms (5%) | 29.418 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  17.774 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   9.506 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   8.165 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   5.080 ms (5%) |           |  12.73 KiB (1%) |         123 |
| `["foreach_seq", "base", "Matrix"]`                                | 561.295 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   1.890 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 560.695 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 564.494 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               | 876.491 μs (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 561.195 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  20.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  20.400 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  20.199 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  20.400 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          | 104.189 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 101.845 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 104.922 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 101.873 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   2.378 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   2.467 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.833 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.933 μs (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.071 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.290 ms (5%) |           |   1.19 MiB (1%) |         534 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   |   1.425 ms (5%) |           | 965.09 KiB (1%) |        1225 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |   1.382 ms (5%) |           |   1.02 MiB (1%) |        1244 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.751 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.833 ms (5%) |           |   1.19 MiB (1%) |         563 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   5.040 ms (5%) |           |   1.01 MiB (1%) |        2146 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.567 ms (5%) |           |   1.39 MiB (1%) |        2194 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 128.799 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 132.099 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 138.199 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 131.899 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.093 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   3.799 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.776 ms (5%) |           |   1.01 MiB (1%) |        2236 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.396 ms (5%) |           |   1.40 MiB (1%) |        2270 |
| `["sort", "reversed", "Base"]`                                     | 642.094 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.119 ms (5%) |           |   1.18 MiB (1%) |         434 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 996.891 μs (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.363 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["sort", "sorted", "Base"]`                                       | 607.794 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 800.492 μs (5%) |           |   1.18 MiB (1%) |         431 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |   1.081 ms (5%) |           | 998.77 KiB (1%) |        1872 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.133 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   8.271 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.546 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.927 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.980 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1026-azure #26~18.04.1-Ubuntu SMP Thu Sep 10 16:19:25 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      56738 s          0 s       2899 s      35165 s          0 s
       #2  2294 MHz      56153 s          0 s       2826 s      35667 s          0 s
       
  Memory: 6.791393280029297 GB (2347.96875 MB free)
  Uptime: 964.0 sec
  Load Avg:  1.2392578125  1.27880859375  0.8779296875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 9 Oct 2020 - 0:34
* Package commit: b36e77
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
| `["findfirst", "0%", "base"]`                                      |   2.799 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  23.100 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  21.899 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 200.828 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  59.299 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  67.599 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 167.497 μs (5%) |           |  33.03 KiB (1%) |         614 |
| `["findfirst", "10%", "tx-seq"]`                                   |  59.898 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 117.197 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 122.997 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 176.396 μs (5%) |           |  42.25 KiB (1%) |         779 |
| `["findfirst", "20%", "tx-seq"]`                                   | 117.997 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 176.196 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 167.597 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 191.295 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 176.296 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 234.695 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 240.995 μs (5%) |           |  35.38 KiB (1%) |         655 |
| `["findfirst", "40%", "tx-noterm"]`                                | 239.195 μs (5%) |           |  35.41 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-seq"]`                                   | 234.795 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 293.393 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 283.194 μs (5%) |           |  37.84 KiB (1%) |         707 |
| `["findfirst", "50%", "tx-noterm"]`                                | 300.394 μs (5%) |           |  47.11 KiB (1%) |         878 |
| `["findfirst", "50%", "tx-seq"]`                                   | 293.194 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 421.096 ms (5%) | 25.239 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 228.013 ms (5%) | 23.499 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  15.749 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   9.217 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   8.089 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   5.423 ms (5%) |           |  12.75 KiB (1%) |         124 |
| `["foreach_seq", "base", "Matrix"]`                                | 560.691 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   1.852 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 560.592 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 564.692 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               | 892.687 μs (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 560.692 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  20.700 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  21.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  23.299 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  20.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          | 104.187 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |  99.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |  99.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |  99.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.599 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.599 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.499 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.699 μs (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "Base"]`                                 |   1.982 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.311 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   |   1.428 ms (5%) |           | 965.09 KiB (1%) |        1225 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |   1.391 ms (5%) |           |   1.02 MiB (1%) |        1244 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.056 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.567 ms (5%) |           |   1.19 MiB (1%) |         563 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.428 ms (5%) |           |   1.01 MiB (1%) |        2145 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.362 ms (5%) |           |   1.39 MiB (1%) |        2193 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 128.598 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 131.998 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 131.897 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 132.398 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.106 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   3.999 ms (5%) |           |   1.19 MiB (1%) |         553 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.568 ms (5%) |           |   1.01 MiB (1%) |        2236 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.309 ms (5%) |           |   1.40 MiB (1%) |        2270 |
| `["sort", "reversed", "Base"]`                                     | 641.890 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.103 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       | 986.784 μs (5%) |           | 998.73 KiB (1%) |        1870 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.375 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["sort", "sorted", "Base"]`                                       | 609.091 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 800.688 μs (5%) |           |   1.18 MiB (1%) |         430 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |   1.020 ms (5%) |           | 998.73 KiB (1%) |        1870 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.135 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   8.218 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.292 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   7.481 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   4.608 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1026-azure #26~18.04.1-Ubuntu SMP Thu Sep 10 16:19:25 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      81380 s          0 s       3508 s      46209 s          0 s
       #2  2294 MHz      79333 s          0 s       3611 s      48048 s          0 s
       
  Memory: 6.791393280029297 GB (2761.67578125 MB free)
  Uptime: 1329.0 sec
  Load Avg:  1.2744140625  1.32421875  1.0400390625
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
    Model:               79
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:            1
    CPU MHz:             2294.686
    BogoMIPS:            4589.37
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            51200K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

