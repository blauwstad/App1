# App1

## Local AI development

This project is set up to be worked on with a **local** model — Qwen3.8-27B
(MLX 8-bit) served by mlx-dspark, driven through DeepSeek Harness. Nothing is
sent to a cloud provider.

```bash
# start the engine once (~40s, loads 29.5 GB)
cd /Users/vahdetd/local-ai && make engine

# work in this project
/Users/vahdetd/local-ai/app1.sh web        # UI at http://127.0.0.1:3080
/Users/vahdetd/local-ai/app1.sh ask "..."  # one-shot
```

The first agent turn after starting the engine takes ~40s (prompt prefill);
every turn after is ~1.4s thanks to the prefix cache.
