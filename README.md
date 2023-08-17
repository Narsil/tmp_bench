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

