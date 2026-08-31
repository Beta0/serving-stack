# Lab W3D2: Inference Anatomy, By Hand

## Predict (By Hand) - Main Lab
* TTFT (Time to First Token) with a longer prompt: Up.
* TPOT (mean gap between tokens) depends mostly on: prompt length.
* KV cache per token: 56 KB per token.
* KV cache for a 4096-token context: About 0.5 GB.
* Static batching finishes when the: longest prompt finishes.

GREEN CHECK:

<img width="608" height="120" alt="Screenshot-2026-08-31-140559" src="https://github.com/user-attachments/assets/ed847d72-48a5-4bf6-9f28-a9b1371d573e" />

## Predict (By Hand) - Extra Lab
* Fraction of unused reserved slab (4096 max vs 300 avg): Roughly 60% goes unused.
* Blocks needed for a 300-token sequence (block size 16): 18 blocks.
* Blocks needed for a 4096-token sequence (block size 16): 256 blocks.

GREEN CHECK:

<img width="768" height="89" alt="Screenshot-2026-08-31-140433" src="https://github.com/user-attachments/assets/014bc9fe-f28a-44d9-9674-ebf639139551" />
