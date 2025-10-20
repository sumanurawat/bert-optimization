# BERT Production Optimization

Optimizing BERT inference for production deployment on NVIDIA GPUs.

## Project Goals
- Achieve 5-10x latency reduction through quantization and optimization
- Deploy production-ready FastAPI serving endpoint
- Document learnings for blog post

## Tech Stack
- PyTorch + CUDA
- Transformers (Hugging Face)
- TensorRT, ONNX Runtime
- FastAPI, Redis
- Docker

## Current Progress
- ✅ Week 1: Baseline benchmarking complete
- 🔄 Week 2: Quantization experiments
- 📅 Week 3: Production serving

## Results
See [baseline results](results/baseline_results.md)

## Setup
```bash
pip install torch transformers accelerate
```

## Usage
See notebooks for experiments and results.
