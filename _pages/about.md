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

I’m currently a hpc engineer at PaddlePaddle, Baidu, Beijing. 
I obtained my master’s degree from School of Computer Science, Nankai University, in 2023.
My research interests include computer architecture, software/hardware co-optimization for machine learning.

<!--
My research interest includes neural machine translation and computer vision. I have published more than 100 papers at the top international AI conferences with total <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'>google scholar citations <strong><span id='total_cit'>260000+</span></strong></a> (You can also use google scholar badge <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&logo=Google%20Scholar&labelColor=f6f6f6&color=9cf&style=flat&label=citations"></a>).
 -->

# 🔥 News
- *2024.04*: &nbsp;🎉🎉 Our work **Hybrid-Memcached** was accepted by **IEEE Transactions on Computers** 🎉🎉 
- *2023.07*: &nbsp;🎉🎉 I will join Baidu PaddlePaddle as a HPC engineer!
- *2022.10*: &nbsp;🎉🎉 Won the first-class (Top 10%) scholarship of Nankai University 🎉🎉
- *2022.04*: &nbsp;🎉🎉 Join Shuhai Lab Huawei Cloud as Research Intern for three months 🎉🎉
- *2022.02*: &nbsp;🎉🎉 Out work **ABM-SpConv-SIMD** was accepted by **IEEE Transactions on Network Science and Engineering** 🎉🎉
<!-- - * -->
<!-- - *2022.02*: &nbsp;🎉🎉 Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet.  -->

# 📖 Educations
- *2020.09 - 2023.06*: M.S. in Computer Technology, School of Computer Science and Cyber Science, Nankai University. Advisor: Prof.[Xiaoli Gong](https://cc.nankai.edu.cn/2019/0619/c13620a179396/page.htm). 
- *2016.09 - 2020.06*: B.E. in Electronic Information Science and Engineering, School of Computer Science and Technology, China University of Mining and Technology.

# 👨‍💻 Work Experience
- **HPC Engineer / Machine Learning Framework Engineer, Baidu PaddlePaddle, Beijing.**
- Semi-auto parallelism distributed training of Ernie LLMs, including Pretrain, SFT, LoRA, PTQ and so on
- AutoML. From hand-written parallel distributed training (such as megatron-lm.tensor_paralle.column_parallel/row_parallel), to semi-auto parallel training (such as  parallelize_module in pytorch, shard_op/shard_tensor in paddle), to full-auto parallel training
- Prim mechanism. Decompose op into primitive ops, to support back-end compiler and high-order differentiation

- **Shuhai Lab at Huawei Cloud, Research Intern.** 
- Cloud workload characterization from micro-architectural perspective
- Benchmark suite design for latency-critical cloud applications (such as Memcached, Redis, et al) with a wide variety of latency requirements

# 📝 Publications 
<!-- 
<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Hybrid-Memcached</div><img src='images/paper3.jpeg' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1"> -->

[《Hybrid-Memcached: A Novel Approach for Memcached Persistence Optimization with Hybrid Memory》](https://ieeexplore.ieee.org/abstract/document/10492614)

**IEEE Transactions on Computers, 2024**

✍🏻 **Zhang Jiang**, **Xianduo Li** **(joint first author)**, Xiaoli Gong, et al.
- DRAM-based data aggregation to avoid fine-grained writes
- data-object alignment mechanism to avoid write amplification
- non-temporal store instruction based writing to improve the bandwidth utilization


<!-- <div class='paper-box'><div class='paper-box-image'><div><div class="badge">ABM-SpConv-SIMD</div><img src='images/paper1.jpeg' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1"> -->

[《ABM-SpConv-SIMD: Accelerating Convolutional Neural Network Inference for Industrial IoT Applications on Edge Devices》](https://ieeexplore.ieee.org/document/9721546)

**IEEE Transactions on Network Science and Engineering, 2022**

✍🏻 **Xianduo Li**, Xiaoli Gong, Dong Wang, Jin Zhang, et al.
- Propose a framework that employs offline pruning and quantization and online SIMD optimization to fit DNN for cost-effective edge devices.
- Design and implement accumulation-before-multiplication sparse convolutional algorithm.
- Conduct a series of experiments to evaluate the performance of our framework on various edge devices.

<!-- </div>
</div> -->


# 💻 Research Experience
### Systems
- **Hybrid-Memcached**, a novel approach for Memcached persistence optimization with hybrid memory. (Labels: Hybrid Memory, DRAM-based Data Aggregation)
- **Linux THP**, Source code analysis of Transparent Huge Page (THP) mechanism and linux memory management.
- **Ucore OS**, a micro-os for teaching.

### Software/Hardware Co-optimization for Machine Learning
- **ABM-SpConv-SIMD**, an on-device optimization framework for low-cost and common ARM CPUs to reduce CNN inference latency by exploiting NEON instructions for parallelism. (Labels: ARM CPU, SIMD, DNN Inference Latency)
- **CILPO**, a framework for ARM Mobile SoCs to improve CNN inference throughput by exploiting heterogeneous CPU-GPU scheduling and pipeline technology. (Labels: ARM CPU and Mobile GPU, Heterogeneous Scheduling, DNN INference Throughput)
- **NLP-DSP**, design an efficient training framework to implement NLP models (such as Bert, GPT2, et al.) on a custom multi-core DSP processor (GPU-like). (Labels: DSP Accelerators, Custom DSP Scalar and Vector Instructions, GPU-like Kernel Design, NLP Training)


### Areas of interest
- Deep Learning Compiler: TVM, OpenAI Triton, ...
- Hashing-based DNN Training
- QoS-aware Scheduling in Cloud; Interference-aware Scheduling in Cloud; (Cloud Computing)
- Zero-Knowledge Proofs; (Security)
- P4 Language; In-network Computing; Distributed Training; Profiler; Network Telemetry; (Network)


# 🎖 Honors and Awards
- *2024.03* Member of Ernie-Team, Baidu Proud of 2024
- *2023.10* Best New-comer Award of Baidu PaddlePaddle
- *2023.06* Outstanding Master Thesis Award, Nankai University
- *2022-2023* The first-class GongNeng Scholarship of Nankai University
- *2020-2021* New Student Scholarship of Nankai University
- *2020.06* Outstanding Student of China University of Mining and Technology
- *2017-2018,2018-2019* Two times first-class scholarships of China University of Mining and Technology





# 💬 Services
- Teaching assistant, Operating System (OS) course in the fall semester of 2020 at Nankai University. 


