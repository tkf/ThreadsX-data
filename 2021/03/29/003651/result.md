# Benchmark result

* Pull request commit: [`976aea4182dfa46c3f474125a91aff5402472ea1`](https://github.com/tkf/ThreadsX.jl/commit/976aea4182dfa46c3f474125a91aff5402472ea1)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 29 Mar 2021 - 00:28
    - Baseline: 29 Mar 2021 - 00:36
* Package commits:
    - Target: 210dcf
    - Baseline: 3ff826
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
| `["findfirst", "0%", "tx"]`                                        |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "0%", "tx-noterm"]`                                 |               17.64 (5%) :x: |                2.06 (1%) :x: |
| `["findfirst", "0%", "tx-seq"]`                                    | 0.70 (5%) :white_check_mark: | 0.71 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx"]`                                       |                2.59 (5%) :x: |                2.26 (1%) :x: |
| `["findfirst", "10%", "tx-noterm"]`                                |                1.98 (5%) :x: | 0.62 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "20%", "tx"]`                                       |                1.27 (5%) :x: |                1.31 (1%) :x: |
| `["findfirst", "20%", "tx-noterm"]`                                |                1.98 (5%) :x: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "20%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "30%", "tx"]`                                       |                1.23 (5%) :x: |                   0.99 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                                |                2.09 (5%) :x: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "30%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx"]`                                       |                   1.02 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx-noterm"]`                                |                1.51 (5%) :x: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "40%", "tx-seq"]`                                   |                   1.00 (5%)  | 0.72 (1%) :white_check_mark: |
| `["findfirst", "50%", "base"]`                                     |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                                       |                1.09 (5%) :x: |                1.41 (1%) :x: |
| `["findfirst", "50%", "tx-noterm"]`                                |                1.23 (5%) :x: | 0.62 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx-seq"]`                                   |                1.09 (5%) :x: | 0.72 (1%) :white_check_mark: |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |                1.25 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |                1.25 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                                        |                   0.97 (5%)  |                1.02 (1%) :x: |
| `["mapi", "consume-100us", "tx"]`                                  |                   0.99 (5%)  |                1.01 (1%) :x: |
| `["mapi", "consume-1ms", "tx"]`                                    |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   |                   1.01 (5%)  | 0.59 (1%) :white_check_mark: |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   |                   1.01 (5%)  | 0.59 (1%) :white_check_mark: |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             |                   1.00 (5%)  | 0.59 (1%) :white_check_mark: |
| `["sort", "I64 (wide)", "Base"]`                                   |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "sorted", "Base"]`                                       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |                   0.99 (5%)  | 0.55 (1%) :white_check_mark: |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |                   1.03 (5%)  | 0.98 (1%) :white_check_mark: |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1041-azure #43-Ubuntu SMP Fri Feb 26 10:21:20 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      70666 s         12 s       2952 s      31533 s          0 s
       #2  2294 MHz      62350 s          8 s       2822 s      39896 s          0 s
       
  Memory: 6.791343688964844 GB (2344.26953125 MB free)
  Uptime: 1066.0 sec
  Load Avg:  1.33837890625  1.35888671875  1.017578125
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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1041-azure #43-Ubuntu SMP Fri Feb 26 10:21:20 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      96520 s         12 s       3594 s      49584 s          0 s
       #2  2294 MHz      94002 s          8 s       3954 s      51703 s          0 s
       
  Memory: 6.791343688964844 GB (2621.16796875 MB free)
  Uptime: 1513.0 sec
  Load Avg:  1.24169921875  1.3740234375  1.154296875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 29 Mar 2021 - 0:28
* Package commit: 210dcf
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
| `["findfirst", "0%", "base"]`                                      |   3.100 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  23.800 μs (5%) |           |  11.77 KiB (1%) |         218 |
| `["findfirst", "0%", "tx-noterm"]`                                 | 381.003 μs (5%) |           |  24.70 KiB (1%) |         245 |
| `["findfirst", "0%", "tx-seq"]`                                    | 159.091 ns (5%) |           |  400 bytes (1%) |          13 |
| `["findfirst", "10%", "base"]`                                     |  64.700 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       | 193.398 μs (5%) |           |  32.61 KiB (1%) |         607 |
| `["findfirst", "10%", "tx-noterm"]`                                | 379.594 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "10%", "tx-seq"]`                                   |  64.899 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "20%", "base"]`                                     | 128.599 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 181.599 μs (5%) |           |  28.05 KiB (1%) |         525 |
| `["findfirst", "20%", "tx-noterm"]`                                | 387.901 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "20%", "tx-seq"]`                                   | 128.699 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "30%", "base"]`                                     | 192.202 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 226.204 μs (5%) |           |  28.06 KiB (1%) |         526 |
| `["findfirst", "30%", "tx-noterm"]`                                | 385.101 μs (5%) |           |  24.81 KiB (1%) |         252 |
| `["findfirst", "30%", "tx-seq"]`                                   | 192.201 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "40%", "base"]`                                     | 255.996 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 264.299 μs (5%) |           |  35.02 KiB (1%) |         654 |
| `["findfirst", "40%", "tx-noterm"]`                                | 393.597 μs (5%) |           |  24.80 KiB (1%) |         251 |
| `["findfirst", "40%", "tx-seq"]`                                   | 255.996 μs (5%) |           |  416 bytes (1%) |          14 |
| `["findfirst", "50%", "base"]`                                     | 319.801 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 318.701 μs (5%) |           |  53.55 KiB (1%) |        1000 |
| `["findfirst", "50%", "tx-noterm"]`                                | 392.101 μs (5%) |           |  24.89 KiB (1%) |         257 |
| `["findfirst", "50%", "tx-seq"]`                                   | 319.800 μs (5%) |           |  416 bytes (1%) |          14 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 427.290 ms (5%) | 31.512 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 262.541 ms (5%) | 33.848 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  20.831 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |  10.416 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |   9.992 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   5.182 ms (5%) |           |  12.75 KiB (1%) |         124 |
| `["foreach_seq", "base", "Matrix"]`                                | 611.701 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.088 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 611.401 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 615.801 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               | 989.002 μs (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 611.701 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  22.000 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  22.100 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  22.000 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  22.100 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          | 116.485 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 117.615 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 117.396 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 116.703 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   2.367 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   2.378 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.833 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.833 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 273.943 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 194.076 ms (5%) |  5.638 ms | 158.26 MiB (1%) |     2016660 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.190 ms (5%) |           |  59.09 KiB (1%) |        1115 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.340 ms (5%) |           |  59.03 KiB (1%) |        1115 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.267 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.589 ms (5%) |           |   1.19 MiB (1%) |         535 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   |   1.566 ms (5%) |           | 965.11 KiB (1%) |        1226 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |   1.576 ms (5%) |           |   1.02 MiB (1%) |        1245 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.630 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.792 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.956 ms (5%) |           |   1.01 MiB (1%) |        2144 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.679 ms (5%) |           |   1.39 MiB (1%) |        2194 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 138.200 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 141.500 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 142.100 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 140.801 μs (5%) |           |  512 bytes (1%) |          12 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.641 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.169 ms (5%) |           |   1.19 MiB (1%) |         550 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.929 ms (5%) |           |   1.01 MiB (1%) |        2231 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.777 ms (5%) |           |   1.39 MiB (1%) |        2266 |
| `["sort", "reversed", "Base"]`                                     | 700.500 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.187 ms (5%) |           |   1.18 MiB (1%) |         429 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.123 ms (5%) |           | 998.42 KiB (1%) |        1867 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.479 ms (5%) |           |   1.36 MiB (1%) |        1899 |
| `["sort", "sorted", "Base"]`                                       | 611.700 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 884.201 μs (5%) |           |   1.18 MiB (1%) |         425 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |   1.125 ms (5%) |           | 998.42 KiB (1%) |        1867 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.254 ms (5%) |           |   1.36 MiB (1%) |        1897 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   8.787 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.671 ms (5%) |           |  28.06 KiB (1%) |         368 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.324 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.253 ms (5%) |           |   1.05 MiB (1%) |         672 |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1041-azure #43-Ubuntu SMP Fri Feb 26 10:21:20 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      70666 s         12 s       2952 s      31533 s          0 s
       #2  2294 MHz      62350 s          8 s       2822 s      39896 s          0 s
       
  Memory: 6.791343688964844 GB (2344.26953125 MB free)
  Uptime: 1066.0 sec
  Load Avg:  1.33837890625  1.35888671875  1.017578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 29 Mar 2021 - 0:36
* Package commit: 3ff826
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
| `["findfirst", "0%", "base"]`                                      |   3.000 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                        |  23.900 μs (5%) |           |  11.97 KiB (1%) |         219 |
| `["findfirst", "0%", "tx-noterm"]`                                 |  21.600 μs (5%) |           |  12.02 KiB (1%) |         221 |
| `["findfirst", "0%", "tx-seq"]`                                    | 227.632 ns (5%) |           |  560 bytes (1%) |          15 |
| `["findfirst", "10%", "base"]`                                     |  65.100 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                       |  74.800 μs (5%) |           |  14.44 KiB (1%) |         271 |
| `["findfirst", "10%", "tx-noterm"]`                                | 192.000 μs (5%) |           |  39.89 KiB (1%) |         736 |
| `["findfirst", "10%", "tx-seq"]`                                   |  65.100 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "20%", "base"]`                                     | 128.100 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                       | 143.101 μs (5%) |           |  21.42 KiB (1%) |         399 |
| `["findfirst", "20%", "tx-noterm"]`                                | 195.500 μs (5%) |           |  28.42 KiB (1%) |         529 |
| `["findfirst", "20%", "tx-seq"]`                                   | 128.800 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "30%", "base"]`                                     | 192.000 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                       | 183.801 μs (5%) |           |  28.34 KiB (1%) |         525 |
| `["findfirst", "30%", "tx-noterm"]`                                | 184.500 μs (5%) |           |  28.41 KiB (1%) |         528 |
| `["findfirst", "30%", "tx-seq"]`                                   | 192.900 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "40%", "base"]`                                     | 256.000 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                       | 259.300 μs (5%) |           |  35.39 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-noterm"]`                                | 260.801 μs (5%) |           |  35.41 KiB (1%) |         656 |
| `["findfirst", "40%", "tx-seq"]`                                   | 256.000 μs (5%) |           |  576 bytes (1%) |          16 |
| `["findfirst", "50%", "base"]`                                     | 293.201 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                       | 291.100 μs (5%) |           |  37.84 KiB (1%) |         707 |
| `["findfirst", "50%", "tx-noterm"]`                                | 318.600 μs (5%) |           |  40.23 KiB (1%) |         755 |
| `["findfirst", "50%", "tx-seq"]`                                   | 293.500 μs (5%) |           |  576 bytes (1%) |          16 |
| `["foreach", "base", "A .= B .+ B'"]`                              | 436.962 ms (5%) | 30.364 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                               | 253.326 ms (5%) | 31.009 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                         |  21.462 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                          |   9.974 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                |  10.121 ms (5%) |           |  25.94 KiB (1%) |         360 |
| `["foreach", "tx", "A .= B .+ C"]`                                 |   5.178 ms (5%) |           |  12.75 KiB (1%) |         124 |
| `["foreach_seq", "base", "Matrix"]`                                | 611.301 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                             |   2.026 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                | 611.500 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                  | 615.201 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                               | 951.901 μs (5%) |           |   16 bytes (1%) |           1 |
| `["foreach_seq", "tx", "Vector"]`                                  | 611.501 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                       |  22.100 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => :ivdep"]`     |  22.200 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => false"]`      |  22.000 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", ":simd => true"]`       |  22.100 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                          | 116.266 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => :ivdep"]`        | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => false"]`         | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", ":simd => true"]`          | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "man"]`                   |   1.900 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => :ivdep"]` |   1.899 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => false"]`  |   2.700 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", ":nvecs => 8", "tx", ":simd => true"]`   |   2.700 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                      | 282.464 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                        | 200.604 ms (5%) |  6.726 ms | 154.63 MiB (1%) |     2016679 |
| `["mapi", "consume-100us", "base"]`                                |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                  |   1.197 ms (5%) |           |  58.34 KiB (1%) |        1099 |
| `["mapi", "consume-1ms", "base"]`                                  |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                    |  10.328 ms (5%) |           |  59.97 KiB (1%) |        1129 |
| `["sort", "F64 (narrow)", "Base"]`                                 |   2.267 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                   |   2.730 ms (5%) |           |   1.19 MiB (1%) |         534 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                   |   1.620 ms (5%) |           | 965.11 KiB (1%) |        1226 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`             |   1.617 ms (5%) |           |   1.02 MiB (1%) |        1245 |
| `["sort", "F64 (wide)", "Base"]`                                   |   5.699 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                     |   4.744 ms (5%) |           |   1.19 MiB (1%) |         564 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                     |   4.949 ms (5%) |           |   1.01 MiB (1%) |        2146 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`               |   5.999 ms (5%) |           |   1.39 MiB (1%) |        2191 |
| `["sort", "I64 (narrow)", "Base"]`                                 | 138.000 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                   | 139.800 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                   | 140.600 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`             | 140.600 μs (5%) |           |  864 bytes (1%) |          17 |
| `["sort", "I64 (wide)", "Base"]`                                   |   5.185 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                     |   4.100 ms (5%) |           |   1.19 MiB (1%) |         554 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                     |   3.967 ms (5%) |           |   1.01 MiB (1%) |        2236 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`               |   4.854 ms (5%) |           |   1.40 MiB (1%) |        2271 |
| `["sort", "reversed", "Base"]`                                     | 698.301 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                       |   1.248 ms (5%) |           |   1.18 MiB (1%) |         435 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                       |   1.153 ms (5%) |           | 998.75 KiB (1%) |        1871 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                 |   1.577 ms (5%) |           |   1.36 MiB (1%) |        1903 |
| `["sort", "sorted", "Base"]`                                       | 659.601 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                         | 894.501 μs (5%) |           |   1.18 MiB (1%) |         431 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                         |   1.205 ms (5%) |           | 998.77 KiB (1%) |        1872 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                   |   1.247 ms (5%) |           |   1.36 MiB (1%) |        1904 |
| `["unique", "rand(1:10, 1000000)", "base"]`                        |   8.973 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                          |   4.701 ms (5%) |           |  50.98 KiB (1%) |         882 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                      |   8.259 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                        |   5.102 ms (5%) |           |   1.07 MiB (1%) |        1186 |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1041-azure #43-Ubuntu SMP Fri Feb 26 10:21:20 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      96520 s         12 s       3594 s      49584 s          0 s
       #2  2294 MHz      94002 s          8 s       3954 s      51703 s          0 s
       
  Memory: 6.791343688964844 GB (2621.16796875 MB free)
  Uptime: 1513.0 sec
  Load Avg:  1.24169921875  1.3740234375  1.154296875
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
    Model:                           79
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:                        1
    CPU MHz:                         2294.690
    BogoMIPS:                        4589.38
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
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
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

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

