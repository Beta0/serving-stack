# Lab W3D2: Inference Anatomy, By Hand

## Predict (By Hand) - Main Lab
* **TTFT (Time to First Token) with a longer prompt: Up.
* **TPOT (mean gap between tokens) depends mostly on: prompt length.
* **KV cache per token: 56 KB per token.
* **KV cache for a 4096-token context: About 0.5 GB.
* **Static batching finishes when the: longest prompt finishes.

GREEN CHECK:

![Green Check Pass](Screenshot-2026-08-31-140559.png)

## Predict (By Hand) - Extra Lab
* **Fraction of unused reserved slab (4096 max vs 300 avg): Roughly 60% goes unused.
* **Blocks needed for a 300-token sequence (block size 16): 18 blocks.
* **Blocks needed for a 4096-token sequence (block size 16): 256 blocks.

GREEN CHECK:

![Green Check Pass](Screenshot-2026-08-31-140433.png)
