# Lab W3D4: Quantise and Lock the Model
## Predictions

* **VRAM Usage (`nvidia-smi`):** Predicted to be **about the same**. The weights are smaller, but vLLM allocates the freed memory to expand the KV cache based on `--gpu-memory-utilization 0.85`.
* **Tokens/s:** Predicted to be **about the same or faster**, thanks to vLLM using fused AWQ kernels for efficient 4-bit computation.
* **Smoke Test:** Predicted to pass the gate (>= 8/10).

## Locked Model Results

* **Model ID:** `Qwen/Qwen2.5-1.5B-Instruct-AWQ`
* **Smoke Score:** 10/10 

## Verification (Green Check)

<img width="477" height="123" alt="Screenshot 2026-09-02 145215" src="https://github.com/user-attachments/assets/11f1db07-8255-4410-8c6b-e12297a17865" />
