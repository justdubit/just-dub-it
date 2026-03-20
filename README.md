
<div align="right">
  <details>
    <summary >🌐 Language</summary>
    <div>
      <div align="center">
        <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=en">English</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=zh-CN">简体中文</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=zh-TW">繁體中文</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=ja">日本語</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=ko">한국어</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=hi">हिन्दी</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=th">ไทย</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=fr">Français</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=de">Deutsch</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=es">Español</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=it">Italiano</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=ru">Русский</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=pt">Português</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=nl">Nederlands</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=pl">Polski</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=ar">العربية</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=fa">فارسی</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=tr">Türkçe</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=vi">Tiếng Việt</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=id">Bahasa Indonesia</a>
        | <a href="https://openaitx.github.io/view.html?user=justdubit&project=just-dub-it&lang=as">অসমীয়া</
      </div>
    </div>
  </details>
</div>

# JustDubit: Video Dubbing via Joint Audio-Visual Diffusion

[![Website](https://img.shields.io/badge/Project-Page-181717?logo=google-chrome)](https://justdubit.github.io)
[![Model](https://img.shields.io/badge/HuggingFace-Model-orange?logo=huggingface)](https://huggingface.co/justdubit/justdubit)
[![Dataset](https://img.shields.io/badge/HuggingFace-Dataset-blue?logo=huggingface)](https://huggingface.co/datasets/justdubit/audiovisual_translation_dub/settings)

## 📰 News

- [2026/02/10] 🔥 Code, checkpoints, and data released
- [2026/01/29] 🔥 Tech report released


---

## 📄 Abstract

Audio-Visual Foundation Models, which are pretrained to jointly generate sound and visual content, have recently shown an unprecedented ability to model multi-modal generation and editing, opening new opportunities for downstream tasks.

Among these tasks, video dubbing could greatly benefit from such priors, yet most existing solutions still rely on complex, task-specific pipelines that struggle in real-world settings.

In this work, we introduce a single-model approach that adapts a foundational audio-video diffusion model for video-to-video dubbing via a lightweight LoRA. The LoRA enables the model to condition on an input audio-video while jointly generating translated audio and synchronized facial motion.

To train this LoRA, we leverage the generative model itself to synthesize paired multilingual videos of the same speaker. Specifically, we generate multilingual videos with language switches within a single clip, and then inpaint the face and audio in each half to match the language of the other half.

By leveraging the rich generative prior of the audio-visual model, our approach preserves speaker identity and lip synchronization while remaining robust to complex motion and real-world dynamics. We demonstrate that our approach produces high-quality dubbed videos with improved visual fidelity, lip synchronization, and robustness compared to existing dubbing pipelines.

---

## 🚀 Quick Links

| Resource | Description |
|----------|-------------|
| [**Inference Pipeline**](packages/ltx-pipelines/README.md) | Run video dubbing with the JustDubit pipeline |
| [**Training Guide**](packages/ltx-trainer/README.md) | Train your own JustDubit LoRA |

---

## 📦 Repository Structure

```
just-dub-it/
├── packages/
│   ├── ltx-pipelines/     # Inference pipeline for video dubbing
│   │   └── README.md      # Pipeline usage guide
│   ├── ltx-trainer/       # Training tools for JustDubit LoRA
│   │   └── README.md      # Training guide
│   └── ltx-core/          # Core model components
└── README.md              # This file
```

---

## 🎬 Inference

See the [Pipeline README](packages/ltx-pipelines/README.md) for:
- Installation instructions
- Model checkpoint downloads
- Prompt format guide
- CLI arguments reference

---

## 🏋️ Training

See the [Trainer README](packages/ltx-trainer/README.md) for:
- Dataset download and preparation
- Preprocessing pipeline
- Training configuration
- Multi-GPU training setup


