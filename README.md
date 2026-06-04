# Hi there, I'm Peng Rui (彭锐) 👋

🎓 **Joint-Training Master's Student** at **NERCITA** (National Engineering Research Center for Information Technology in Agriculture) & **Zhejiang A&F University**.

📧 **Email**: pengrui130@gmail.com |  📄 **CV**:https://drive.google.com/file/d/1yKBUXycMAl-Tc2pTSAd8Q-74h-keMZVN/view?usp=drive_link

---

## 🔍 Research Interests
My research focuses on the intersection of multimodal perception and efficient reasoning, specifically:
- **Multimodal Large Language Models (MLLMs)**: Cross-modal alignment, multimodal perception, and fine-grained controllability.
- **Computer Vision & Referring Segmentation**: Image/video referring segmentation, boundary consistency, and dense prediction algorithms.
- **Model Efficiency & Compression**: Training-free MLLM pruning and query-adaptive compute routing.

---

## 🚀 Featured Research Projects

### [SALMA: Structure-Aware Alignment Framework for Referring Image and Video Segmentation](Link-to-your-repo)
*Status: Under Review (CCF-A) | First Author*
- **Core Contribution**: Proposed **Mask-Biased Attention** and **Text-Mask Contrastive (TMC) Loss** to inject class-agnostic structural priors into cross-modal alignment, solving attention drift issues in MLLMs.
- **Performance**: Achieved **+3.4 J&F** on Ref-DAVIS17 and **+4.3** on MeVis compared to strong Sa2VA-1B baseline, with only ~0.7% inference latency overhead (17.84 FPS).
- **Engineering**: Implemented end-to-end training pipeline using PyTorch, LoRA, and DeepSpeed ZeRO-2 with BF16 mixed precision on a 4×RTX 5090 cluster.

### [QACR: Query-Adaptive Visual Token Compression for MLLMs](Link-to-your-repo)
*Status: Manuscript in Preparation | First Author*
- **Core Contribution**: A **training-free** query-adaptive token scoring mechanism combining attention saliency and query relevance, effectively compressing visual tokens without new checkpoints.
- **Performance**: Retained 97.75% of full-compute performance ($Avg.=0.7914$) at only 30% visual compute budget on Qwen3.5-VL-4B, outperforming VisionZip by **+14.74%**.
- **Engineering**: Designed depth-aware latter-layer pruning and established a matched-compute evaluation protocol across multiple benchmarks.

---

## 🛠️ Technical Skills & Infrastructure

- **Languages**: Python, C/C++, SQL, Shell.
- **Frameworks & Tools**: PyTorch, Hugging Face Transformers, PEFT/LoRA, DeepSpeed ZeRO, vLLM.
- **Infrastructure**: Experienced in environment deployment, GPU memory optimization, and experimental scheduling for multi-GPU high-end server clusters (**4× RTX 5090**).

---

## 🏆 Honors & Awards
- **2nd Prize**, National AI Application Scenario Innovation Challenge (2025.11).
- **Silver Award**, 18th "Challenge Cup" Extracurricular Academic and Technological Work Competition, Zhejiang Province (2023.06).

<!--
**pengrui-art/pengrui-art** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.
-->
