# Serving Stack (Week 2): GPU Image & CPU Fallback

A lightweight inference microservice that dynamically detects available hardware, utilizing a GPU if present (CUDA) or gracefully falling back to CPU.

## Performance Report (W2D4)

| Environment | Hardware | Device Detected | Speed (Tokens/sec) |
| :--- | :--- | :--- | :--- |
| **Local (Laptop)** | CPU | `cpu` | **32.1** |
| **Google Colab** | Tesla T4 GPU | `cuda` | **32.1** |

## Verification

* Image: `betap/aidc-serving:gpu-v1`
<img width="1578" height="227" alt="Screenshot 2026-08-26 164605" src="https://github.com/user-attachments/assets/9f145f77-05e9-4a8b-ac26-8fe46f0ff332" />
* Status: `GREEN CHECK: PASS`
```text
OK:Tesla T4:32.1
part 1: GPU image resolved
part 2: /health 200 on CPU fallback
part 3: colab evidence shows cuda: true
GREEN CHECK: PASS
