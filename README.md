# Intelligent-Page-Prefetch-LLM
通过动态分析大语言模型的访存特征，实现操作系统层的内存预取优化。
## 项目名称
基于大模型访存特征的智能页面预取器设计
## 项目描述

随着大模型训练和推理的普及，内存访问的缺页率成为制约性能的关键因素。传统操作系统的页面管理策略无法有效捕捉大模型特有的长距离依赖、稀疏注意力机制等动态访问模式，导致缺页中断频繁发生，严重影响训练/推理效率。

本项目要求参赛者设计并实现一套基于访存行为分析的智能预取系统。要求通过操作系统层的内存管理机制改进，动态预测模型推理过程中的参数访问序列，提前将所需参数加载至物理内存，降低缺页中断次数，同时保证预取过程对推理延迟的影响可控。
## 项目特征

1. ​**实时监测**大模型推理过程中的缺页异常分布特征  
2. 结合**时间局部性**与**空间局部性**设计分级预取算法  
3. 适配`llama.cpp`等主流推理框架的内存映射机制，实现透明化部署
## 预期目标
预期目标包括但不限于以下方面：
### 1. 核心优化能力
- 显著降低大模型训练/推理过程中的缺页率，提升内存访问效率  
- 实现推理吞吐量有效提升，优化交互场景下的响应延迟  
- 支持多线程推理任务的协同预取，避免资源冲突  

### 2. 系统兼容性
- 兼容主流大模型框架，支持轻量级集成且不侵入原有计算流程  
- 适配开源大模型生态，可基于原生模型代码进行端到端验证  

### 3. 可观测性与可复现性
- 提供可视化监控界面，实时展示缺页热力图、预取命中轨迹与内存压力状态  
- 实现与AI工具链的无缝适配，确保优化效果可量化验证  
- 提供自动化测试方案与可复现的基准对比案例  
选择本项目的同学也可提出自己的新想法，得到导师认可支持后亦可加入预期目标或
进阶特性。
## 参考资料

1. ​**开源项目与工具链**  
   - [ZeRO](https://arxiv.org/abs/2104.04473)  
   - [vLLM](https://github.com/vllm-project/vllm)  
   - [Perf](https://perf.wiki.kernel.org/)
2. ​**框架与生态**  
   - [Hugging Face Transformers](https://github.com/huggingface/transformers)  
   - [llama.cpp](https://github.com/ggerganov/llama.cpp)  
   - [TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM)

## 所属赛道
2025全国大学生操作系统比赛的“OS功能设计”赛道
## 难度
中等
## 项目导师
- 姓名：宫晓利
- 单位：南开大学
- email:gongxiaoli@nankai.edu.cn


