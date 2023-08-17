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
