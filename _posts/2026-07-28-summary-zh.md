---
layout: default
title: "Horizon Summary: 2026-07-28 (ZH)"
date: 2026-07-28
lang: zh
---

> 从 28 条内容中筛选出 6 条重要资讯。

---

1. [Kimi K3：全球首个开源 2.8 万亿参数模型](#item-1) ⭐️ 9.0/10
2. [DP-FedSOFIM：无需额外隐私成本的二阶差分隐私联邦优化](#item-2) ⭐️ 9.0/10
3. [中国开始量产国产 DUV 光刻机，今年目标约 5 台](#item-3) ⭐️ 9.0/10
4. [Anthropic 开放权重模型立场引发批评](#item-4) ⭐️ 8.0/10
5. [Fastjson2 曝远程代码执行漏洞，所有版本受影响](#item-5) ⭐️ 8.0/10
6. [中方驳斥美方以 AI 模型蒸馏为由的制裁威胁](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Kimi K3：全球首个开源 2.8 万亿参数模型](https://simonwillison.net/2026/Jul/27/kimi-k3/#atom-everything) ⭐️ 9.0/10

月之暗面（Moonshot AI）在 Hugging Face 上发布了其 2.8 万亿参数的 Kimi K3 模型权重，采用修改版许可证，要求大型商业实体进行署名，大型模型即服务企业需另行签订协议。 此次发布是开源权重 AI 的一个重要里程碑，Kimi K3 是迄今公开的最大模型之一，可与 GPT-5.6 Sol 和 Claude Fable 5 等专有模型相媲美。其修改版许可证反映了 AI 行业在开放性与商业控制之间的持续张力。 Kimi K3 采用 Stable LatentMoE 架构，拥有 896 个专家，每 token 激活 16 个，并引入了 Kimi Delta Attention（KDA）和 Attention Residuals（AttnRes）。它支持文本、图像和视频理解，上下文窗口达 100 万 token，并支持 MXFP4 量化。

rss · Simon Willison · 7月27日 23:39

**背景**: 大型语言模型如 GPT-4 和 Claude 传统上都是专有的，仅通过 API 提供有限访问。开源权重模型公开释放训练好的参数，允许研究人员和开发者在本地或自有基础设施上运行模型。月之暗面此前发布了采用类似修改版许可证的 Kimi K2 模型，K3 则大幅扩展至 2.8 万亿参数。

**标签**: `#AI`, `#large language models`, `#open-source`, `#Moonshot`, `#Kimi K3`

---

<a id="item-2"></a>
## [DP-FedSOFIM：无需额外隐私成本的二阶差分隐私联邦优化](https://www.reddit.com/r/MachineLearning/comments/1v8pkb7/dpfedsofim_secondorder_federated_optimization/) ⭐️ 9.0/10

DP-FedSOFIM 提出了一种在差分隐私下的二阶联邦优化方法，将曲率估计移至服务器端，仅利用已经私有化的聚合梯度构建秩一 Fisher 代理，从而避免了先前二阶方法所需的额外隐私成本和 O\(d²\) 客户端通信。该方法在 CIFAR-10/ResNet 上、eps=5 时，早期轮次相比 DP-FedGD 提升高达 +20.3 个点，并且达到 DP-FedGD 最终准确率 95% 所需的轮次减少约 4-5 倍。 这项工作解决了差分隐私联邦学习中的一个关键限制：无法在不增加额外隐私成本或通信开销的情况下有效利用二阶信息。通过将曲率适应视为服务器端的后处理问题，DP-FedSOFIM 使得在严格隐私预算下实现二阶收益成为可能，有望加速通信受限的联邦场景中的收敛。 该方法使用私有化聚合梯度的指数移动平均（EMA），并将其正则化的秩一外积视为 Fisher 代理，应用 Sherman-Morrison 公式以闭式形式计算预处理步骤，而无需构建完整矩阵。预处理开销每轮相比 DP-FedGD 不到 2% 的挂钟时间，而客户端内存保持 O\(d\) 而非 O\(d²\)。

reddit · r/MachineLearning · /u/worthybog0 · 7月28日 06:04

**背景**: 差分隐私联邦学习（DP-FL）通常使用一阶优化方法，如 DP-FedAvg 或 DP-FedGD，这些方法对每个样本的梯度进行裁剪、添加高斯噪声并聚合。二阶方法可以通过利用曲率信息改善收敛，但先前的方法要求客户端传输完整的协方差矩阵（O\(d²\) 通信），并引入新的敏感度项，增加了隐私成本。DP-FedSOFIM 通过完全在服务器端使用已经私有化的聚合来估计曲率，利用差分隐私的后处理免疫性，从而规避了这一问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2601.09166v2">DP - FedSOFIM : Differentially Private Federated Stochastic Optimization...</a></li>
<li><a href="https://www.emergentmind.com/topics/dp-fedsofim">DP - FedSOFIM : Efficient DP Federated Learning</a></li>

</ul>
</details>

**标签**: `#differential privacy`, `#federated learning`, `#second-order optimization`, `#privacy-preserving machine learning`, `#optimization`

---

<a id="item-3"></a>
## [中国开始量产国产 DUV 光刻机，今年目标约 5 台](https://www.theinformation.com/articles/china-starts-mass-producing-homegrown-duv-chipmaking-tools-advance-local-chip-industry) ⭐️ 9.0/10

中国已开始大规模生产自主研发的浸没式 DUV 光刻机，计划今年生产约 5 台，2027 年达到约 20 台。这些设备将交付给中芯国际、华虹半导体等国内厂商，但在性能和可靠性上仍落后于 ASML。 这一里程碑标志着中国在半导体自给自足方面迈出了重要一步，可能减少对 ASML 等外国供应商的依赖。该消息导致 ASML 股价显著下跌，反映出市场对长期竞争压力和潜在出口管制影响的担忧。 国产浸没式 DUV 光刻机使用 193nm 波长，但分辨率和套刻精度低于 ASML 的先进机型。关键部件仍来自日本，本地供应链延误已影响进度；芯片商需要数月测试才能将其投入量产。

telegram · zaihuapd · 7月27日 14:10

**背景**: DUV 光刻机使用深紫外光（193nm 波长）在硅片上刻印电路图案。浸没式光刻通过在镜头和晶圆之间填充液体来提高分辨率。ASML 是全球光刻机领导者，特别是在用于尖端芯片的 EUV 领域。由于美国主导的出口管制，中国一直在加速半导体设备的自主研发，因此这次量产尽管存在性能差距，仍是一个关键里程碑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/23271784579">国产DUV光刻机分析 - 知乎</a></li>
<li><a href="https://www.maskalignercn.com/a/20240508385.html">duv光刻机 euv光刻机 - 科汇华晟</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#lithography`, `#China`, `#ASML`, `#chip manufacturing`

---

<a id="item-4"></a>
## [Anthropic 开放权重模型立场引发批评](https://www.anthropic.com/news/position-open-weights-models) ⭐️ 8.0/10

Anthropic 发布了一份政策声明，阐述了其对开放权重 AI 模型的立场。该公司主张对所有足够强大的模型进行强制性安全测试，但并未呼吁禁止开放权重模型。 这一声明意义重大，因为它涉及 AI 领域的一个关键辩论：开放性与安全性之间的平衡。Anthropic 的立场可能影响监管讨论和开放权重模型分发的未来。 Anthropic 支持诸如禁止向中国销售芯片和打击走私等措施，但不主张禁止开放权重模型。该公司呼吁对所有足够强大的模型（包括开放和封闭模型）进行强制性安全测试。

hackernews · surprisetalk · 7月27日 22:03 · [社区讨论](https://news.ycombinator.com/item?id=49076057)

**背景**: 开放权重 AI 模型是指其训练参数（权重）公开发布的模型，允许开发者下载、微调并将其集成到应用程序中。与完全开源模型不同，开放权重模型可能不包括训练代码或数据。这种方法实现了更广泛的访问和定制，但也引发了关于滥用的担忧，因为模型可以不受限制地使用。Anthropic 是一家领先的 AI 安全公司，开发开放和封闭模型，现已阐明其政策立场。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/@aruna.kolluru/exploring-the-world-of-open-source-and-open-weights-ai-aa09707b69fc">Exploring the World of Open Source and Open Weights AI | Medium</a></li>
<li><a href="https://www.linkedin.com/posts/mit-csail_what-are-open-weights-ai-models-why-are-activity-7358606381521747969-k_Hd">What are open - weights AI models and why do they matter? | LinkedIn</a></li>

</ul>
</details>

**社区讨论**: 社区评论对 Anthropic 的立场持高度批评态度。用户指出其矛盾之处，例如主张芯片出口禁令却声称不支持禁令，并指责该公司出于企业自身利益。一些评论者质疑 Anthropic 安全担忧的诚意，考虑到其此前在其他问题上缺乏行动。

**标签**: `#open-weights`, `#Anthropic`, `#AI policy`, `#AI safety`, `#debate`

---

<a id="item-5"></a>
## [Fastjson2 曝远程代码执行漏洞，所有版本受影响](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 8.0/10

长亭科技于 7 月 27 日披露了 Fastjson2 的一个远程代码执行漏洞，攻击者可通过恶意 JSON 数据绕过 AutoType 类型校验并执行任意代码。该漏洞影响 2.0.62 及之前的所有版本，目前官方尚未发布补丁。 这是一个严重的安全问题，因为 Fastjson2 被广泛用于 Java 应用的 JSON 处理，该漏洞允许未经认证的远程代码执行。由于尚无补丁，用户必须禁用 AutoType 或采取其他缓解措施，这可能会影响依赖自动类型反序列化的系统功能。 项目维护者已确认该安全问题，但相关的 PR \#7695 已被关闭且未合入主分支。完整的漏洞细节和利用代码尚未公开，目前建议彻底禁用 AutoType 作为缓解措施。

telegram · zaihuapd · 7月27日 10:31

**背景**: Fastjson2 是阿里巴巴开发的高性能 Java JSON 库，以其快速的序列化和反序列化能力著称。AutoType 功能允许库在反序列化时根据 JSON 数据中的&\#x27;@type&\#x27;字段自动确定对象类型。然而，该功能历史上一直是反序列化攻击的载体，攻击者可以构造恶意 JSON 触发任意类的实例化，从而导致远程代码执行。此漏洞类似于之前 Fastjson1 中出现的 AutoType 相关 RCE 漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/alibaba/fastjson2">GitHub - alibaba/fastjson2: 🚄 FASTJSON2 is a Java JSON library with excellent performance.</a></li>
<li><a href="https://alibaba.github.io/fastjson2/autotype_cn.html">FASTJSON 2 Autotype机制介绍 | fastjson2</a></li>
<li><a href="https://www.alphabot.com/security/blog/2020/java/Fastjson-exceptional-deserialization-vulnerabilities.html">Fastjson: exceptional deserialization vulnerabilities - Alphabot Security</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#fastjson2`, `#rce`, `#java`

---

<a id="item-6"></a>
## [中方驳斥美方以 AI 模型蒸馏为由的制裁威胁](https://www.mofcom.gov.cn/syxwfb/art/2026/art_7f1622463a7c48ef9fad600ce0ef702f.html) ⭐️ 8.0/10

7 月 27 日，中国商务部正式驳斥了美方关于中国 AI 企业通过模型蒸馏窃取知识产权的指控，并警告称，若美方实施制裁，中方将采取必要措施维护中国企业合法权益。 这一交锋凸显了人工智能领域地缘政治紧张局势的升级，可能扰乱全球 AI 合作与开源模型的获取，因为中美企业都依赖对方的模型。 商务部指出，模型蒸馏是行业广泛使用的技术，近 200 家美国初创企业已呼吁政府不要限制访问中国开源模型，这凸显了 AI 发展中的相互依赖关系。

telegram · zaihuapd · 7月27日 11:01

**背景**: 模型蒸馏是一种机器学习技术，其中较小的“学生”模型从较大的“教师”模型中学习，通常用于压缩模型以提高效率。这是 AI 研究和开发中的常见做法，本身并不涉及知识产权盗窃。中美科技竞争日益激烈，双方互相指责对方采取不公平做法，而许多企业受益于跨境模型访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation - Wikipedia</a></li>
<li><a href="https://blog.csdn.net/pythonhy/article/details/149597959">blog.csdn.net/pythonhy/article/details/149597959</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#model distillation`, `#US-China relations`, `#intellectual property`, `#open-source AI`

---