---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

I am a Distributed Training Engineer at [Beijing Academy of Artificial Intelligence (BAAI)](https://www.baai.ac.cn/english.html). Previously, I was an HPC Engineer at Baidu PaddlePaddle (2023–2024). I obtained my M.E. in Computer Technology from [Nankai University](https://www.nankai.edu.cn/) in 2023.

My work focuses on **large-scale distributed training systems** for frontier LLMs. I specialize in hybrid-parallelism strategies, high-performance kernel engineering (CUDA/Triton), and training infrastructure for Mixture-of-Experts and long-context multimodal models. I have been deeply involved in training systems for **DeepSeek V3/V4** and **BAAI EMU3.5**.


# 🔥 News
- *2025.04*: &nbsp; DualPipeV open-sourced and adopted by FlagScale for MoE pipeline parallelism.
- *2025.02*: &nbsp; Ring-Flex-Attention validated at 64K seq length for 32B multimodal models (EMU3.5).
- *2024.12*: &nbsp; MTP reference implementation cited by Alibaba PAI and upstream Megatron-LM.
- *2024.11*: &nbsp; Joined BAAI as Distributed Training Engineer.
- *2024.04*: &nbsp; **Hybrid-Memcached** accepted by IEEE Transactions on Computers (CCF-A).


# 📖 Educations
- *2020.09 – 2023.06*: M.E. in Computer Technology, Nankai University. Advisor: Prof. [Xiaoli Gong](https://cc.nankai.edu.cn/2019/0619/c13620a179396/page.htm).
- *2016.09 – 2020.06*: B.E. in Computer Science and Technology, China University of Mining and Technology.


# 👨‍💻 Work Experience

**Distributed Training Engineer, Beijing Academy of Artificial Intelligence (BAAI)** &nbsp; *Nov 2024 – Present*

Core contributor to DeepSeek V3/V4 and EMU3.5 training infrastructure. Leading performance optimization for sparse attention, MoE parallelism, and long-context multimodal training at scale on NVIDIA H100/A800 clusters.

**HPC Engineer, Baidu PaddlePaddle** &nbsp; *Jul 2023 – Nov 2024*

AI Infra engineer for ERNIE LLMs. Designed semi-auto parallelism distributed training, supporting full-chain hybrid parallel strategies (DP/TP/PP/SP) for Pretrain, SFT, and LoRA.


# 💻 Selected Projects

### DeepSeek V3/V4 Performance Optimization & Tuning &nbsp; *Dec 2024 – Present*
- **Sparse Attention for Long-Context Training**: Led CP tuning for DeepSeek V4's Hybrid Attention (CSA/HCA/Sliding-Window). Fused fragmented micro-ops into unified GEMMs and custom Triton kernels; overlapped P2P/All-Gather with computation via multi-stream execution; eliminated CPU-GPU sync bottlenecks; designed end-to-end CP infrastructure with cross-rank halo exchange and causal sparse top-K for 4×/128× compressed attention.
- **Multi-Token Predictor (MTP)**: Architected the inaugural DeepSeek V3 MTP module with custom pipeline parallelism. This reference design was later cited and adopted by Alibaba PAI and upstream Megatron-LM.
- **Engram Implementation**: Engineered AllGather-Based and All-to-All-Based Engram Embedding with CPU state offloading and asynchronous scheduling for large-scale training.
- **DualPipeV**: Engineered and open-sourced a pipeline parallelism strategy for MoE, achieving seamless overlap of all-to-all communication with forward/backward computation. Adopted by FlagScale.
- **Auxiliary-Loss-Free Load Balancing**: Independently reproduced DeepSeek V3's Sigmoid Router and Auxiliary-Loss-Free balancing from paper specifications; integrated MLA + Shared-Expert MoE for end-to-end training fidelity.
- **Production Infrastructure**: Delivered stable months-long training for DeepSeek V3-style MoE models across scales (16B-A3B and beyond) with fault-tolerant distributed checkpointing.

### EMU3.5: Efficient Long-Sequence Multimodal Training &nbsp; *Feb 2025 – Oct 2025*
- **Ring-Flex-Attention**: Designed a novel fusion of Ring-style Context Parallelism with PyTorch FlexAttention from the ground up. Validated at 64K sequence length for 32B models with GPU multi-streaming and dynamic masked-block bypassing.
- **OmniMask Support**: Integrated FlexAttention with TP/SP/PP/CP for Emu's complex attention patterns (causal, bidirectional, region-specific), replacing 4-D attention masks with per-row block-masks.
- **Hybrid Parallelism**: Orchestrated TP8/CP4/SP/DP/PP combinations at multi-node scale.
- **Modality-Aware LoRA**: Designed tensor-wise sharded, modality-specific LoRA for parameter-efficient fine-tuning on image tokens.
- Delivered production-grade training for EMU3.5 (1.5B–32B) across 4K–64K sequence lengths.

### NVIDIA TransformerEngine Plugin System &nbsp; *Aug 2025 – Mar 2026*
*Plugin system officially recognized by NVIDIA; mainline integration in progress.*
- Designed a general plugin-based operator management mechanism for TransformerEngine, enabling multi-chip (NVIDIA, Hygon, Metax, Kunlunxin, Iluvatar, Moore), multi-language (CUDA, Triton), and priority-adaptive operator dispatch.
- **Triton Backend**: Reimplemented all core TransformerLayer operators via Triton kernel composition (Generic GEMM, Attention, Adam Optimizer), achieving full Triton coverage for Qwen3 Dense model training.
- **Dynamic Sparse Attention**: Built from scratch in Triton, achieving 10% latency reduction vs. Flash Attention by skipping fully-masked regions.
- Co-optimized Triton GEMM with Sequence Parallel AllGather/AllReduce for long-context throughput gains.

### DualPipeV Pipeline Parallelism &nbsp; *Apr 2025 – Jul 2025*
- 7-stage pipeline orchestration with 2-chunk forward/backward micro-batches and precise dependency tracking.
- Decoupled backward pass into backward-for-inputs and backward-for-weights for finer-grained overlap.
- Profiling-driven MoE kernel reordering for seamless compute-communication disentanglement.
- **Result**: 1.12× throughput vs. Megatron-LM 1F1B baseline on 8×H100 (PP4EP2) with DeepSeek 16B.

### ERNIE Semi-Auto Distributed Training &nbsp; *Aug 2023 – Oct 2024*
- Semi-auto parallelism framework design with hybrid parallel strategy support.
- Full-chain distributed training (DP/TP/PP/SP) and verification for ERNIE LLMs: Pretrain, SFT, LoRA.


# 📝 Publications

[Hybrid-Memcached: A Novel Approach for Memcached Persistence Optimization with Hybrid Memory](https://ieeexplore.ieee.org/abstract/document/10492614)

**IEEE Transactions on Computers (TC), 2024** &nbsp; [CCF-A]

Zhang Jiang\*, **Xianduo Li**\* (joint first author), Xiaoli Gong, et al.

---

[ABM-SpConv-SIMD: Accelerating Convolutional Neural Network Inference for Industrial IoT Applications on Edge Devices](https://ieeexplore.ieee.org/document/9721546)

**IEEE Transactions on Network Science and Engineering (TNSE), 2022** &nbsp; [JCR-Q1]

**Xianduo Li**, Xiaoli Gong, Dong Wang, Jin Zhang, et al.


# 🎖 Honors and Awards
- *2024.03* &nbsp; Member of Ernie-Team, Baidu Proud of 2024
- *2023.10* &nbsp; Best New-comer Award, Baidu PaddlePaddle
- *2023.06* &nbsp; Outstanding Master Thesis Award, Nankai University
- *2022.10* &nbsp; First-class (Top 10%) GongNeng Scholarship, Nankai University
- *2020.06* &nbsp; Outstanding Student, China University of Mining and Technology


# 💬 Services
- Teaching Assistant, Operating System course, Nankai University, Fall 2020.
