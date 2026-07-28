---
layout: default
title: "Horizon Summary: 2026-07-28 (EN)"
date: 2026-07-28
lang: en
---

> From 28 items, 6 important content pieces were selected

---

1. [Moonshot AI Releases 2.8 Trillion Parameter Kimi K3 Weights](#item-1) ⭐️ 9.0/10
2. [DP-FedSOFIM: Second-Order DP Federated Optimization Without Extra Cost](#item-2) ⭐️ 9.0/10
3. [China Begins Mass Production of Domestic DUV Lithography Tools](#item-3) ⭐️ 9.0/10
4. [Anthropic Stance on Open-Weights Models Draws Criticism](#item-4) ⭐️ 8.0/10
5. [Critical RCE Vulnerability in Fastjson2 Affects All Versions](#item-5) ⭐️ 8.0/10
6. [China Rejects US Sanctions Threats Over AI Model Distillation](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Moonshot AI Releases 2.8 Trillion Parameter Kimi K3 Weights](https://simonwillison.net/2026/Jul/27/kimi-k3/#atom-everything) ⭐️ 9.0/10

Moonshot AI has released the weights for their 2.8 trillion parameter Kimi K3 model on Hugging Face, under a modified license that requires attribution for large commercial entities and a separate agreement for large Model-as-a-Service businesses. This release marks a major milestone in open-weight AI, as Kimi K3 is one of the largest models ever made publicly available, rivaling proprietary models like GPT-5.6 Sol and Claude Fable 5. Its modified license reflects ongoing tensions between openness and commercial control in the AI industry. Kimi K3 uses a Stable LatentMoE architecture with 896 experts, activating 16 per token, and features Kimi Delta Attention \(KDA\) and Attention Residuals \(AttnRes\). It supports text, image, and video understanding with a 1 million token context window and MXFP4 quantization.

rss · Simon Willison · Jul 27, 23:39

**Background**: Large language models like GPT-4 and Claude have traditionally been proprietary, with only limited access via APIs. Open-weight models, where the trained parameters are publicly released, allow researchers and developers to run the models locally or on their own infrastructure. Moonshot AI previously released the Kimi K2 model with a similar modified license, and K3 represents a significant scale-up to 2.8 trillion parameters.

**Tags**: `#AI`, `#large language models`, `#open-source`, `#Moonshot`, `#Kimi K3`

---

<a id="item-2"></a>
## [DP-FedSOFIM: Second-Order DP Federated Optimization Without Extra Cost](https://www.reddit.com/r/MachineLearning/comments/1v8pkb7/dpfedsofim_secondorder_federated_optimization/) ⭐️ 9.0/10

DP-FedSOFIM introduces a second-order federated optimization method under differential privacy that moves curvature estimation to the server, using only the already-privatized aggregate gradients to build a rank-one Fisher proxy, thus avoiding the extra privacy cost and O\(d²\) client communication typical of prior second-order approaches. The method achieves up to +20.3 points improvement over DP-FedGD at early rounds on CIFAR-10/ResNet with eps=5, and requires 4-5x fewer rounds to reach 95% of DP-FedGD&\#x27;s final accuracy. This work addresses a critical limitation in differentially private federated learning: the inability to efficiently use second-order information without incurring additional privacy cost or communication overhead. By treating curvature adaptation as a server-side post-processing problem, DP-FedSOFIM makes second-order benefits practical under tight privacy budgets, potentially accelerating convergence in communication-constrained federated settings. The method uses an exponential moving average \(EMA\) of the privatized aggregate gradient and treats its regularized rank-one outer product as a Fisher proxy, applying the Sherman-Morrison formula to compute the preconditioned step in closed form without ever forming the full matrix. The preconditioning overhead is under 2% wall-clock time per round compared to DP-FedGD, while client memory remains O\(d\) instead of O\(d²\).

reddit · r/MachineLearning · /u/worthybog0 · Jul 28, 06:04

**Background**: Differentially private federated learning \(DP-FL\) typically uses first-order optimization methods like DP-FedAvg or DP-FedGD, which clip per-example gradients, add Gaussian noise, and aggregate. Second-order methods can improve convergence by using curvature information, but prior approaches required clients to transmit full covariance matrices \(O\(d²\) communication\) and introduced new sensitivity terms, increasing the privacy cost. DP-FedSOFIM circumvents this by estimating curvature entirely on the server using the already-privatized aggregate, leveraging the post-processing immunity of differential privacy.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2601.09166v2">DP - FedSOFIM : Differentially Private Federated Stochastic Optimization...</a></li>
<li><a href="https://www.emergentmind.com/topics/dp-fedsofim">DP - FedSOFIM : Efficient DP Federated Learning</a></li>

</ul>
</details>

**Tags**: `#differential privacy`, `#federated learning`, `#second-order optimization`, `#privacy-preserving machine learning`, `#optimization`

---

<a id="item-3"></a>
## [China Begins Mass Production of Domestic DUV Lithography Tools](https://www.theinformation.com/articles/china-starts-mass-producing-homegrown-duv-chipmaking-tools-advance-local-chip-industry) ⭐️ 9.0/10

China has started mass production of domestically developed immersion DUV lithography machines, with a plan to produce about 5 units this year and 20 by 2027. The tools will be delivered to Chinese chipmakers like SMIC and Hua Hong Semiconductor, though they still lag behind ASML in performance and reliability. This milestone marks a significant step in China&\#x27;s semiconductor self-sufficiency, potentially reducing dependence on foreign suppliers like ASML. The news triggered a notable drop in ASML&\#x27;s stock, reflecting market concerns about long-term competitive pressure and the impact of potential export controls. The domestic immersion DUV lithography machine uses 193nm wavelength but has lower resolution and overlay accuracy compared to ASML&\#x27;s advanced models. Key components still come from Japan, and local supply chain delays have impacted progress; chipmakers require months of testing before the tools can be used in mass production.

telegram · zaihuapd · Jul 27, 14:10

**Background**: DUV lithography uses deep ultraviolet light \(193nm wavelength\) to create circuit patterns on silicon wafers. Immersion lithography improves resolution by filling the space between the lens and wafer with a liquid. ASML is the global leader in lithography, especially for EUV machines used in cutting-edge chips. China has been accelerating domestic development of semiconductor equipment due to US-led export controls, making this mass production a key milestone despite performance gaps.

<details><summary>References</summary>
<ul>
<li><a href="https://zhuanlan.zhihu.com/p/23271784579">国产DUV光刻机分析 - 知乎</a></li>
<li><a href="https://www.maskalignercn.com/a/20240508385.html">duv光刻机 euv光刻机 - 科汇华晟</a></li>

</ul>
</details>

**Tags**: `#semiconductor`, `#lithography`, `#China`, `#ASML`, `#chip manufacturing`

---

<a id="item-4"></a>
## [Anthropic Stance on Open-Weights Models Draws Criticism](https://www.anthropic.com/news/position-open-weights-models) ⭐️ 8.0/10

Anthropic published a policy statement outlining its stance on open-weights AI models. The company advocates for mandatory safety testing for all capable models but stops short of calling for a ban on open-weights models. This statement is significant because it addresses a key debate in AI: the balance between openness and safety. Anthropic&\#x27;s position could influence regulatory discussions and the future of open-weights model distribution. Anthropic supports measures such as banning chip sales to China and cracking down on smuggling, but does not advocate for a ban on open-weights models. The company calls for mandatory safety testing for all sufficiently capable models, both open and closed.

hackernews · surprisetalk · Jul 27, 22:03 · [Discussion](https://news.ycombinator.com/item?id=49076057)

**Background**: Open-weights AI models are models whose trained parameters \(weights\) are publicly released, allowing developers to download, fine-tune, and integrate them into applications. Unlike fully open-source models, open-weights models may not include the training code or data. This approach enables broader access and customization but raises concerns about misuse, as the models can be used without restrictions. Anthropic, a leading AI safety company, develops both open and closed models and has now clarified its policy stance.

<details><summary>References</summary>
<ul>
<li><a href="https://medium.com/@aruna.kolluru/exploring-the-world-of-open-source-and-open-weights-ai-aa09707b69fc">Exploring the World of Open Source and Open Weights AI | Medium</a></li>
<li><a href="https://www.linkedin.com/posts/mit-csail_what-are-open-weights-ai-models-why-are-activity-7358606381521747969-k_Hd">What are open - weights AI models and why do they matter? | LinkedIn</a></li>

</ul>
</details>

**Discussion**: The community comments are highly critical of Anthropic&\#x27;s position. Users point out contradictions, such as advocating for chip export bans while claiming not to support bans, and accuse the company of corporate self-interest. Some commenters question the sincerity of Anthropic&\#x27;s safety concerns, given its previous lack of action on other issues.

**Tags**: `#open-weights`, `#Anthropic`, `#AI policy`, `#AI safety`, `#debate`

---

<a id="item-5"></a>
## [Critical RCE Vulnerability in Fastjson2 Affects All Versions](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 8.0/10

On July 27, Chaitin Technology disclosed a remote code execution vulnerability in Fastjson2 that allows attackers to bypass AutoType validation and execute arbitrary code via malicious JSON data. The vulnerability affects all versions up to 2.0.62, and no official patch has been released yet. This is a critical security issue because Fastjson2 is widely used in Java applications for JSON processing, and the vulnerability allows remote code execution without authentication. With no patch available, users must disable AutoType or implement other mitigations, which could break functionality in systems that rely on automatic type deserialization. The maintainers have confirmed the issue but closed the related pull request \#7695 without merging it into the main branch. Full vulnerability details and exploit code have not been publicly released, and the recommended mitigation is to completely disable AutoType until a fix is available.

telegram · zaihuapd · Jul 27, 10:31

**Background**: Fastjson2 is a high-performance JSON library for Java developed by Alibaba, known for its fast serialization and deserialization. The AutoType feature allows the library to automatically determine the type of objects during deserialization based on a &\#x27;@type&\#x27; field in the JSON data. However, this feature has historically been a vector for deserialization attacks, as attackers can craft malicious JSON that triggers the instantiation of arbitrary classes, leading to remote code execution. This vulnerability is similar to previous issues in Fastjson1, which also suffered from AutoType-related RCE vulnerabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/alibaba/fastjson2">GitHub - alibaba/fastjson2: 🚄 FASTJSON2 is a Java JSON library with excellent performance.</a></li>
<li><a href="https://alibaba.github.io/fastjson2/autotype_cn.html">FASTJSON 2 Autotype机制介绍 | fastjson2</a></li>
<li><a href="https://www.alphabot.com/security/blog/2020/java/Fastjson-exceptional-deserialization-vulnerabilities.html">Fastjson: exceptional deserialization vulnerabilities - Alphabot Security</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#fastjson2`, `#rce`, `#java`

---

<a id="item-6"></a>
## [China Rejects US Sanctions Threats Over AI Model Distillation](https://www.mofcom.gov.cn/syxwfb/art/2026/art_7f1622463a7c48ef9fad600ce0ef702f.html) ⭐️ 8.0/10

On July 27, China&\#x27;s Ministry of Commerce officially rejected US allegations that Chinese AI companies are stealing intellectual property through model distillation, and warned that China will take necessary measures to protect its firms if US sanctions are imposed. This exchange highlights escalating geopolitical tensions in AI, potentially disrupting global AI collaboration and access to open-source models, as both US and Chinese companies rely on each other&\#x27;s models. The ministry noted that model distillation is a widely used industry technique, and that nearly 200 US startups have called for unrestricted access to Chinese open-source models, underscoring the mutual dependence in AI development.

telegram · zaihuapd · Jul 27, 11:01

**Background**: Model distillation is a machine learning technique where a smaller &\#x27;student&\#x27; model learns from a larger &\#x27;teacher&\#x27; model, often used to compress models for efficiency. It is a common practice in AI research and development, not inherently tied to intellectual property theft. The US-China tech rivalry has intensified, with both sides accusing each other of unfair practices, while many companies benefit from cross-border model access.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation - Wikipedia</a></li>
<li><a href="https://blog.csdn.net/pythonhy/article/details/149597959">blog.csdn.net/pythonhy/article/details/149597959</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#model distillation`, `#US-China relations`, `#intellectual property`, `#open-source AI`

---