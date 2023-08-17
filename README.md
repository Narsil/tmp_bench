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



# TGI: 1.0.1

![Screenshot from 2023-08-17 16-46-11](https://github.com/Narsil/tmp_bench/assets/204321/8beff53d-b7d6-4eb0-825f-ed5279d0e8ca)


```
| Parameter          | Value                               |
|--------------------|-------------------------------------|
| Model              | hf-internal-testing/llama-tokenizer |
| Sequence Length    | 10                                  |
| Decode Length      | 8                                   |
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
| Prefill        | 1          | 31.74 ms  | 31.68 ms  | 31.94 ms  | 31.73 ms  | 31.94 ms  | 31.94 ms  |
|                | 2          | 36.25 ms  | 36.16 ms  | 36.38 ms  | 36.23 ms  | 36.38 ms  | 36.38 ms  |
|                | 4          | 39.14 ms  | 39.03 ms  | 39.27 ms  | 39.12 ms  | 39.27 ms  | 39.27 ms  |
|                | 8          | 43.12 ms  | 43.00 ms  | 43.32 ms  | 43.12 ms  | 43.32 ms  | 43.32 ms  |
|                | 16         | 62.20 ms  | 61.99 ms  | 62.40 ms  | 62.24 ms  | 62.40 ms  | 62.40 ms  |
|                | 32         | 101.91 ms | 101.64 ms | 102.48 ms | 101.93 ms | 102.48 ms | 102.48 ms |
| Decode (token) | 1          | 30.42 ms  | 30.37 ms  | 30.49 ms  | 30.43 ms  | 30.40 ms  | 30.40 ms  |
|                | 2          | 30.60 ms  | 30.51 ms  | 30.68 ms  | 30.63 ms  | 30.68 ms  | 30.68 ms  |
|                | 4          | 30.95 ms  | 30.89 ms  | 31.02 ms  | 30.96 ms  | 31.02 ms  | 31.02 ms  |
|                | 8          | 31.58 ms  | 31.48 ms  | 31.68 ms  | 31.59 ms  | 31.48 ms  | 31.48 ms  |
|                | 16         | 33.12 ms  | 33.08 ms  | 33.18 ms  | 33.13 ms  | 33.15 ms  | 33.15 ms  |
|                | 32         | 37.99 ms  | 37.91 ms  | 38.11 ms  | 37.99 ms  | 38.11 ms  | 38.11 ms  |
| Decode (total) | 1          | 212.94 ms | 212.57 ms | 213.41 ms | 213.00 ms | 212.83 ms | 212.83 ms |
|                | 2          | 214.20 ms | 213.56 ms | 214.75 ms | 214.41 ms | 214.74 ms | 214.74 ms |
|                | 4          | 216.66 ms | 216.25 ms | 217.11 ms | 216.74 ms | 217.11 ms | 217.11 ms |
|                | 8          | 221.07 ms | 220.40 ms | 221.73 ms | 221.10 ms | 220.40 ms | 220.40 ms |
|                | 16         | 231.86 ms | 231.56 ms | 232.29 ms | 231.93 ms | 232.02 ms | 232.02 ms |
|                | 32         | 265.93 ms | 265.39 ms | 266.74 ms | 265.95 ms | 266.74 ms | 266.74 ms |


| Step    | Batch Size | Average            | Lowest             | Highest            |
|---------|------------|--------------------|--------------------|--------------------|
| Prefill | 1          | 31.50 tokens/secs  | 31.31 tokens/secs  | 31.57 tokens/secs  |
|         | 2          | 55.18 tokens/secs  | 54.98 tokens/secs  | 55.31 tokens/secs  |
|         | 4          | 102.21 tokens/secs | 101.85 tokens/secs | 102.47 tokens/secs |
|         | 8          | 185.51 tokens/secs | 184.69 tokens/secs | 186.06 tokens/secs |
|         | 16         | 257.23 tokens/secs | 256.40 tokens/secs | 258.09 tokens/secs |
|         | 32         | 314.00 tokens/secs | 312.26 tokens/secs | 314.84 tokens/secs |
| Decode  | 1          | 32.87 tokens/secs  | 32.80 tokens/secs  | 32.93 tokens/secs  |
|         | 2          | 65.36 tokens/secs  | 65.19 tokens/secs  | 65.55 tokens/secs  |
|         | 4          | 129.24 tokens/secs | 128.97 tokens/secs | 129.48 tokens/secs |
|         | 8          | 253.31 tokens/secs | 252.55 tokens/secs | 254.08 tokens/secs |
|         | 16         | 483.05 tokens/secs | 482.16 tokens/secs | 483.69 tokens/secs |
|         | 32         | 842.32 tokens/secs | 839.76 tokens/secs | 844.04 tokens/secs |
```

# Pretty much identical to before the commit.

# TOP TOKENS NUM_SHARD=4 (no topk)

![Screenshot from 2023-08-17 16-52-22](https://github.com/Narsil/tmp_bench/assets/204321/19abde7a-cd39-4632-b7d7-2a812dbf530c)

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
| Prefill        | 1          | 18.92 ms  | 17.01 ms  | 32.72 ms  | 17.27 ms  | 32.72 ms  | 32.72 ms  |
|                | 2          | 18.17 ms  | 17.59 ms  | 18.50 ms  | 18.38 ms  | 18.50 ms  | 18.50 ms  |
|                | 4          | 24.14 ms  | 22.77 ms  | 35.50 ms  | 22.90 ms  | 35.50 ms  | 35.50 ms  |
|                | 8          | 32.14 ms  | 31.80 ms  | 32.46 ms  | 32.10 ms  | 32.46 ms  | 32.46 ms  |
|                | 16         | 51.67 ms  | 51.30 ms  | 52.04 ms  | 51.77 ms  | 52.04 ms  | 52.04 ms  |
|                | 32         | 91.98 ms  | 91.37 ms  | 92.54 ms  | 92.03 ms  | 92.54 ms  | 92.54 ms  |
| Decode (token) | 1          | 16.34 ms  | 15.81 ms  | 17.64 ms  | 16.46 ms  | 15.97 ms  | 15.97 ms  |
|                | 2          | 16.64 ms  | 15.94 ms  | 19.89 ms  | 16.38 ms  | 16.30 ms  | 16.30 ms  |
|                | 4          | 16.59 ms  | 15.61 ms  | 19.94 ms  | 16.29 ms  | 16.19 ms  | 16.19 ms  |
|                | 8          | 17.21 ms  | 16.64 ms  | 19.92 ms  | 16.97 ms  | 17.02 ms  | 17.02 ms  |
|                | 16         | 18.00 ms  | 17.64 ms  | 20.75 ms  | 17.71 ms  | 17.75 ms  | 17.75 ms  |
|                | 32         | 22.09 ms  | 21.55 ms  | 23.90 ms  | 21.66 ms  | 23.90 ms  | 23.90 ms  |
| Decode (total) | 1          | 114.40 ms | 110.67 ms | 123.45 ms | 115.22 ms | 111.82 ms | 111.82 ms |
|                | 2          | 116.50 ms | 111.59 ms | 139.23 ms | 114.66 ms | 114.07 ms | 114.07 ms |
|                | 4          | 116.16 ms | 109.26 ms | 139.59 ms | 114.03 ms | 113.32 ms | 113.32 ms |
|                | 8          | 120.50 ms | 116.47 ms | 139.44 ms | 118.79 ms | 119.11 ms | 119.11 ms |
|                | 16         | 126.02 ms | 123.46 ms | 145.29 ms | 123.97 ms | 124.26 ms | 124.26 ms |
|                | 32         | 154.60 ms | 150.88 ms | 167.27 ms | 151.60 ms | 167.27 ms | 167.27 ms |


| Step    | Batch Size | Average             | Lowest              | Highest             |
|---------|------------|---------------------|---------------------|---------------------|
| Prefill | 1          | 54.85 tokens/secs   | 30.56 tokens/secs   | 58.78 tokens/secs   |
|         | 2          | 110.11 tokens/secs  | 108.13 tokens/secs  | 113.69 tokens/secs  |
|         | 4          | 168.66 tokens/secs  | 112.69 tokens/secs  | 175.63 tokens/secs  |
|         | 8          | 248.95 tokens/secs  | 246.46 tokens/secs  | 251.55 tokens/secs  |
|         | 16         | 309.66 tokens/secs  | 307.43 tokens/secs  | 311.86 tokens/secs  |
|         | 32         | 347.92 tokens/secs  | 345.81 tokens/secs  | 350.24 tokens/secs  |
| Decode  | 1          | 61.27 tokens/secs   | 56.70 tokens/secs   | 63.25 tokens/secs   |
|         | 2          | 120.62 tokens/secs  | 100.55 tokens/secs  | 125.46 tokens/secs  |
|         | 4          | 242.18 tokens/secs  | 200.59 tokens/secs  | 256.27 tokens/secs  |
|         | 8          | 465.87 tokens/secs  | 401.61 tokens/secs  | 480.82 tokens/secs  |
|         | 16         | 890.81 tokens/secs  | 770.87 tokens/secs  | 907.16 tokens/secs  |
|         | 32         | 1451.01 tokens/secs | 1339.13 tokens/secs | 1484.66 tokens/secs |
```

# TOP TOKENS NUM_SHARD=4 (topk=10)

![Screenshot from 2023-08-17 16-53-27](https://github.com/Narsil/tmp_bench/assets/204321/95ed77e3-bc92-4559-8378-ac7a7e157fff)

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
| Prefill        | 1          | 18.55 ms  | 17.10 ms  | 26.86 ms  | 17.81 ms  | 26.86 ms  | 26.86 ms  |
|                | 2          | 18.47 ms  | 18.27 ms  | 18.77 ms  | 18.42 ms  | 18.77 ms  | 18.77 ms  |
|                | 4          | 23.64 ms  | 23.45 ms  | 23.79 ms  | 23.65 ms  | 23.79 ms  | 23.79 ms  |
|                | 8          | 33.56 ms  | 32.92 ms  | 37.31 ms  | 33.24 ms  | 37.31 ms  | 37.31 ms  |
|                | 16         | 53.63 ms  | 52.92 ms  | 56.90 ms  | 53.36 ms  | 56.90 ms  | 56.90 ms  |
|                | 32         | 93.87 ms  | 92.57 ms  | 97.46 ms  | 93.34 ms  | 97.46 ms  | 97.46 ms  |
| Decode (token) | 1          | 16.90 ms  | 15.98 ms  | 20.77 ms  | 16.57 ms  | 16.31 ms  | 16.31 ms  |
|                | 2          | 17.62 ms  | 16.01 ms  | 22.14 ms  | 16.61 ms  | 22.08 ms  | 22.08 ms  |
|                | 4          | 17.60 ms  | 16.49 ms  | 22.42 ms  | 17.50 ms  | 16.63 ms  | 16.63 ms  |
|                | 8          | 18.38 ms  | 16.74 ms  | 22.56 ms  | 18.08 ms  | 16.94 ms  | 16.94 ms  |
|                | 16         | 20.17 ms  | 19.44 ms  | 23.31 ms  | 19.57 ms  | 19.44 ms  | 19.44 ms  |
|                | 32         | 25.37 ms  | 24.65 ms  | 27.48 ms  | 24.79 ms  | 27.48 ms  | 27.48 ms  |
| Decode (total) | 1          | 118.31 ms | 111.85 ms | 145.37 ms | 116.03 ms | 114.19 ms | 114.19 ms |
|                | 2          | 123.31 ms | 112.08 ms | 154.97 ms | 116.28 ms | 154.53 ms | 154.53 ms |
|                | 4          | 123.19 ms | 115.42 ms | 156.96 ms | 122.52 ms | 116.44 ms | 116.44 ms |
|                | 8          | 128.64 ms | 117.16 ms | 157.90 ms | 126.53 ms | 118.56 ms | 118.56 ms |
|                | 16         | 141.20 ms | 136.06 ms | 163.17 ms | 137.00 ms | 136.07 ms | 136.07 ms |
|                | 32         | 177.57 ms | 172.52 ms | 192.39 ms | 173.52 ms | 192.39 ms | 192.39 ms |


| Step    | Batch Size | Average             | Lowest              | Highest             |
|---------|------------|---------------------|---------------------|---------------------|
| Prefill | 1          | 54.79 tokens/secs   | 37.23 tokens/secs   | 58.49 tokens/secs   |
|         | 2          | 108.30 tokens/secs  | 106.56 tokens/secs  | 109.44 tokens/secs  |
|         | 4          | 169.20 tokens/secs  | 168.10 tokens/secs  | 170.54 tokens/secs  |
|         | 8          | 238.65 tokens/secs  | 214.39 tokens/secs  | 243.02 tokens/secs  |
|         | 16         | 298.44 tokens/secs  | 281.17 tokens/secs  | 302.33 tokens/secs  |
|         | 32         | 340.96 tokens/secs  | 328.32 tokens/secs  | 345.70 tokens/secs  |
| Decode  | 1          | 59.48 tokens/secs   | 48.15 tokens/secs   | 62.58 tokens/secs   |
|         | 2          | 115.12 tokens/secs  | 90.34 tokens/secs   | 124.91 tokens/secs  |
|         | 4          | 228.95 tokens/secs  | 178.39 tokens/secs  | 242.59 tokens/secs  |
|         | 8          | 439.06 tokens/secs  | 354.64 tokens/secs  | 477.96 tokens/secs  |
|         | 16         | 796.42 tokens/secs  | 686.38 tokens/secs  | 823.16 tokens/secs  |
|         | 32         | 1263.31 tokens/secs | 1164.31 tokens/secs | 1298.37 tokens/secs |
```

# Almost negligible slowdown

# TGI:1.0.1 NUM_SHARD=4

![Screenshot from 2023-08-17 16-48-59](https://github.com/Narsil/tmp_bench/assets/204321/2c694340-2462-431a-ac72-d795f810a0e1)

```
| Parameter          | Value                               |
|--------------------|-------------------------------------|
| Model              | hf-internal-testing/llama-tokenizer |
| Sequence Length    | 10                                  |
| Decode Length      | 8                                   |
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
| Prefill        | 1          | 17.33 ms  | 16.65 ms  | 17.68 ms  | 17.50 ms  | 17.68 ms  | 17.68 ms  |
|                | 2          | 19.45 ms  | 17.74 ms  | 33.72 ms  | 17.89 ms  | 33.72 ms  | 33.72 ms  |
|                | 4          | 22.94 ms  | 22.80 ms  | 23.22 ms  | 22.91 ms  | 23.22 ms  | 23.22 ms  |
|                | 8          | 32.19 ms  | 31.99 ms  | 32.50 ms  | 32.13 ms  | 32.50 ms  | 32.50 ms  |
|                | 16         | 52.58 ms  | 52.10 ms  | 55.61 ms  | 52.21 ms  | 55.61 ms  | 55.61 ms  |
|                | 32         | 91.19 ms  | 90.54 ms  | 91.79 ms  | 91.25 ms  | 91.79 ms  | 91.79 ms  |
| Decode (token) | 1          | 16.35 ms  | 15.65 ms  | 18.50 ms  | 16.27 ms  | 16.12 ms  | 16.12 ms  |
|                | 2          | 16.12 ms  | 15.76 ms  | 16.44 ms  | 16.15 ms  | 16.06 ms  | 16.06 ms  |
|                | 4          | 16.95 ms  | 15.96 ms  | 20.06 ms  | 16.73 ms  | 16.04 ms  | 16.04 ms  |
|                | 8          | 16.85 ms  | 16.17 ms  | 20.05 ms  | 16.44 ms  | 16.17 ms  | 16.17 ms  |
|                | 16         | 17.89 ms  | 17.62 ms  | 19.04 ms  | 17.72 ms  | 17.70 ms  | 17.70 ms  |
|                | 32         | 22.17 ms  | 21.67 ms  | 24.35 ms  | 21.70 ms  | 24.35 ms  | 24.35 ms  |
| Decode (total) | 1          | 114.45 ms | 109.57 ms | 129.50 ms | 113.89 ms | 112.87 ms | 112.87 ms |
|                | 2          | 112.85 ms | 110.34 ms | 115.07 ms | 113.06 ms | 112.45 ms | 112.45 ms |
|                | 4          | 118.63 ms | 111.71 ms | 140.42 ms | 117.09 ms | 112.29 ms | 112.29 ms |
|                | 8          | 117.95 ms | 113.19 ms | 140.32 ms | 115.08 ms | 113.19 ms | 113.19 ms |
|                | 16         | 125.25 ms | 123.34 ms | 133.28 ms | 124.04 ms | 123.94 ms | 123.94 ms |
|                | 32         | 155.17 ms | 151.67 ms | 170.46 ms | 151.89 ms | 170.46 ms | 170.46 ms |


| Step    | Batch Size | Average             | Lowest              | Highest             |
|---------|------------|---------------------|---------------------|---------------------|
| Prefill | 1          | 57.72 tokens/secs   | 56.57 tokens/secs   | 60.05 tokens/secs   |
|         | 2          | 106.69 tokens/secs  | 59.31 tokens/secs   | 112.73 tokens/secs  |
|         | 4          | 174.39 tokens/secs  | 172.28 tokens/secs  | 175.46 tokens/secs  |
|         | 8          | 248.51 tokens/secs  | 246.17 tokens/secs  | 250.08 tokens/secs  |
|         | 16         | 304.40 tokens/secs  | 287.72 tokens/secs  | 307.12 tokens/secs  |
|         | 32         | 350.92 tokens/secs  | 348.63 tokens/secs  | 353.44 tokens/secs  |
| Decode  | 1          | 61.28 tokens/secs   | 54.06 tokens/secs   | 63.88 tokens/secs   |
|         | 2          | 124.07 tokens/secs  | 121.66 tokens/secs  | 126.88 tokens/secs  |
|         | 4          | 237.39 tokens/secs  | 199.40 tokens/secs  | 250.65 tokens/secs  |
|         | 8          | 476.60 tokens/secs  | 399.09 tokens/secs  | 494.72 tokens/secs  |
|         | 16         | 894.63 tokens/secs  | 840.35 tokens/secs  | 908.02 tokens/secs  |
|         | 32         | 1446.07 tokens/secs | 1314.11 tokens/secs | 1476.89 tokens/secs |
```


###################################################################################### FALCON 40B

# TOPK: NUM_SHARD=4 (topk=0)
![Screenshot from 2023-08-17 17-06-42](https://github.com/Narsil/tmp_bench/assets/204321/7cff19be-2b9b-4d79-a8c6-e0e7d03fc209)

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
| Prefill        | 1          | 62.30 ms  | 62.09 ms  | 62.66 ms  | 62.30 ms  | 62.66 ms  | 62.66 ms  |
|                | 2          | 63.99 ms  | 63.83 ms  | 64.36 ms  | 63.93 ms  | 64.36 ms  | 64.36 ms  |
|                | 4          | 70.99 ms  | 70.83 ms  | 71.33 ms  | 71.02 ms  | 71.33 ms  | 71.33 ms  |
|                | 8          | 87.55 ms  | 87.36 ms  | 87.73 ms  | 87.57 ms  | 87.73 ms  | 87.73 ms  |
|                | 16         | 134.49 ms | 134.07 ms | 135.32 ms | 134.45 ms | 135.32 ms | 135.32 ms |
|                | 32         | 255.67 ms | 254.54 ms | 257.07 ms | 255.73 ms | 257.07 ms | 257.07 ms |
| Decode (token) | 1          | 50.29 ms  | 50.16 ms  | 50.50 ms  | 50.26 ms  | 50.50 ms  | 50.50 ms  |
|                | 2          | 55.95 ms  | 55.81 ms  | 56.07 ms  | 55.97 ms  | 55.95 ms  | 55.95 ms  |
|                | 4          | 57.72 ms  | 57.63 ms  | 57.79 ms  | 57.71 ms  | 57.77 ms  | 57.77 ms  |
|                | 8          | 61.19 ms  | 61.11 ms  | 61.29 ms  | 61.22 ms  | 61.16 ms  | 61.16 ms  |
|                | 16         | 65.29 ms  | 65.17 ms  | 65.58 ms  | 65.29 ms  | 65.19 ms  | 65.19 ms  |
|                | 32         | 67.53 ms  | 67.47 ms  | 67.67 ms  | 67.54 ms  | 67.67 ms  | 67.67 ms  |
| Decode (total) | 1          | 352.01 ms | 351.16 ms | 353.52 ms | 351.79 ms | 353.52 ms | 353.52 ms |
|                | 2          | 391.67 ms | 390.70 ms | 392.49 ms | 391.76 ms | 391.65 ms | 391.65 ms |
|                | 4          | 404.04 ms | 403.43 ms | 404.56 ms | 403.98 ms | 404.43 ms | 404.43 ms |
|                | 8          | 428.37 ms | 427.76 ms | 429.03 ms | 428.53 ms | 428.09 ms | 428.09 ms |
|                | 16         | 457.03 ms | 456.22 ms | 459.07 ms | 457.02 ms | 456.36 ms | 456.36 ms |
|                | 32         | 472.73 ms | 472.30 ms | 473.71 ms | 472.80 ms | 473.71 ms | 473.71 ms |


| Step    | Batch Size | Average            | Lowest             | Highest            |
|---------|------------|--------------------|--------------------|--------------------|
| Prefill | 1          | 16.05 tokens/secs  | 15.96 tokens/secs  | 16.11 tokens/secs  |
|         | 2          | 31.26 tokens/secs  | 31.07 tokens/secs  | 31.33 tokens/secs  |
|         | 4          | 56.35 tokens/secs  | 56.08 tokens/secs  | 56.48 tokens/secs  |
|         | 8          | 91.37 tokens/secs  | 91.18 tokens/secs  | 91.57 tokens/secs  |
|         | 16         | 118.97 tokens/secs | 118.24 tokens/secs | 119.34 tokens/secs |
|         | 32         | 125.16 tokens/secs | 124.48 tokens/secs | 125.72 tokens/secs |
| Decode  | 1          | 19.89 tokens/secs  | 19.80 tokens/secs  | 19.93 tokens/secs  |
|         | 2          | 35.74 tokens/secs  | 35.67 tokens/secs  | 35.83 tokens/secs  |
|         | 4          | 69.30 tokens/secs  | 69.21 tokens/secs  | 69.40 tokens/secs  |
|         | 8          | 130.73 tokens/secs | 130.53 tokens/secs | 130.91 tokens/secs |
|         | 16         | 245.06 tokens/secs | 243.97 tokens/secs | 245.49 tokens/secs |
|         | 32         | 473.84 tokens/secs | 472.87 tokens/secs | 474.27 tokens/secs |
```

# TOPK: NUM_SHARD=4 (topk=10)
![Screenshot from 2023-08-17 17-04-34](https://github.com/Narsil/tmp_bench/assets/204321/415b7976-e3fb-48af-a93f-2064d0a0307b)

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
| Prefill        | 1          | 62.77 ms  | 62.59 ms  | 63.14 ms  | 62.74 ms  | 63.14 ms  | 63.14 ms  |
|                | 2          | 64.45 ms  | 64.14 ms  | 66.05 ms  | 64.28 ms  | 66.05 ms  | 66.05 ms  |
|                | 4          | 71.01 ms  | 70.79 ms  | 71.34 ms  | 71.02 ms  | 71.34 ms  | 71.34 ms  |
|                | 8          | 86.73 ms  | 86.47 ms  | 87.23 ms  | 86.66 ms  | 87.23 ms  | 87.23 ms  |
|                | 16         | 135.05 ms | 134.27 ms | 136.82 ms | 134.79 ms | 136.82 ms | 136.82 ms |
|                | 32         | 255.83 ms | 254.56 ms | 258.12 ms | 255.83 ms | 258.12 ms | 258.12 ms |
| Decode (token) | 1          | 50.78 ms  | 50.52 ms  | 51.12 ms  | 50.82 ms  | 50.70 ms  | 50.70 ms  |
|                | 2          | 56.41 ms  | 56.23 ms  | 56.61 ms  | 56.41 ms  | 56.34 ms  | 56.34 ms  |
|                | 4          | 58.37 ms  | 58.11 ms  | 58.70 ms  | 58.49 ms  | 58.70 ms  | 58.70 ms  |
|                | 8          | 61.74 ms  | 61.55 ms  | 61.96 ms  | 61.84 ms  | 61.60 ms  | 61.60 ms  |
|                | 16         | 66.17 ms  | 66.01 ms  | 66.44 ms  | 66.14 ms  | 66.36 ms  | 66.36 ms  |
|                | 32         | 69.02 ms  | 68.82 ms  | 69.30 ms  | 68.98 ms  | 69.30 ms  | 69.30 ms  |
| Decode (total) | 1          | 355.46 ms | 353.63 ms | 357.86 ms | 355.73 ms | 354.94 ms | 354.94 ms |
|                | 2          | 394.88 ms | 393.59 ms | 396.29 ms | 394.84 ms | 394.37 ms | 394.37 ms |
|                | 4          | 408.63 ms | 406.77 ms | 410.94 ms | 409.42 ms | 410.92 ms | 410.92 ms |
|                | 8          | 432.19 ms | 430.82 ms | 433.72 ms | 432.86 ms | 431.18 ms | 431.18 ms |
|                | 16         | 463.17 ms | 462.05 ms | 465.12 ms | 462.99 ms | 464.53 ms | 464.53 ms |
|                | 32         | 483.15 ms | 481.76 ms | 485.09 ms | 482.89 ms | 485.09 ms | 485.09 ms |


| Step    | Batch Size | Average            | Lowest             | Highest            |
|---------|------------|--------------------|--------------------|--------------------|
| Prefill | 1          | 15.93 tokens/secs  | 15.84 tokens/secs  | 15.98 tokens/secs  |
|         | 2          | 31.04 tokens/secs  | 30.28 tokens/secs  | 31.18 tokens/secs  |
|         | 4          | 56.33 tokens/secs  | 56.07 tokens/secs  | 56.51 tokens/secs  |
|         | 8          | 92.25 tokens/secs  | 91.71 tokens/secs  | 92.52 tokens/secs  |
|         | 16         | 118.48 tokens/secs | 116.94 tokens/secs | 119.16 tokens/secs |
|         | 32         | 125.08 tokens/secs | 123.97 tokens/secs | 125.71 tokens/secs |
| Decode  | 1          | 19.69 tokens/secs  | 19.56 tokens/secs  | 19.79 tokens/secs  |
|         | 2          | 35.45 tokens/secs  | 35.33 tokens/secs  | 35.57 tokens/secs  |
|         | 4          | 68.52 tokens/secs  | 68.14 tokens/secs  | 68.83 tokens/secs  |
|         | 8          | 129.57 tokens/secs | 129.11 tokens/secs | 129.99 tokens/secs |
|         | 16         | 241.81 tokens/secs | 240.80 tokens/secs | 242.40 tokens/secs |
|         | 32         | 463.63 tokens/secs | 461.77 tokens/secs | 464.96 tokens/secs |
```

# Negligible slowdown

![Screenshot from 2023-08-17 17-14-25](https://github.com/Narsil/tmp_bench/assets/204321/745f9a8f-c34b-4685-831d-6e9475d285f9)

```

| Parameter          | Value                               |
|--------------------|-------------------------------------|
| Model              | hf-internal-testing/llama-tokenizer |
| Sequence Length    | 10                                  |
| Decode Length      | 8                                   |
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
| Prefill        | 1          | 62.17 ms  | 62.02 ms  | 62.38 ms  | 62.15 ms  | 62.38 ms  | 62.38 ms  |
|                | 2          | 63.74 ms  | 63.53 ms  | 64.05 ms  | 63.75 ms  | 64.05 ms  | 64.05 ms  |
|                | 4          | 70.50 ms  | 70.10 ms  | 71.48 ms  | 70.48 ms  | 71.48 ms  | 71.48 ms  |
|                | 8          | 87.31 ms  | 87.06 ms  | 87.50 ms  | 87.33 ms  | 87.50 ms  | 87.50 ms  |
|                | 16         | 133.08 ms | 132.60 ms | 133.51 ms | 133.22 ms | 133.51 ms | 133.51 ms |
|                | 32         | 254.05 ms | 252.50 ms | 255.26 ms | 254.25 ms | 255.26 ms | 255.26 ms |
| Decode (token) | 1          | 50.24 ms  | 50.16 ms  | 50.36 ms  | 50.26 ms  | 50.36 ms  | 50.36 ms  |
|                | 2          | 55.95 ms  | 55.75 ms  | 56.46 ms  | 55.94 ms  | 55.88 ms  | 55.88 ms  |
|                | 4          | 57.63 ms  | 57.54 ms  | 57.90 ms  | 57.60 ms  | 57.65 ms  | 57.65 ms  |
|                | 8          | 61.08 ms  | 60.91 ms  | 61.34 ms  | 61.11 ms  | 60.91 ms  | 60.91 ms  |
|                | 16         | 65.10 ms  | 65.01 ms  | 65.23 ms  | 65.08 ms  | 65.19 ms  | 65.19 ms  |
|                | 32         | 67.44 ms  | 67.37 ms  | 67.59 ms  | 67.42 ms  | 67.59 ms  | 67.59 ms  |
| Decode (total) | 1          | 351.71 ms | 351.15 ms | 352.54 ms | 351.84 ms | 352.54 ms | 352.54 ms |
|                | 2          | 391.64 ms | 390.24 ms | 395.24 ms | 391.57 ms | 391.19 ms | 391.19 ms |
|                | 4          | 403.38 ms | 402.80 ms | 405.28 ms | 403.20 ms | 403.55 ms | 403.55 ms |
|                | 8          | 427.58 ms | 426.39 ms | 429.41 ms | 427.80 ms | 426.39 ms | 426.39 ms |
|                | 16         | 455.69 ms | 455.10 ms | 456.58 ms | 455.58 ms | 456.36 ms | 456.36 ms |
|                | 32         | 472.05 ms | 471.61 ms | 473.12 ms | 471.98 ms | 473.12 ms | 473.12 ms |


| Step    | Batch Size | Average            | Lowest             | Highest            |
|---------|------------|--------------------|--------------------|--------------------|
| Prefill | 1          | 16.08 tokens/secs  | 16.03 tokens/secs  | 16.12 tokens/secs  |
|         | 2          | 31.38 tokens/secs  | 31.23 tokens/secs  | 31.48 tokens/secs  |
|         | 4          | 56.74 tokens/secs  | 55.96 tokens/secs  | 57.06 tokens/secs  |
|         | 8          | 91.63 tokens/secs  | 91.42 tokens/secs  | 91.89 tokens/secs  |
|         | 16         | 120.23 tokens/secs | 119.84 tokens/secs | 120.67 tokens/secs |
|         | 32         | 125.96 tokens/secs | 125.36 tokens/secs | 126.73 tokens/secs |
| Decode  | 1          | 19.90 tokens/secs  | 19.86 tokens/secs  | 19.93 tokens/secs  |
|         | 2          | 35.75 tokens/secs  | 35.42 tokens/secs  | 35.88 tokens/secs  |
|         | 4          | 69.41 tokens/secs  | 69.09 tokens/secs  | 69.51 tokens/secs  |
|         | 8          | 130.97 tokens/secs | 130.41 tokens/secs | 131.34 tokens/secs |
|         | 16         | 245.78 tokens/secs | 245.30 tokens/secs | 246.10 tokens/secs |
|         | 32         | 474.53 tokens/secs | 473.45 tokens/secs | 474.97 tokens/secs |
```
