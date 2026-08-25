# Serving Stack (Week 2): OpenAI-Compatible CPU Inference Service

A lightweight, production-structured inference microservice built with FastAPI and Hugging Face Transformers. It serves the `Qwen/Qwen2.5-0.5B-Instruct` model behind an OpenAI-compatible `/v1` HTTP API contract entirely on CPU.

## Container Size Report (W2D3)

| Stage | Image Tag / Build | Compressed (Pull) Size | Disk (Uncompressed) Size |
| :--- | :--- | :--- | :--- |
| **Naive Build** | `aidc-serving:naive` | ~6.89 GB | ~17.9 GB |
| **Slim Build** | `betap/aidc-serving:cpu-v1` | ~627 MB | ~3.02 GB |

## Verification

* Image: `betap/aidc-serving:cpu-v1`
<img width="1323" height="90" alt="Screenshot 2026-08-25 165753" src="https://github.com/user-attachments/assets/2fbe5f84-b0c9-4183-9c69-1ab996640ba2" />

* Status: `GREEN CHECK: PASS`
<img width="1356" height="199" alt="Screenshot 2026-08-25 165541" src="https://github.com/user-attachments/assets/32462834-4c67-44f8-8cc1-0a043e865fc1" />
