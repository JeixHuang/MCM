<p align="center">
  <img src="assets/figs/logo.png"  height=120>
</p>


### <div align="center">⚔ Medical MLLM is Vulnerable: Cross-Modality Jailbreak and Mismatched Attacks on Medical Multimodal Large Language Models<div> 
### <div align="center"> AAAI 2025 <div> 

<div align="center">
  <!-- <a href="https://pixart-alpha.github.io/"><img src="https://img.shields.io/static/v1?label=Project%20Page&message=Github&color=blue&logo=github-pages"></a> &ensp; -->
  <a href="https://arxiv.org/abs/2405.20775"><img src="https://img.shields.io/static/v1?label=Paper&message=Arxiv:Alpha&color=red&logo=arxiv"></a> &ensp;
  <a href="https://huggingface.co/datasets/MedMLLM-attack/3MAD-Tiny-1K"><img src="https://img.shields.io/static/v1?label=3MAD-Tiny-1K&message=HF&color=yellow"></a> &ensp;
  <a href="https://huggingface.co/datasets/MedMLLM-attack/3MAD-66K"><img src="https://img.shields.io/static/v1?label=3MAD-66K&message=HF&color=yellow"></a> &ensp;
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-green" alt="License"></a> &ensp;
  <a href="https://www.python.org/downloads/release/python-370/"><img src="https://img.shields.io/badge/python-3.7%2B-blue" alt="Python Version"></a> &ensp;
</div>

---
## Breaking News 🔥🔥!!
- **🔥💥 `2024/12`:** Glad to announce that [MCM](https://arxiv.org/abs/2405.20775) is accepted by AAAI 2025.
- **🎉🎉 `2024/5`:**  We are excited to officially announce the open-sourcing of MCM.

## Abstract

Security concerns related to Large Language Models (LLMs) have been extensively explored; however, the safety implications for Multimodal Large Language Models (MLLMs), particularly in medical contexts (MedMLLMs), remain inadequately addressed. This paper investigates the security vulnerabilities of MedMLLMs, focusing on their deployment in clinical environments where the accuracy and relevance of question-and-answer interactions are crucial for addressing complex medical challenges. We introduce and redefine two attack types: mismatched malicious attack (2M-attack) and optimized mismatched malicious attack (O2M-attack), by integrating existing clinical data with atypical natural phenomena. 

Using the comprehensive 3MAD dataset that we developed, which spans a diverse range of medical imaging modalities and adverse medical scenarios, we performed an in-depth analysis and proposed the MCM optimization method. This approach significantly improves the attack success rate against MedMLLMs. Our evaluations, which include white-box attacks on LLaVA-Med and transfer (black-box) attacks on four other SOTA models, reveal that even MedMLLMs designed with advanced security mechanisms remain vulnerable to breaches. This study highlights the critical need for robust security measures to enhance the safety and reliability of open-source MedMLLMs, especially in light of the potential impact of jailbreak attacks and other malicious exploits in clinical applications. 
\textbf{Warning:} Medical jailbreaking may generate content that includes unverified diagnoses and treatment recommendations. Always consult professional medical advice.

## Methodlogy
The Multimodal Cross-Optimization (MCM) algorithm simultaneously optimizes both continuous image inputs (image w/ noise) and discrete text tokens (suffix) to jailbreak multimodal large language models into producing harmful content (jailbreaking answer). It does this by manipulating the input image (image w/o noise) with noise and appending specific text tokens to the query, aiming to maximize the likelihood of the model generating a harmful response to a malicious question
![MCM_chat](assets/figs/mcm_attack_chat.png)
![MCM](assets/figs/algorithm.png)



## Code and Dataset

<!-- Our code is available at [GitHub Repository](https://github.com/dirtycomputer/O2M_attack.git).


Our datasets are available at [3MAD-Tiny-1K](https://huggingface.co/datasets/MedMLLM-attack/3MAD-Tiny-1K), [3MAD-66K](https://huggingface.co/datasets/MedMLLM-attack/3MAD-66K). -->

Left: Components of images in the 3MAD (9 modalities and 12 body parts). Right: Components of
normal prompts in the 3MAD (18 medical tasks or requirements).
![3MAD](assets/figs/dataset_overview.png)




## Warning

Medical large model jailbreaking may generate content that includes unverified diagnoses and treatment recommendations. Always consult professional medical advice.

## Citation

If you find our work helpful, please consider citing the following paper:

```
@article{huang2024cross,
  title={Cross-Modality Jailbreak and Mismatched Attacks on Medical Multimodal Large Language Models},
  author={Huang, Xijie and Wang, Xinyuan and Zhang, Hantao and Xi, Jiawen and An, Jingkun and Wang, Hao and Pan, Chengwei},
  journal={arXiv preprint arXiv:2405.20775},
  year={2024}
}
```

# Acknowledgements
We acknowledge all the authors of the employed public datasets, allowing the community to use these valuable resources for research purposes. We also thank the authors of LLaVA-Med, GCG, and PGD for their significant research contributions.
