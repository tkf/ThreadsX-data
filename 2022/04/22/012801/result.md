# Benchmark result

* Pull request commit: [`894fc3f39fdec34a53e022769d1a9640ee62eee4`](https://github.com/tkf/ThreadsX.jl/commit/894fc3f39fdec34a53e022769d1a9640ee62eee4)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 22 Apr 2022 - 01:20
    - Baseline: 22 Apr 2022 - 01:27
* Package commits:
    - Target: bafbd0
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
| `["findfirst", "0%", "base"]`                          | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx"]`                            |                1.32 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                           |                1.15 (5%) :x: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx-noterm"]`                    |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx-seq"]`                       | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                           |                1.24 (5%) :x: |                1.19 (1%) :x: |
| `["findfirst", "20%", "tx-seq"]`                       | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-seq"]`                       | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                    |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-seq"]`                       | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                           |                   0.98 (5%)  | 0.95 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx-seq"]`                       | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ B'"]`             |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["foreach", "tx", "A .= B .+ B'"]`                    |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Matrix"]`                    |                1.33 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Transpose"]`                 |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Matrix"]`                      |                1.32 (5%) :x: |                   1.00 (1%)  |
| `["foreach_seq", "tx", "Transpose"]`                   | 0.77 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "man"]`           |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["mapi", "collatz", "tx"]`                            | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`       |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`         |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`         | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`         | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`   | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "reversed", "ThreadsX.MergeSort"]`           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.MergeSort"]`             | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`       | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["unique", "rand(1:10, 1000000)", "base"]`            |                1.07 (5%) :x: |                   1.00 (1%)  |

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
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       4669 s          1 s        253 s       6225 s          0 s
       #2  2095 MHz       6931 s          1 s        335 s       3918 s          0 s
       
  Memory: 6.783611297607422 GB (2653.7890625 MB free)
  Uptime: 1124.86 sec
  Load Avg:  1.2  1.25  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.6.6
Commit b8708f954a (2022-03-28 07:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7426 s          1 s        336 s       7573 s          0 s
       #2  2095 MHz       9586 s          1 s        442 s       5346 s          0 s
       
  Memory: 6.783611297607422 GB (3031.609375 MB free)
  Uptime: 1545.1 sec
  Load Avg:  1.3  1.35  1.07
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 22 Apr 2022 - 1:20
* Package commit: bafbd0
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
| `["findfirst", "0%", "base"]`                                        |   2.200 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   5.583 μs (5%) |           |   3.91 KiB (1%) |          48 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 543.929 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  78.951 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       | 146.007 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 224.112 μs (5%) |           |  12.50 KiB (1%) |         166 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 635.033 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     |  59.403 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 292.115 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 238.013 μs (5%) |           |  14.12 KiB (1%) |         188 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 545.729 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 118.306 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 438.023 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 194.610 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 548.129 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 176.509 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 584.030 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 263.214 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 630.933 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 234.912 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 730.038 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 382.120 μs (5%) |           |  16.08 KiB (1%) |         227 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 562.230 μs (5%) |           |  17.59 KiB (1%) |         260 |
| `["findfirst", "50%", "tx-seq"]`                                     | 293.315 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 344.456 ms (5%) | 40.250 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 284.287 ms (5%) | 39.545 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |   8.295 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   6.689 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   4.145 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   3.353 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  | 835.544 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   2.198 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 626.133 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 842.344 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 |   1.033 ms (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 621.933 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  22.701 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  18.901 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  22.201 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  22.501 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            |  78.229 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         |  78.517 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          |  79.860 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           |  78.620 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    | 951.209 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` | 927.333 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   2.300 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   2.300 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 314.626 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 277.235 ms (5%) | 19.028 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.172 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.254 ms (5%) |           |  58.70 KiB (1%) |        1173 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   2.184 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   2.996 ms (5%) |           |   1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 624.933 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 701.237 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   5.909 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   5.736 ms (5%) |           |   1.17 MiB (1%) |         320 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   3.349 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.284 ms (5%) |           |   1.35 MiB (1%) |        1582 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 117.206 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 111.406 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 110.406 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 111.306 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   5.901 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   4.366 ms (5%) |           |   1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   3.326 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   3.537 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 665.635 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.078 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         | 847.245 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.214 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 633.134 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           | 819.143 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           | 843.045 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     | 929.750 μs (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   4.507 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   1.906 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   6.937 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   3.936 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       4669 s          1 s        253 s       6225 s          0 s
       #2  2095 MHz       6931 s          1 s        335 s       3918 s          0 s
       
  Memory: 6.783611297607422 GB (2653.7890625 MB free)
  Uptime: 1124.86 sec
  Load Avg:  1.2  1.25  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 22 Apr 2022 - 1:27
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
| `["findfirst", "0%", "base"]`                                        |   2.500 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   4.217 μs (5%) |           |   3.90 KiB (1%) |          47 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 546.729 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  79.364 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       | 146.006 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 194.709 μs (5%) |           |  13.27 KiB (1%) |         176 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 549.625 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     |  88.303 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 292.514 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 192.509 μs (5%) |           |  11.88 KiB (1%) |         161 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 535.624 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 175.908 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 438.623 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 189.010 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 555.630 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 263.514 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 584.825 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 275.212 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 555.125 μs (5%) |           |  17.44 KiB (1%) |         252 |
| `["findfirst", "40%", "tx-seq"]`                                     | 351.315 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 730.639 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 389.310 μs (5%) |           |  16.89 KiB (1%) |         238 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 544.528 μs (5%) |           |  17.59 KiB (1%) |         260 |
| `["findfirst", "50%", "tx-seq"]`                                     | 438.623 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 334.392 ms (5%) | 37.188 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 292.677 ms (5%) | 38.148 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |   7.626 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   6.596 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   3.913 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   3.346 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  | 626.833 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   2.067 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 623.633 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 635.933 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 |   1.348 ms (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 635.733 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  20.901 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  22.201 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  20.001 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  20.601 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            |  78.229 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           |   0.001 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    | 900.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` | 900.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   2.300 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   2.300 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 311.883 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 292.781 ms (5%) | 20.974 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.000 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.208 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.253 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   2.169 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   2.651 ms (5%) |           |   1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 653.635 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 672.512 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   5.738 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   4.893 ms (5%) |           |   1.17 MiB (1%) |         320 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   3.650 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   4.270 ms (5%) |           |   1.35 MiB (1%) |        1582 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 116.107 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     | 107.805 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     | 108.706 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               | 110.006 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   5.647 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   4.699 ms (5%) |           |   1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   3.326 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   3.748 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 658.334 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         |   1.151 ms (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         | 837.844 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   |   1.266 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 645.364 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           | 944.152 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           | 826.644 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     |   1.081 ms (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   4.207 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   2.000 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   6.705 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   3.867 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
  uname: Linux 5.13.0-1021-azure #24~20.04.1-Ubuntu SMP Tue Mar 29 15:34:22 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7426 s          1 s        336 s       7573 s          0 s
       #2  2095 MHz       9586 s          1 s        442 s       5346 s          0 s
       
  Memory: 6.783611297607422 GB (3031.609375 MB free)
  Uptime: 1545.1 sec
  Load Avg:  1.3  1.35  1.07
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
    CPU MHz:                         2095.178
    BogoMIPS:                        4190.35
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
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
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

