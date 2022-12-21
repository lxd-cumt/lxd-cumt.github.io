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

I’m currently a master student at Nankai University. I obtained my bachelor’s degree from School of Computer Science and Technology, China University of Mining and Technology (CUMT), June, 2020. 
My research interests include computer architecture, software/hardware co-optimization for machine learning.

<!--
My research interest includes neural machine translation and computer vision. I have published more than 100 papers at the top international AI conferences with total <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'>google scholar citations <strong><span id='total_cit'>260000+</span></strong></a> (You can also use google scholar badge <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&logo=Google%20Scholar&labelColor=f6f6f6&color=9cf&style=flat&label=citations"></a>).
 -->

# 🔥 News
- *2022.12*: &nbsp;🎉🎉 I will join Baidu PaddlePaddle as a HPC engineer!
- *2022.10*: &nbsp;🎉🎉 Won the first-class (Top 10%) scholarship of Nankai University 🎉🎉
- *2022.04*: &nbsp;🎉🎉 Join Shuhai Lab Huawei Cloud as Research Intern for three months 🎉🎉
- *2022.02*: &nbsp;🎉🎉 Out work **ABM-SpConv-SIMD** was accepted by **IEEE Transactions on Network Science and Engineering** 🎉🎉
<!-- - * -->
<!-- - *2022.02*: &nbsp;🎉🎉 Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet.  -->

# 📖 Educations
- *2020.09 - 2022.11 (now)*: M.S. in Computer Technology, School of Computer Science and Cyber Science, Nankai University. Advisor: Prof.[Xiaoli Gong](https://cc.nankai.edu.cn/2019/0619/c13620a179396/page.htm). 
- *2016.09 - 2020.06*: B.E. in Electronic Information Science and Engineering, School of Computer Science and Technology, China University of Mining and Technology.

# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ABM-SpConv-SIMD</div><img src='images/paper1.jpeg' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[《ABM-SpConv-SIMD: Accelerating Convolutional Neural Network Inference for Industrial IoT Applications on Edge Devices》](https://ieeexplore.ieee.org/document/9721546)

IEEE Transactions on Network Science and Engineering, 2022

✍🏻 **Xianduo Li**, Xiaoli Gong, Dong Wang, Jin Zhang, et al.

🎉 **Contribution** 
- Propose a framework that employs offline pruning and quantization and online SIMD optimization to fit DNN for cost-effective edge devices.
- Design and implement accumulation-before-multiplication sparse convolutional algorithm.
- Conduct a series of experiments to evaluate the performance of our framework on various edge devices.

</div>
</div>

# 👨‍💻 Work Experience
- **Shuhai Lab at Huawei Cloud, Research Intern.** 
Research Topic: Design a benchmark suite for latency-critical cloud applications (such as Memcached, Redis, et al) with a wide variety of latency requirements and micro-architectural characteristics.

# 💻 Research Experience
### Software/Hardware Co-optimization for Machine Learning
- **ABM-SpConv-SIMD**, an on-device optimization framework for low-cost and common ARM CPUs to reduce CNN inference latency by exploiting NEON instructions for parallelism. (Labels: ARM CPU, SIMD, DNN Inference Latency)
- **CILPO**, a framework for ARM Mobile SoCs to improve CNN inference throughput by exploiting heterogeneous CPU-GPU scheduling and pipeline technology. (Labels: ARM CPU and Mobile GPU, Heterogeneous Scheduling, DNN INference Throughput)
- **NLP-DSP**, design an efficient training framework to implement NLP models (such as Bert, GPT2, et al.) on a custom multi-core DSP processor (GPU-like). (Labels: DSP Accelerators, Custom DSP Scalar and Vector Instructions, GPU-like Kernel Design, NLP Training)

### Linux Kernel
- Source code analysis of Transparent Huge Page (THP) mechanism and linux memory management.
- Ucore OS, a micro-os for teaching.


<!-- 
### Areas of interest but not researched in depth

- Hashing-based DNN Training; Deep Learning Compiler; (Machine Learning)
- QoS-aware Scheduling in Cloud; Interference-aware Scheduling in Cloud; (Cloud Computing)
- Zero-Knowledge Proofs; (Security)
- P4 Language, In-network Computing, Distributed Training, Profiler, Network Telemetry(Network)
 -->


# 🎖 Honors and Awards
- *2022-2023* The first-class GongNeng Scholarship of Nankai University
- *2020-2021* New Student Scholarship of Nankai University
- *2020.06* Outstanding Student of China University of Mining and Technology
- *2017-2018,2018-2019* Two times first-class scholarships of China University of Mining and Technology





# 💬 Services
- Teaching assistant, Operating System (OS) course in the fall semester of 2020 at Nankai University. 


