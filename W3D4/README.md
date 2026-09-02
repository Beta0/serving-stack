# Lab W3D4: Quantise and Lock the Model

This repository contains the results of the Week 3 Day 4 lab, where we served a 4-bit AWQ quantized model and validated its function-calling capabilities.

## Predictions

* **VRAM Usage (`nvidia-smi`):** Predicted to be **about the same**. The weights are smaller, but vLLM allocates the freed memory to expand the KV cache based on `--gpu-memory-utilization 0.85`.
* **Tokens/s:** Predicted to be **about the same or faster**, thanks to vLLM using fused AWQ kernels for efficient 4-bit computation.
* **Smoke Test:** Predicted to pass the gate (>= 8/10).

## Locked Model Results

* **Model ID:** `Qwen/Qwen2.5-1.5B-Instruct-AWQ`
* **Smoke Score:** 10/10 (Perfect score with full distractor compliance)

## Verification (Green Check)

The endpoint passed the function-calling smoke test and the configuration is fully locked. Below is the verification proof:

<!-- أضف صورة العلامة الخضراء (Green Check) تحت هذا السطر مباشرة -->
![Green Check](ضع_رابط_أو_مسار_الصورة_هنا)