# Lab W3D3: The Engine Swap - vLLM vs Static Batching

This repository contains the results of the Week 3 Day 3 lab, comparing the performance of a static batching serving engine with vLLM using continuous batching and PagedAttention on a T4 GPU.

## Deliverables

### Prediction Card

Before running the load tests, the following predictions were recorded for how throughput would scale from concurrency 1 to 8:

*   **Static Batching Scaling (Monday):** ~3.0x
*   **vLLM Scaling (Predicted):** ~4.0x
*   **Rationale:** Static batching slot efficiency collapses under mixed output lengths, as short requests occupy memory until the longest request in the batch finishes. Continuous batching admits a waiting sequence on the next token step after a sequence finishes, avoiding this tax. Therefore, vLLM's scaling multiple should be **larger** than static batching's.

### Verification (Green Check)

The `verify_cell.py` script was executed against the generated `ab_report.json` to confirm the A/B test results and report schema.

```text
GREEN CHECK: PASS
```

### Key Results

At concurrency level 8, the following throughput (tokens/second) was observed:

*   **vLLM Throughput (concurrency 8):** 232.6 tokens/s (Recorded on the Progress Board)
