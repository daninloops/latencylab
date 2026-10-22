# LatencyLab

Automated inference optimization and benchmarking for vision models.

LatencyLab exports a vision model to ONNX, runs it through different backends
and precisions, and measures what each optimization actually costs: latency
(p50/p95/p99), throughput, and accuracy.

## Why
A trained model is not a deployable model. Optimization is usually done
ad hoc and its accuracy cost rarely measured. LatencyLab automates the
pipeline and quantifies the tradeoff.

## Status
In development. Started October 2026.

## Roadmap
- [ ] PyTorch to ONNX export with numerical verification
- [ ] Benchmark harness (warmup, p50/p95/p99)
- [ ] SQLite result storage
- [ ] REST API (FastAPI)
- [ ] Docker + CI
- [ ] TensorRT backend, FP16/INT8 (on Colab T4)
- [ ] Accuracy-vs-latency dashboard

## Setup
    py -3.11 -m venv .venv
    .venv\Scripts\Activate.ps1
    pip install -r requirements.txt
    pip install -e .
