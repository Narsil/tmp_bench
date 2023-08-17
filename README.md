top_tokens_llama2_7b_shard_1.txt

![Screenshot from 2023-08-17 16-30-50](https://github.com/Narsil/tmp_bench/assets/204321/57bb9ed8-7cc2-4b9a-8903-44fea0c159c4)

```
| Parameter          | Value                               |
|--------------------|-------------------------------------|
| Model              | hf-internal-testing/llama-tokenizer |
| Sequence Length    | 10                                  |
| Decode Length      | 8                                   |
| Top N Tokens       | None                                |
| N Runs             | 10                                  |
| Warmups            | 1                                   |
| Temperature        | None                                |
| Top K              | None                                |
| Top P              | None                                |
| Typical P          | None                                |
| Repetition Penalty | None                                |
| Watermark          | false                               |
| Do Sample          | false                               |


| Step           | Batch Size | Average   | Lowest    | Highest   | p50       | p90       | p99       |
|----------------|------------|-----------|-----------|-----------|-----------|-----------|-----------|
| Prefill        | 1          | 31.83 ms  | 31.74 ms  | 31.94 ms  | 31.83 ms  | 31.94 ms  | 31.94 ms  |
|                | 2          | 36.30 ms  | 36.18 ms  | 36.37 ms  | 36.34 ms  | 36.37 ms  | 36.37 ms  |
|                | 4          | 39.11 ms  | 38.98 ms  | 39.53 ms  | 39.06 ms  | 39.53 ms  | 39.53 ms  |
|                | 8          | 42.74 ms  | 42.64 ms  | 42.93 ms  | 42.72 ms  | 42.93 ms  | 42.93 ms  |
|                | 16         | 61.67 ms  | 61.52 ms  | 61.91 ms  | 61.67 ms  | 61.91 ms  | 61.91 ms  |
|                | 32         | 101.30 ms | 101.12 ms | 101.56 ms | 101.30 ms | 101.56 ms | 101.56 ms |
| Decode (token) | 1          | 30.45 ms  | 30.40 ms  | 30.51 ms  | 30.45 ms  | 30.51 ms  | 30.51 ms  |
|                | 2          | 30.58 ms  | 30.53 ms  | 30.62 ms  | 30.59 ms  | 30.53 ms  | 30.53 ms  |
|                | 4          | 30.94 ms  | 30.83 ms  | 31.19 ms  | 30.94 ms  | 30.83 ms  | 30.83 ms  |
|                | 8          | 31.40 ms  | 31.35 ms  | 31.51 ms  | 31.40 ms  | 31.42 ms  | 31.42 ms  |
|                | 16         | 32.89 ms  | 32.83 ms  | 32.95 ms  | 32.89 ms  | 32.95 ms  | 32.95 ms  |
|                | 32         | 37.73 ms  | 37.66 ms  | 37.81 ms  | 37.73 ms  | 37.81 ms  | 37.81 ms  |
| Decode (total) | 1          | 213.18 ms | 212.81 ms | 213.60 ms | 213.19 ms | 213.60 ms | 213.60 ms |
|                | 2          | 214.05 ms | 213.73 ms | 214.38 ms | 214.13 ms | 213.73 ms | 213.73 ms |
|                | 4          | 216.57 ms | 215.83 ms | 218.33 ms | 216.61 ms | 215.83 ms | 215.83 ms |
|                | 8          | 219.82 ms | 219.46 ms | 220.59 ms | 219.78 ms | 219.96 ms | 219.96 ms |
|                | 16         | 230.22 ms | 229.82 ms | 230.67 ms | 230.26 ms | 230.67 ms | 230.67 ms |
|                | 32         | 264.14 ms | 263.65 ms | 264.65 ms | 264.12 ms | 264.65 ms | 264.65 ms |


| Step    | Batch Size | Average            | Lowest             | Highest            |
|---------|------------|--------------------|--------------------|--------------------|
| Prefill | 1          | 31.42 tokens/secs  | 31.31 tokens/secs  | 31.51 tokens/secs  |
|         | 2          | 55.10 tokens/secs  | 54.99 tokens/secs  | 55.28 tokens/secs  |
|         | 4          | 102.27 tokens/secs | 101.18 tokens/secs | 102.63 tokens/secs |
|         | 8          | 187.18 tokens/secs | 186.35 tokens/secs | 187.62 tokens/secs |
|         | 16         | 259.45 tokens/secs | 258.44 tokens/secs | 260.07 tokens/secs |
|         | 32         | 315.90 tokens/secs | 315.08 tokens/secs | 316.46 tokens/secs |
| Decode  | 1          | 32.84 tokens/secs  | 32.77 tokens/secs  | 32.89 tokens/secs  |
|         | 2          | 65.40 tokens/secs  | 65.30 tokens/secs  | 65.50 tokens/secs  |
|         | 4          | 129.29 tokens/secs | 128.25 tokens/secs | 129.73 tokens/secs |
|         | 8          | 254.75 tokens/secs | 253.86 tokens/secs | 255.17 tokens/secs |
|         | 16         | 486.49 tokens/secs | 485.53 tokens/secs | 487.34 tokens/secs |
|         | 32         | 848.02 tokens/secs | 846.39 tokens/secs | 849.62 tokens/secs |
```

# With top_n_tokens

![Screenshot from 2023-08-17 16-35-24](https://github.com/Narsil/tmp_bench/assets/204321/6f0affa9-5adc-4e03-a205-ca2763b4b7fa)
```
| Parameter          | Value                               |
|--------------------|-------------------------------------|
| Model              | hf-internal-testing/llama-tokenizer |
| Sequence Length    | 10                                  |
| Decode Length      | 8                                   |
| Top N Tokens       | Some(10)                            |
| N Runs             | 10                                  |
| Warmups            | 1                                   |
| Temperature        | None                                |
| Top K              | None                                |
| Top P              | None                                |
| Typical P          | None                                |
| Repetition Penalty | None                                |
| Watermark          | false                               |
| Do Sample          | false                               |


| Step           | Batch Size | Average   | Lowest    | Highest   | p50       | p90       | p99       |
|----------------|------------|-----------|-----------|-----------|-----------|-----------|-----------|
| Prefill        | 1          | 32.47 ms  | 32.41 ms  | 32.59 ms  | 32.49 ms  | 32.59 ms  | 32.59 ms  |
|                | 2          | 37.19 ms  | 37.10 ms  | 37.45 ms  | 37.18 ms  | 37.45 ms  | 37.45 ms  |
|                | 4          | 40.44 ms  | 40.33 ms  | 40.60 ms  | 40.44 ms  | 40.60 ms  | 40.60 ms  |
|                | 8          | 45.24 ms  | 45.12 ms  | 45.46 ms  | 45.25 ms  | 45.46 ms  | 45.46 ms  |
|                | 16         | 66.26 ms  | 66.03 ms  | 66.75 ms  | 66.21 ms  | 66.75 ms  | 66.75 ms  |
|                | 32         | 109.81 ms | 109.50 ms | 110.22 ms | 109.81 ms | 110.22 ms | 110.22 ms |
| Decode (token) | 1          | 31.10 ms  | 31.06 ms  | 31.18 ms  | 31.10 ms  | 31.14 ms  | 31.14 ms  |
|                | 2          | 31.51 ms  | 31.48 ms  | 31.56 ms  | 31.52 ms  | 31.50 ms  | 31.50 ms  |
|                | 4          | 32.41 ms  | 32.34 ms  | 32.48 ms  | 32.41 ms  | 32.48 ms  | 32.48 ms  |
|                | 8          | 34.14 ms  | 34.05 ms  | 34.44 ms  | 34.10 ms  | 34.17 ms  | 34.17 ms  |
|                | 16         | 37.91 ms  | 37.78 ms  | 38.09 ms  | 37.94 ms  | 37.95 ms  | 37.95 ms  |
|                | 32         | 47.29 ms  | 47.14 ms  | 47.52 ms  | 47.24 ms  | 47.52 ms  | 47.52 ms  |
| Decode (total) | 1          | 217.73 ms | 217.40 ms | 218.24 ms | 217.70 ms | 218.01 ms | 218.01 ms |
|                | 2          | 220.61 ms | 220.37 ms | 220.92 ms | 220.64 ms | 220.47 ms | 220.47 ms |
|                | 4          | 226.90 ms | 226.40 ms | 227.37 ms | 226.90 ms | 227.37 ms | 227.37 ms |
|                | 8          | 238.97 ms | 238.32 ms | 241.08 ms | 238.72 ms | 239.18 ms | 239.18 ms |
|                | 16         | 265.39 ms | 264.50 ms | 266.63 ms | 265.56 ms | 265.63 ms | 265.63 ms |
|                | 32         | 331.00 ms | 329.97 ms | 332.67 ms | 330.67 ms | 332.67 ms | 332.67 ms |


| Step    | Batch Size | Average            | Lowest             | Highest            |
|---------|------------|--------------------|--------------------|--------------------|
| Prefill | 1          | 30.79 tokens/secs  | 30.69 tokens/secs  | 30.85 tokens/secs  |
|         | 2          | 53.77 tokens/secs  | 53.41 tokens/secs  | 53.90 tokens/secs  |
|         | 4          | 98.91 tokens/secs  | 98.52 tokens/secs  | 99.17 tokens/secs  |
|         | 8          | 176.82 tokens/secs | 175.99 tokens/secs | 177.30 tokens/secs |
|         | 16         | 241.48 tokens/secs | 239.70 tokens/secs | 242.31 tokens/secs |
|         | 32         | 291.42 tokens/secs | 290.33 tokens/secs | 292.25 tokens/secs |
| Decode  | 1          | 32.15 tokens/secs  | 32.07 tokens/secs  | 32.20 tokens/secs  |
|         | 2          | 63.46 tokens/secs  | 63.37 tokens/secs  | 63.53 tokens/secs  |
|         | 4          | 123.40 tokens/secs | 123.15 tokens/secs | 123.67 tokens/secs |
|         | 8          | 234.34 tokens/secs | 232.29 tokens/secs | 234.98 tokens/secs |
|         | 16         | 422.03 tokens/secs | 420.05 tokens/secs | 423.44 tokens/secs |
|         | 32         | 676.74 tokens/secs | 673.34 tokens/secs | 678.85 tokens/secs |
```

~25% slowdown at high batch sizes.
