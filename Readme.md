# Buias-Guided Prompt Search (BGPS)



Official repository for the paper "Exposing Hidden Biases in Text-to-Image Models via Automated Prompt Search" (Accepted at the ICLR 2026 Workshop for Algorithmic Fairness Across Alignment Procedures and Agentic Systems).
<!-- 
<p align="center">
  <img src="./figure1.png" alt="Figure 1" width="600"/>
</p>

* While conventional prompt inversion techniques update prompt embeddings through gradient-based optimization and quantization, VGD is a gradient-free technique that utilizes large language models and CLIP to generate relevant sentences.

<p align="center">
  <img src="./figure2.png" alt="Figure 2" width="600"/>
</p> -->

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
cd bgps
python ./inference_bias.py --config ./config/{taskname}.yaml
```

- Replace `{taskname}` with the name of the YAML config for your desired task.
- See `./bgps/run.sh` for example CLI commands used in our experiments.

---



This repository is based on the [VGD repository](https://github.com/DonghoonKim-1938/VGD).



<!-- ## 📊 Key Results

### Figure 2: Prompt Generation Pipeline



*VGD generates initial prompts using an LLM and refines them using CLIP-based feedback to maximize visual similarity.*

### Figure 3: Qualitative Comparisons



*Compared to previous prompt inversion methods, VGD achieves higher visual alignment and interpretability.*

--- -->




<!-- 
## 👩‍💻 Authors

- **Donghoon Kim** – [dhkim@islab.snu.ac.kr](mailto\:byonghyo.shim@example.com)
- **Minji Bae** – [mjbae@islab.snu.ac.kr](mailto\:byonghyo.shim@example.com)
- **Kyuhong Shim** – [khshim@skku.edu](mailto\:byonghyo.shim@example.com)
- **Byonghyo Shim** – [bshim@islab.snu.ac.kr](mailto\:byonghyo.shim@example.com)

--- -->
<!-- 
## 📅 Citation

If you use this work, please cite our paper:

```bibtex
@inproceedings{kim2025visually,
  title={Visually Guided Decoding: Gradient-Free Hard Prompt Inversion with Language Models},
  author={Kim, Donghoon and Bae, Minji and Shim, Kyuhong and Shim, Byonghyo},
  booktitle={International Conference on Learning Representations (ICLR)},
  year={2025}
}
```

--- -->
<!-- 
## 📁 Directory Structure

```
vgd/
├── bluestar/
│   ├── data/
│   ├── losses/
│   ├── metrics/
│   ├── models/
│   ├── modules/
│   ├── nn/
│   ├── optim/
│   ├── utils/
│   ├── __init__.py
├── vgd/
│   ├── config/
│   │   ├── {taskname}.yaml
│   ├── run.sh
│   ├── inference.py
│   ├── wrapper.py
│   ├── run.sh
├── requirements.txt
├── README.md
```

---

## 📢 Contact

For questions or issues, feel free to open a GitHub issue or contact the authors directly.
 -->
