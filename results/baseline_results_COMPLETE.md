
# BERT Baseline Optimization - COMPLETE RESULTS

**Date:** 2025-10-20
**Hardware:** Tesla T4
**Model:** bert-base-uncased (110M parameters)
**Precision:** FP32

## 1. Simple Text Benchmark
- Average Latency: 23.52 ms
- P95 Latency: 41.47 ms
- Throughput: 1332.91 sentences/second

## 2. IMDB Dataset (Sentiment Classification)
- Average Latency: 27.51 ms
- P95 Latency: 47.68 ms
- Dataset: Movie reviews (variable length)

## 3. SQuAD Dataset (Question Answering)
- Average Latency: 21.48 ms
- P95 Latency: 37.93 ms
- Dataset: Question-context pairs

## 4. Resource Utilization (PyTorch Profiler)
- Peak GPU Memory: 0.47 GB
- Model Parameters: 110M
- FP32 Model Size: ~440 MB

## Key Findings
- Latency varies with sequence length (expected)
- Real-world data (IMDB/SQuAD) slower than simple text
- GPU memory usage: ~0.47 GB
- Bottleneck: Attention computation (from profiler)

## Week 2 Optimization Targets
1. INT8 Quantization → Target: 2-3x speedup
2. FP16 Mixed Precision → Target: 1.5-2x speedup
3. ONNX Runtime → Target: 1.3-1.5x speedup
4. Combined → Target: **5-10x total speedup!**

---
*Tech Stack: PyTorch, CUDA, Transformers, Google Colab T4 GPU*
*Repository: github.com/YOUR_USERNAME/bert-optimization*
