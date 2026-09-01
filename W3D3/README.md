# Lab W3D3: The Engine Swap

### Prediction Card
Before running the load tests, the following predictions were recorded for how throughput would scale from concurrency 1 to 8:
*   Static Batching Scaling (Monday): 3.0x
*   vLLM Scaling (Predicted): 4.0x
*   Rationale: Static batching slot efficiency collapses under mixed output lengths, as short requests occupy memory until the longest request in the batch finishes. Continuous batching admits a waiting sequence on the next token step after a sequence finishes, avoiding this tax. Therefore, vLLM's scaling multiple should be **larger** than static batching's.

### Verification (Green Check)

<img width="566" height="105" alt="Screenshot 2026-09-01 141856" src="https://github.com/user-attachments/assets/a2609d3b-47a5-4849-b4f4-321d9e76116a" />
