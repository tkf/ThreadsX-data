# Benchmark result

* Pull request commit: [`8b14e8515f55715db29762691ea14351359e9309`](https://github.com/tkf/ThreadsX.jl/commit/8b14e8515f55715db29762691ea14351359e9309)
* Pull request: <https://github.com/tkf/ThreadsX.jl/pull/122> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 27 Mar 2025 - 01:24
    - Baseline: 27 Mar 2025 - 01:30
* Package commits:
    - Target: ab75c3c
    - Baseline: d40e1be
* Julia commits:
    - Target: 3b76b25
    - Baseline: 3b76b25
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 2`
    - Baseline: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 2`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Brackets display [tolerances](https://juliaci.github.io/BenchmarkTools.jl/stable/manual/#Benchmark-Parameters) for the benchmark estimates. Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                     | time ratio                   | memory ratio                 |
|--------------------------------------------------------|------------------------------|------------------------------|
| `["findfirst", "0%", "base"]`                          | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx"]`                            |                   1.04 (5%)  | 0.95 (1%) :white_check_mark: |
| `["findfirst", "0%", "tx-noterm"]`                     |                1.48 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "0%", "tx-seq"]`                        | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx"]`                           |                1.36 (5%) :x: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "10%", "tx-noterm"]`                    |                1.48 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "10%", "tx-seq"]`                       |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx"]`                           |                1.39 (5%) :x: |                1.23 (1%) :x: |
| `["findfirst", "20%", "tx-noterm"]`                    |                1.48 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "20%", "tx-seq"]`                       |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx"]`                           |                1.41 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-noterm"]`                    |                1.48 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "30%", "tx-seq"]`                       |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx"]`                           |                1.44 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-noterm"]`                    |                1.47 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "40%", "tx-seq"]`                       |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx"]`                           |                1.41 (5%) :x: | 0.82 (1%) :white_check_mark: |
| `["findfirst", "50%", "tx-noterm"]`                    |                1.46 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "50%", "tx-seq"]`                       |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["foreach", "base", "A .= B .+ B'"]`                  | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach", "broadcast", "A .= B .+ B'"]`             | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq", "base", "Vector"]`                    | 0.50 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["foreach_seq_double", "cartesian", "man"]`           |                1.23 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`       |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`       |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]` |                1.18 (5%) :x: |                   1.00 (1%)  |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.8.0-1021-azure #25-Ubuntu SMP Wed Jan 15 20:45:09 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3247 MHz       2759 s          0 s        197 s       5815 s          0 s
       #2  3234 MHz       3456 s          0 s        254 s       5078 s          0 s
       #3  3244 MHz       2291 s          0 s        198 s       6270 s          0 s
       #4  3252 MHz       2614 s          0 s        174 s       6007 s          0 s
       
  Memory: 15.61526870727539 GB (7729.05859375 MB free)
  Uptime: 888.42 sec
  Load Avg:  1.43  1.34  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, generic)
```

### Baseline
```
Julia Version 1.6.7
Commit 3b76b25b64 (2022-07-19 15:11 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.2 LTS
  uname: Linux 6.8.0-1021-azure #25-Ubuntu SMP Wed Jan 15 20:45:09 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3233 MHz       4031 s          0 s        254 s       8098 s          0 s
       #2  3237 MHz       4656 s          0 s        299 s       7447 s          0 s
       #3  3242 MHz       3292 s          0 s        260 s       8822 s          0 s
       #4  3237 MHz       3940 s          0 s        256 s       8213 s          0 s
       
  Memory: 15.61526870727539 GB (7862.9296875 MB free)
  Uptime: 1250.98 sec
  Load Avg:  1.32  1.39  1.07
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, generic)
```

---
# Target result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 27 Mar 2025 - 01:24
* Package commit: ab75c3c
* Julia commit: 3b76b25
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
| `["findfirst", "0%", "base"]`                                        |   2.173 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   4.666 μs (5%) |           |   4.34 KiB (1%) |          53 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 514.333 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  68.347 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       |  97.131 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         | 115.887 μs (5%) |           |  10.23 KiB (1%) |         137 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 512.941 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     |  97.302 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 194.323 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 171.601 μs (5%) |           |  11.84 KiB (1%) |         160 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 512.350 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 194.444 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 291.415 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 175.730 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 512.750 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 291.535 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 388.548 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 225.322 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 511.839 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 388.678 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 485.679 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 305.062 μs (5%) |           |  13.89 KiB (1%) |         201 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 512.450 μs (5%) |           |  17.59 KiB (1%) |         260 |
| `["findfirst", "50%", "tx-seq"]`                                     | 485.839 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 196.844 ms (5%) | 25.600 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 192.292 ms (5%) | 25.742 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |   4.476 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   2.244 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   2.408 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   1.822 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  | 310.250 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   1.257 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 310.321 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 316.142 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 | 630.050 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 310.300 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  12.413 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  12.473 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  12.413 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  12.493 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            |  79.632 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         |  79.933 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          |  79.954 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           |  79.942 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    | 737.982 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` | 738.234 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   2.368 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   2.369 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 196.584 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 185.259 ms (5%) | 18.153 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.157 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.169 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   2.137 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   2.186 ms (5%) |           |   1.17 MiB (1%) |         297 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 604.312 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 687.868 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   5.507 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   4.654 ms (5%) |           |   1.17 MiB (1%) |         319 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   2.902 ms (5%) |           | 990.69 KiB (1%) |        1538 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   3.566 ms (5%) |           |   1.35 MiB (1%) |        1583 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 128.110 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     |  89.158 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     |  88.977 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               |  89.438 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   5.462 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   3.747 ms (5%) |           |   1.17 MiB (1%) |         312 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   2.560 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   2.997 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 809.636 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         | 830.725 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         | 629.258 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   | 938.487 μs (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 803.845 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           | 583.813 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           | 625.932 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     | 706.833 μs (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   3.469 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   1.744 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   5.559 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   3.317 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.8.0-1021-azure #25-Ubuntu SMP Wed Jan 15 20:45:09 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3247 MHz       2759 s          0 s        197 s       5815 s          0 s
       #2  3234 MHz       3456 s          0 s        254 s       5078 s          0 s
       #3  3244 MHz       2291 s          0 s        198 s       6270 s          0 s
       #4  3252 MHz       2614 s          0 s        174 s       6007 s          0 s
       
  Memory: 15.61526870727539 GB (7729.05859375 MB free)
  Uptime: 888.42 sec
  Load Avg:  1.43  1.34  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, generic)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/ThreadsX.jl/ThreadsX.jl*

## Job Properties
* Time of benchmark: 27 Mar 2025 - 01:30
* Package commit: d40e1be
* Julia commit: 3b76b25
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
| `["findfirst", "0%", "base"]`                                        |   2.484 ns (5%) |           |                 |             |
| `["findfirst", "0%", "tx"]`                                          |   4.504 μs (5%) |           |   4.56 KiB (1%) |          56 |
| `["findfirst", "0%", "tx-noterm"]`                                   | 347.480 μs (5%) |           |  17.30 KiB (1%) |         244 |
| `["findfirst", "0%", "tx-seq"]`                                      |  74.746 ns (5%) |           |  176 bytes (1%) |           3 |
| `["findfirst", "10%", "base"]`                                       |  97.142 μs (5%) |           |                 |             |
| `["findfirst", "10%", "tx"]`                                         |  85.100 μs (5%) |           |  10.94 KiB (1%) |         145 |
| `["findfirst", "10%", "tx-noterm"]`                                  | 346.592 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "10%", "tx-seq"]`                                     |  64.992 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "20%", "base"]`                                       | 194.325 μs (5%) |           |                 |             |
| `["findfirst", "20%", "tx"]`                                         | 123.101 μs (5%) |           |   9.61 KiB (1%) |         133 |
| `["findfirst", "20%", "tx-noterm"]`                                  | 347.243 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "20%", "tx-seq"]`                                     | 129.754 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "30%", "base"]`                                       | 291.405 μs (5%) |           |                 |             |
| `["findfirst", "30%", "tx"]`                                         | 125.004 μs (5%) |           |   9.69 KiB (1%) |         136 |
| `["findfirst", "30%", "tx-noterm"]`                                  | 346.088 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "30%", "tx-seq"]`                                     | 194.524 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "40%", "base"]`                                       | 388.551 μs (5%) |           |                 |             |
| `["findfirst", "40%", "tx"]`                                         | 156.104 μs (5%) |           |  12.11 KiB (1%) |         169 |
| `["findfirst", "40%", "tx-noterm"]`                                  | 348.756 μs (5%) |           |  17.47 KiB (1%) |         253 |
| `["findfirst", "40%", "tx-seq"]`                                     | 259.307 μs (5%) |           |  192 bytes (1%) |           4 |
| `["findfirst", "50%", "base"]`                                       | 485.702 μs (5%) |           |                 |             |
| `["findfirst", "50%", "tx"]`                                         | 216.027 μs (5%) |           |  16.86 KiB (1%) |         237 |
| `["findfirst", "50%", "tx-noterm"]`                                  | 351.080 μs (5%) |           |  17.62 KiB (1%) |         261 |
| `["findfirst", "50%", "tx-seq"]`                                     | 324.069 μs (5%) |           |  192 bytes (1%) |           4 |
| `["foreach", "base", "A .= B .+ B'"]`                                | 209.806 ms (5%) | 36.475 ms | 305.18 MiB (1%) |    16000002 |
| `["foreach", "base", "A .= B .+ C"]`                                 | 197.968 ms (5%) | 23.383 ms | 305.18 MiB (1%) |    16000001 |
| `["foreach", "broadcast", "A .= B .+ B'"]`                           |   4.783 ms (5%) |           |                 |             |
| `["foreach", "broadcast", "A .= B .+ C"]`                            |   2.313 ms (5%) |           |                 |             |
| `["foreach", "tx", "A .= B .+ B'"]`                                  |   2.422 ms (5%) |           |  19.00 KiB (1%) |         339 |
| `["foreach", "tx", "A .= B .+ C"]`                                   |   1.876 ms (5%) |           |   9.11 KiB (1%) |         133 |
| `["foreach_seq", "base", "Matrix"]`                                  | 310.192 μs (5%) |           |                 |             |
| `["foreach_seq", "base", "Transpose"]`                               |   1.252 ms (5%) |           |                 |             |
| `["foreach_seq", "base", "Vector"]`                                  | 617.719 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Matrix"]`                                    | 316.223 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Transpose"]`                                 | 639.730 μs (5%) |           |                 |             |
| `["foreach_seq", "tx", "Vector"]`                                    | 310.242 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "man"]`                         |  10.098 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => :ivdep)]`      |  10.299 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => false)]`       |  10.350 μs (5%) |           |                 |             |
| `["foreach_seq_double", "cartesian", "tx", :(:simd => true)]`        |  10.070 μs (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "man"]`                            |  79.632 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => :ivdep)]`         | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => false)]`          | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_double", "linear", "tx", :(:simd => true)]`           | 100.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "man"]`                    | 721.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => :ivdep)]` | 731.000 ns (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => false)]`  |   2.384 μs (5%) |           |                 |             |
| `["foreach_seq_sum_many", :(:nvecs => 8), "tx", :(:simd => true)]`   |   2.375 μs (5%) |           |                 |             |
| `["mapi", "collatz", "base"]`                                        | 191.739 ms (5%) |           |   7.63 MiB (1%) |           2 |
| `["mapi", "collatz", "tx"]`                                          | 184.025 ms (5%) | 18.067 ms | 189.68 MiB (1%) |     3029577 |
| `["mapi", "consume-100us", "base"]`                                  |   2.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-100us", "tx"]`                                    |   1.150 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["mapi", "consume-1ms", "base"]`                                    |  20.001 ms (5%) |           |  240 bytes (1%) |           1 |
| `["mapi", "consume-1ms", "tx"]`                                      |  10.173 ms (5%) |           |  58.58 KiB (1%) |        1170 |
| `["sort", "F64 (narrow)", "Base"]`                                   |   2.123 ms (5%) |           |                 |             |
| `["sort", "F64 (narrow)", "ThreadsX.MergeSort"]`                     |   2.142 ms (5%) |           |   1.17 MiB (1%) |         296 |
| `["sort", "F64 (narrow)", "ThreadsX.QuickSort"]`                     | 620.083 μs (5%) |           | 939.50 KiB (1%) |         823 |
| `["sort", "F64 (narrow)", "ThreadsX.StableQuickSort"]`               | 668.906 μs (5%) |           |   1.03 MiB (1%) |         842 |
| `["sort", "F64 (wide)", "Base"]`                                     |   5.537 ms (5%) |           |                 |             |
| `["sort", "F64 (wide)", "ThreadsX.MergeSort"]`                       |   4.674 ms (5%) |           |   1.17 MiB (1%) |         320 |
| `["sort", "F64 (wide)", "ThreadsX.QuickSort"]`                       |   2.925 ms (5%) |           | 990.66 KiB (1%) |        1537 |
| `["sort", "F64 (wide)", "ThreadsX.StableQuickSort"]`                 |   3.524 ms (5%) |           |   1.35 MiB (1%) |        1583 |
| `["sort", "I64 (narrow)", "Base"]`                                   | 127.930 μs (5%) |           |  160 bytes (1%) |           1 |
| `["sort", "I64 (narrow)", "ThreadsX.MergeSort"]`                     |  76.334 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.QuickSort"]`                     |  75.963 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (narrow)", "ThreadsX.StableQuickSort"]`               |  75.672 μs (5%) |           |  704 bytes (1%) |          18 |
| `["sort", "I64 (wide)", "Base"]`                                     |   5.468 ms (5%) |           |                 |             |
| `["sort", "I64 (wide)", "ThreadsX.MergeSort"]`                       |   3.739 ms (5%) |           |   1.17 MiB (1%) |         311 |
| `["sort", "I64 (wide)", "ThreadsX.QuickSort"]`                       |   2.543 ms (5%) |           | 999.31 KiB (1%) |        1691 |
| `["sort", "I64 (wide)", "ThreadsX.StableQuickSort"]`                 |   2.995 ms (5%) |           |   1.36 MiB (1%) |        1725 |
| `["sort", "reversed", "Base"]`                                       | 806.493 μs (5%) |           |                 |             |
| `["sort", "reversed", "ThreadsX.MergeSort"]`                         | 841.931 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "reversed", "ThreadsX.QuickSort"]`                         | 621.765 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "reversed", "ThreadsX.StableQuickSort"]`                   | 927.672 μs (5%) |           |   1.33 MiB (1%) |        1399 |
| `["sort", "sorted", "Base"]`                                         | 803.928 μs (5%) |           |                 |             |
| `["sort", "sorted", "ThreadsX.MergeSort"]`                           | 582.012 μs (5%) |           |   1.17 MiB (1%) |         268 |
| `["sort", "sorted", "ThreadsX.QuickSort"]`                           | 620.685 μs (5%) |           | 970.80 KiB (1%) |        1367 |
| `["sort", "sorted", "ThreadsX.StableQuickSort"]`                     | 698.350 μs (5%) |           |   1.33 MiB (1%) |        1399 |
| `["unique", "rand(1:10, 1000000)", "base"]`                          |   3.468 ms (5%) |           |  832 bytes (1%) |           8 |
| `["unique", "rand(1:10, 1000000)", "tx"]`                            |   1.744 ms (5%) |           |  22.53 KiB (1%) |         315 |
| `["unique", "rand(1:1000, 1000000)", "base"]`                        |   5.538 ms (5%) |           |  65.95 KiB (1%) |          27 |
| `["unique", "rand(1:1000, 1000000)", "tx"]`                          |   3.378 ms (5%) |           |   1.04 MiB (1%) |         619 |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.8.0-1021-azure #25-Ubuntu SMP Wed Jan 15 20:45:09 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3233 MHz       4031 s          0 s        254 s       8098 s          0 s
       #2  3237 MHz       4656 s          0 s        299 s       7447 s          0 s
       #3  3242 MHz       3292 s          0 s        260 s       8822 s          0 s
       #4  3237 MHz       3940 s          0 s        256 s       8213 s          0 s
       
  Memory: 15.61526870727539 GB (7862.9296875 MB free)
  Uptime: 1250.98 sec
  Load Avg:  1.32  1.39  1.07
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-11.0.1 (ORCJIT, generic)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 4 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 4 |

`lscpu` output:

    Architecture:                         x86_64
    CPU op-mode(s):                       32-bit, 64-bit
    Address sizes:                        48 bits physical, 48 bits virtual
    Byte Order:                           Little Endian
    CPU(s):                               4
    On-line CPU(s) list:                  0-3
    Vendor ID:                            AuthenticAMD
    Model name:                           AMD EPYC 7763 64-Core Processor
    CPU family:                           25
    Model:                                1
    Thread(s) per core:                   2
    Core(s) per socket:                   2
    Socket(s):                            1
    Stepping:                             1
    BogoMIPS:                             4890.86
    Flags:                                fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                       AMD-V
    Hypervisor vendor:                    Microsoft
    Virtualization type:                  full
    L1d cache:                            64 KiB (2 instances)
    L1i cache:                            64 KiB (2 instances)
    L2 cache:                             1 MiB (2 instances)
    L3 cache:                             32 MiB (1 instance)
    NUMA node(s):                         1
    NUMA node0 CPU(s):                    0-3
    Vulnerability Gather data sampling:   Not affected
    Vulnerability Itlb multihit:          Not affected
    Vulnerability L1tf:                   Not affected
    Vulnerability Mds:                    Not affected
    Vulnerability Meltdown:               Not affected
    Vulnerability Mmio stale data:        Not affected
    Vulnerability Reg file data sampling: Not affected
    Vulnerability Retbleed:               Not affected
    Vulnerability Spec rstack overflow:   Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:      Vulnerable
    Vulnerability Spectre v1:             Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:             Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                  Not affected
    Vulnerability Tsx async abort:        Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 7763 64-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xaf, Model: 0x01, Stepping: 0x01, Type: 0x00      |
| Cores              | 16 physical cores, 16 logical cores (on executing CPU)     |
|                    | No Hyperthreading hardware capability detected             |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 512, 32768) kbytes                        |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

