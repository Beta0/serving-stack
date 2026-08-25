# Serving Stack (Week 2): OpenAI-Compatible CPU Inference Service

A lightweight, production-structured inference microservice built with FastAPI and Hugging Face Transformers. It serves the `Qwen/Qwen2.5-0.5B-Instruct` model behind an OpenAI-compatible `/v1` HTTP API contract entirely on CPU.

## Container Size Report (W2D3)

| Stage | Image Tag / Build | Compressed (Pull) Size | Disk (Uncompressed) Size |
| :--- | :--- | :--- | :--- |
| **Naive Build** | `aidc-serving:naive` | ~6.89 GB | ~17.9 GB |
| **Slim Build** | `betap/aidc-serving:cpu-v1` | ~627 MB | ~3.02 GB |

## Verification

* Image: `betap/aidc-serving:cpu-v1`
* Status: `GREEN CHECK: PASS`

```text
pulling betap/aidc-serving:cpu-v1 ...
waiting for /health (up to 420s) ...
image: betap/aidc-serving:cpu-v1
health: 200
completion: ok
GREEN CHECK: PASS
