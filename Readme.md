# Buias-Guided Prompt Search (BGPS)

Official repository for the paper "Exposing Hidden Biases in Text-to-Image Models via Automated Prompt Search" (Accepted at the ICLR 2026 Workshop for Algorithmic Fairness Across Alignment Procedures and Agentic Systems).

---

## 📄 Paper Information

- **Title**: Exposing Hidden Biases in Text-to-Image Models via Automated Prompt Search
- **Authors**: Manos Plitsis, Georgios Bouritsas, Vassilis Katsouros, Yannis Panagakis
- **arXiv**: [https://arxiv.org/abs/2512.08724](https://arxiv.org/abs/2512.08724)

---

## 🧠 Overview

Text-to-image (TTI) diffusion models have achieved remarkable visual quality, yet they have been repeatedly shown to exhibit social biases across sensitive attributes such as gender, race and age. To mitigate these biases, existing approaches frequently depend on curated prompt datasets - either manually constructed or generated with large language models (LLMs) - as part of their training and/or evaluation procedures. Beside the curation cost, this also risks overlooking unanticipated, less obvious prompts that trigger biased generation, even in models that have undergone debiasing. In this work, we introduce Bias-Guided Prompt Search (BGPS), a framework that automatically generates prompts that aim to maximize the presence of biases in the resulting images. BGPS comprises two components: (1) an LLM instructed to produce attribute-neutral prompts and (2) attribute classifiers acting on the TTI’s internal representations that steer the decoding process of the LLM toward regions of the prompt space that amplify the image attributes of interest. We conduct extensive experiments on Stable Diffusion 1.5 and a state-of-the-art debiased model and discover an array of subtle and previously undocumented biases that severely deteriorate fairness metrics. Crucially, the discovered prompts are interpretable, i.e they may be entered by a typical user, quantitatively improving the perplexity metric compared to a prominent hard prompt optimization counterpart. Our findings uncover TTI vulnerabilities, while BGPS expands the bias search space and can act as a new evaluation tool for bias mitigation.

---

## 🛠️ Installation

On an environment with Python 3.11.13, install required packages using:

```bash
pip install -r requirements.txt
```

---

## 🚀 Getting Started

To run inference:

```bash
python ./bgps/inference_bias.py --config ./bgps/config/{taskname}.yaml
```

- Replace `{taskname}` with the name of the YAML config for your desired task.

---

This repository is based on the [VGD repository](https://github.com/DonghoonKim-1938/VGD).

