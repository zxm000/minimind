\# MiniMind 个人复现记录



\## 1. 项目信息



\- 项目名称：MiniMind

\- 原项目地址：https://github.com/jingyaogong/minimind

\- 个人复现仓库：https://github.com/zxm000/minimind

\- 复现目标：从零理解并复现小型语言模型的预训练、监督微调和推理过程。



\## 2. 实验环境



| 项目 | 配置 |

|---|---|

| 操作系统 | Windows |

| GPU | NVIDIA GeForce RTX 5060 Laptop GPU |

| GPU 显存 | 8GB |

| NVIDIA 驱动 | 573.24 |

| CUDA Runtime | 12.8 |

| Python | 3.10.22 |

| PyTorch | 2.7.1+cu128 |

| torchvision | 0.22.1+cu128 |

| torchaudio | 2.7.1+cu128 |

| BF16 | 支持 |



\## 3. 环境搭建进度



\- \[x] 创建 Conda 环境 minimind

\- \[x] 安装 PyTorch

\- \[x] 验证 CUDA 可用

\- \[x] 验证 RTX 5060 正常识别

\- \[x] 下载 MiniMind 项目

\- \[x] 安装项目依赖

\- \[x] Fork 原项目到个人 GitHub

\- \[x] 配置 origin 和 upstream

\- \[x] 补齐 Git 历史记录



\## 4. 模型复现进度



\- \[ ] 训练数据准备

\- \[ ] MiniMind 预训练（Pretrain）

\- \[ ] 监督微调（SFT）

\- \[ ] 模型推理测试

\- \[ ] 实验结果分析



\## 5. 实验记录



\### 2026-11-06：环境搭建



完成 Python、PyTorch 和 CUDA 环境配置。



通过 torch.cuda.is\_available() 验证 GPU 可以正常调用。



成功下载 MiniMind 项目，并完成项目依赖安装。



\### 后续实验



待补充训练参数、Loss 变化、模型权重及测试结果。



\## 6. 复现总结



目前已完成项目下载、运行环境搭建及 Git 仓库配置，后续将开展数据准备、预训练、监督微调和模型推理实验。



\## 2026-11-09 模型推理测试



\### 实验目的

验证预训练模型能否成功加载并生成文本。



\### 模型配置

\- 模型参数量：63.91M

\- Hidden Size：768

\- Transformer 层数：8

\- 最大生成 Token：64

\- 推理设备：NVIDIA RTX 5060 Laptop GPU



\### 实验结果

成功加载模型权重 pretrain\_test\_768.pth。

成功完成文本生成。

生成速度约为 17.50 tokens/s（首次测试）。



\### 实验结论

模型训练与推理流程正常运行，但由于预训练数据量较少，生成文本质量较差。

