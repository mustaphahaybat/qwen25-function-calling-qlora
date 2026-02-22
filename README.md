# 🤖 Fine-Tuning Qwen2.5-3B for Function Calling with QLoRA

Fine-tuning a small LLM to improve tool/function calling accuracy
using QLoRA on Google Colab Free Tier (T4 GPU).

## 📊 Results

| Config | Overall | Tool-call | Loss |
|--------|---------|-----------|------|
| Base model | 80.0% | 29.6% | - |
| steps=120, lr=2e-4 | 93.0% | 85.2% | 0.521 |
| steps=60, lr=2e-4 | 90.0% | 70.4% | 0.396 |

**Key improvement: Tool-call accuracy 29.6% → 85.2% (+55.6%) 🚀**

## 🛠️ Setup

- **Model:** Qwen2.5-3B-Instruct (4-bit quantized)
- **Technique:** QLoRA (LoRA r=16) — only 0.96% of parameters trained
- **Dataset:** glaiveai/glaive-function-calling-v2 (2,500 train / 200 eval)
- **Hardware:** Google Colab Free Tier (T4 GPU, 15.6GB VRAM)
- **Framework:** Unsloth + TRL SFTTrainer

## 🚀 Quick Start

Open directly in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/YOUR_USERNAME/qwen25-function-calling-qlora/blob/main/qwen25_function_calling_qlora.ipynb)

## 📁 Structure
```
├── qwen25_function_calling_qlora.ipynb  # Main notebook
└── README.md
```

## 🔑 Key Findings

1. QLoRA trains only 0.96% of parameters but achieves +55.6% improvement
2. Balanced evaluation set is critical for meaningful metrics
3. steps=120 optimal — more steps showed diminishing returns
4. Full training completed in 13 minutes on free T4 GPU

## 👤 Author

**Mustafa Haybat Gözgöz**  
[LinkedIn](https://www.linkedin.com/in/mustafa-haybat-gozgoz35)
