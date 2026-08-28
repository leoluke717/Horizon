---
layout: default
title: "Horizon Summary: 2026-08-28 (ZH)"
date: 2026-08-28
lang: zh
---

> 从 189 条内容中筛选出 11 条重要资讯。

---

1. [Cloudflare 通过优化 1.1.1.1 DNS 缓存节省 100 TB 内存](#item-1) ⭐️ 8.0/10
2. [会计所职业责任保险实施办法公布](#item-2) ⭐️ 8.0/10
3. [广西“新官不理旧账”专项治理累计清偿欠款 7.42 亿元](#item-3) ⭐️ 8.0/10
4. [加拿大对近 200 亿美元美国商品征收 50%报复性关税](#item-4) ⭐️ 8.0/10
5. [Meta 支付 167 亿美元和解，限制青少年社媒使用](#item-5) ⭐️ 8.0/10
6. [亚马逊将于 9 月 30 日关闭 Mechanical Turk 众包平台](#item-6) ⭐️ 8.0/10
7. [Apple Maps 在搜索结果中引入付费广告](#item-7) ⭐️ 8.0/10
8. [Anthropic 与 Nscale 签署 450 亿美元算力合同](#item-8) ⭐️ 8.0/10
9. [英伟达季度营收 962 亿美元，首次给出一年后 70%增长指引](#item-9) ⭐️ 8.0/10
10. [谷歌推广 goto 跳转，搜索结果改用服务器重定向](#item-10) ⭐️ 8.0/10
11. [美国法官叫停五角大楼对 Anthropic 的供应链风险标签](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Cloudflare 通过优化 1.1.1.1 DNS 缓存节省 100 TB 内存](https://blog.cloudflare.com/dns-cache-memory-optimization-1111/) ⭐️ 8.0/10

Cloudflare 对其 1.1.1.1 解析器的 DNS 缓存（代号 Big Pineapple）实施了五项 Rust 层面的内存优化。这些改动将每个条目的内存占用降低了 56%，在整个全球网络中释放了约 100 TB 的内存。 这件事很重要，因为在 Cloudflare 的规模下，DNS 缓存中每个条目节省的内存会累积成巨大的基础设施收益。减少 100 TB 内存可以降低运营成本、提升缓存容量，并可能为依赖 1.1.1.1 的用户降低延迟。 该优化针对特定工作负载，尚未经过独立验证；Cloudflare 也没有量化内存节省之外的财务或性能影响。这项工作主要关注 Rust 中的内存布局与分配策略。

hackernews · TangerineDream · 8月27日 17:17 · [社区讨论](https://news.ycombinator.com/item?id=49468083)

**背景**: 1.1.1.1 是 Cloudflare 的公共 DNS 解析器，为全球用户提供域名查询服务。为了避免每个请求都去查询权威服务器，解析器会缓存最近的 DNS 响应；在 Cloudflare 的规模下，这个缓存包含海量条目，因此每个条目哪怕只减少一点内存，累积起来也非常可观。在 Rust 这类系统级语言中优化数据结构与内存分配，因此能带来巨大的总体节省。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/dns-cache-memory-optimization-1111/">How we saved 100 terabytes of memory by optimizing 1 . 1 . 1 . 1 ’s DNS ...</a></li>
<li><a href="https://news.ycombinator.com/item?id=49468083">Saving 100 terabytes of memory by optimizing 1 . 1 . 1 . 1 &#x27;s DNS cache</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上称赞了这一做法，有人说这是“交付软件的正确方式”，也有人指出“系统编程仍然重要”。一些人分享了相关的优化技巧，例如 Go 中结构体字段的对齐、以及用一次大的 malloc 加载黑名单条目；还有评论者质疑，把多个独立的 Vec 对象合并成一个列表是否会在某种程度上削弱 Rust 的安全保证。

**标签**: `#productivity\_boundaries`, `#dns cache optimization`, `#memory efficiency`

---

<a id="item-2"></a>
## [会计所职业责任保险实施办法公布](https://www.chinanews.com.cn/cj/2026/08-28/10685813.shtml) ⭐️ 8.0/10

财政部与国家金融监管总局联合印发《会计师事务所职业责任保险实施办法》，自 2027 年 1 月 1 日起施行。该办法为会计师事务所职业责任保险确立了强制性制度规则。 该办法落实了《注册会计师法》规定的法定制度安排，有助于增强会计师事务所的风险抵御能力，更好保护投资者及其他利害关系人。会计师事务所、保险公司和金融监管部门都将受到影响，强制性规则预计将重塑这一保险市场。 公告未披露具体投保要求、赔偿限额、保险费率及适用会计师事务所范围等细节。新闻稿未附办法全文，具体执行细则有待后续公布。

rss · 中国新闻网 - 财经 · 8月28日 06:20

**背景**: 会计师事务所职业责任保险是以会计师事务所及其执业人员因执业活动造成委托人或其他利害关系人经济损失依法应承担的赔偿责任为保险标的的保险。它是《中华人民共和国注册会计师法》规定的法定制度安排，也是国际通行的保障投资者权益、提高会计师事务所风险抵御能力的做法。中国此前于 2015 年发布过《暂行办法》，2025 年曾就修订征求意见稿公开征求意见。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://reanda.com/newsContent.php?id=13137">财政部答复：关于会计师事务所职业责任保险的相关建议！-新闻中心--利安达会计师事务所</a></li>
<li><a href="https://www.shui5.cn/article/30/142164.html">财会[2015]13号 财政部关于印发《会计师事务所职业责任保险暂行办法》的通知_税 屋——第一时间传递财税政策法规！</a></li>
<li><a href="https://kjs.mof.gov.cn/gongzuotongzhi/202511/P020251103570179144579.pdf">1 附件1 会计师事务所职业责任保险暂行办法 （修订征求意见稿） 第一章总则 第一条为进一步规范发展会计师事务所职业责任保</a></li>

</ul>
</details>

**标签**: `#game\_rules`, `#会计师事务所职业责任保险`, `#金融监管`

---

<a id="item-3"></a>
## [广西“新官不理旧账”专项治理累计清偿欠款 7.42 亿元](https://www.chinanews.com.cn/cj/2026/08-28/10685733.shtml) ⭐️ 8.0/10

广西针对“新官不理旧账”问题的专项治理已累计清偿经营主体欠款 7.42 亿元，销号率突破 80%。10 万元以下小额无分歧欠款已全部清零。 这是广西改善营商环境、提升政府公信力的实质性举措。95%的受益对象是中小微企业和个体工商户，它们获得了急需的现金流和发展信心；这一做法也可能为其他存在类似欠款问题的地区提供借鉴。 相关数据由广西壮族自治区市场监督管理局于 8 月 28 日公布。治理工作由经营主体反映问题响应处置工作专班统筹推进，该专班累计受理诉求 68.33 万件。

rss · 中国新闻网 - 财经 · 8月28日 03:54

**背景**: “新官不理旧账”是中国企业经常反映的问题，指新上任的政府官员不愿承认或履行前任作出的承诺和欠下的债务，这会损害企业信心和当地投资环境。广西此次专项治理是中国政府清理拖欠企业账款、支持民营经济发展的一系列举措之一。

**标签**: `#capital\_allocation`, `#government arrears clearance`, `#SME debt relief`

---

<a id="item-4"></a>
## [加拿大对近 200 亿美元美国商品征收 50%报复性关税](https://www.chinanews.com.cn/gj/2026/08-28/10685826.shtml) ⭐️ 8.0/10

加拿大政府于当地时间 8 月 26 日宣布，对价值近 200 亿美元的美国产品征收高达 50%的报复性关税，涵盖钢铁、家具和金枪鱼等商品。此举是对美国最新一轮对加拿大进口商品加征关税的直接回应。 这一升级标志着两大贸易伙伴之间的跨境贸易规则发生了实质性变化，将提高美国对加拿大出口商以及加拿大进口商和消费者的成本。这也表明两国之间的关税战正在加剧而非缓和。 50%的关税税率适用于价值近 200 亿美元的广泛商品，从钢铁、家具到金枪鱼。目前，措施的具体生效日期、完整产品清单、持续时间以及未来谈判的可能性仍存在不确定性。

rss · 中国新闻网 - 国际 · 8月28日 06:29

**背景**: 美国和加拿大是重要的贸易伙伴，在《美墨加协定》（USMCA）等框架下，每天有数十亿美元的商品跨越两国边界。关税战始于一国对另一国的进口商品加征关税，而受影响国家以报复性关税回应，往往导致紧张局势升级。报道标题认为，在这场对抗中加拿大拥有一个核心优势，具体内容在全文中有详细阐述。

**标签**: `#game\_rules`, `#tariffs`, `#Canada-US trade`, `#retaliatory tariffs`

---

<a id="item-5"></a>
## [Meta 支付 167 亿美元和解，限制青少年社媒使用](https://www.solidot.org/story?sid=85215) ⭐️ 8.0/10

Meta 与美国多州达成具有约束力的和解协议，同意支付约 167 亿美元，并对 Facebook 和 Instagram 的青少年用户实施新的结构性规则。规则包括默认在午夜至凌晨 6 点屏蔽访问，以及 Meta 旗下平台每日累计使用时长默认上限为两小时。 这项和解意义重大，因为它将原本自愿或存在争议的安全功能，转变为 Meta 青少年服务中具有法律约束力的平台规则。它可能重塑社交媒体公司设计青少年产品的方式，并为各州监管儿童在线安全树立先例。 这些限制被描述为默认设置，但报道未说明青少年或家长是否可以修改。相关规则的执行与监督机制也尚未披露。

rss · Solidot · 8月27日 15:29

**背景**: Meta 旗下拥有 Facebook 和 Instagram，这两个平台在青少年中广泛使用。美国各州近年来日益关注社交媒体公司如何收集儿童数据，以及成瘾性设计是否对未成年人造成伤害。此次和解通过巨额赔偿与强制性产品变更，解决了多州就儿童隐私和消费者保护提起的诉讼。

**标签**: `#game\_rules`, `#Meta和解`, `#青少年社媒限制`

---

<a id="item-6"></a>
## [亚马逊将于 9 月 30 日关闭 Mechanical Turk 众包平台](https://www.solidot.org/story?sid=85212) ⭐️ 8.0/10

亚马逊宣布 Mechanical Turk 将于 9 月 30 日永久关闭；此前该公司已于 7 月 30 日起停止接受新用户注册。该平台将彻底停止运营，其众包人工任务市场就此终结。 这标志着数据标注和微任务领域历史最悠久、使用最广泛的众包平台之一走向终结。依赖 MTurk 的研究人员、任务发布方和众包工作者需要迁移到替代平台，这也引发了对“人在回路”数据标注未来走向的疑问。 亚马逊曾在 7 月表示，现有用户可以继续正常使用服务，AWS 会继续投资改进安全性和可用性，但不会推出新功能。2023 年的一项研究发现，该平台 33% 到 46% 的众包工作者使用大语言模型完成任务，引发了对数据质量以及是否真的需要人类参与的质疑。

rss · Solidot · 8月27日 10:48

**背景**: Mechanical Turk 是亚马逊于 2005 年推出的众包平台，任务发布方可以在上面发布“人工智能任务”（HITs），例如识别图片内容、内容审核和填写调查问卷。从 2018 年起，亚马逊开始利用该平台为神经网络训练提供标注数据。随着机器人和欺骗行为增多，研究人员逐渐放弃该平台，其衰落速度加快。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Amazon_Mechanical_Turk">Amazon Mechanical Turk - Wikipedia</a></li>
<li><a href="https://www.mturk.com/">Amazon Mechanical Turk</a></li>

</ul>
</details>

**标签**: `#game\_rules`, `#amazon mechanical turk`, `#platform shutdown`, `#crowdsourcing`

---

<a id="item-7"></a>
## [Apple Maps 在搜索结果中引入付费广告](https://www.solidot.org/story?sid=85210) ⭐️ 8.0/10

Apple Maps 已开始向美国和加拿大用户在搜索结果顶部及“推荐地点”区域展示付费广告。付费商家的条目会带有蓝色“Ad”徽章。 这标志着 Apple Maps 从纯粹的功能性地图服务结构性转向广告支撑的平台，开辟了新的本地搜索广告渠道。它会影响寻求本地曝光度的广告主、现在会看到赞助结果的 Apple Maps 用户，以及 Google Maps 等本地搜索广告市场的竞争者。 广告可能基于用户的大致位置、搜索词或正在查看的地图区域进行定向，但苹果表示广告不会与用户的 Apple 帐户关联，个人数据也保留在设备上。苹果还强调，它不会收集或存储个人数据，也不会与第三方共享。

rss · Solidot · 8月27日 08:38

**背景**: Apple Maps 是苹果公司的地图服务，2012 年推出后取代 Google Maps 成为 iOS 设备上的默认地图应用。它历来没有广告，并以隐私保护为定位，这与已经展示赞助本地列表的 Google Maps 不同。苹果一直在将广告业务扩展到 App Store 之外，在地图中加入广告使其直接进入本地搜索广告领域的竞争。

**标签**: `#game\_rules`, `#Apple Maps`, `#advertising`, `#platform policy`

---

<a id="item-8"></a>
## [Anthropic 与 Nscale 签署 450 亿美元算力合同](https://www.ifanr.com/1677210?utm_source=rss&amp;utm_medium=rss&amp;utm_campaign=) ⭐️ 8.0/10

Anthropic 与 Nscale 签署了一份价值 450 亿美元的算力合同，以大规模资本投入锁定 AI 算力资源。该消息出现在中文科技媒体早报中，目前尚未公布合同原文与详细条款。 这标志着 AI 算力基础设施领域已知的最大规模资本投入之一，表明前沿 AI 实验室正在争相锁定 GPU 算力。该交易可能重塑 AI 基础设施市场，并影响下游模型训练与部署成本。 合同期限、交付时间表、融资结构以及算力是否会被完全部署等细节尚未披露。Nscale 是一家垂直整合的 AI 基础设施公司，拥有并运营从能源、数据中心、GPU 算力到云边协同的完整技术栈。

rss · 爱范儿 · 8月28日 00:09

**背景**: Nscale 是一家垂直整合的 AI 基础设施公司，在全球设计、建造和运营面向先进模型训练与推理优化的 AI 数据中心。AI 原生企业可利用 Nscale 可扩展的 GPU 集群基础设施来加速模型开发并支撑关键业务。作为领先的 AI 实验室，Anthropic 需要大量算力来训练和部署模型，因此长期算力合同成为其战略重点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nscale.com/about">About | Nscale</a></li>
<li><a href="https://www.nscale.com/">The engine of superintelligence | Nscale</a></li>
<li><a href="https://www.nscale.com/ai-infrastructure">AI Infrastructure</a></li>

</ul>
</details>

**标签**: `#capital\_allocation`, `#AI compute contract`, `#Anthropic`, `#Nscale`

---

<a id="item-9"></a>
## [英伟达季度营收 962 亿美元，首次给出一年后 70%增长指引](https://mp.weixin.qq.com/s/JTZ_ZJ_pn5vgrI_1QUyWNw) ⭐️ 8.0/10

英伟达发布 2027 财年第二季度财报，营收 962.21 亿美元，同比增长 106%，其中数据中心收入 890 亿美元，同比增长 117%。CFO 科莱特·克雷斯首次给出 2028 财年约 70%的营收增长指引，新一代 Vera Rubin 平台已于本月量产出货。 这标志着 AI 算力部署从需求受限转向供给受限，英伟达提前一年释放持续高增长的信号。AI 基础设施买家、云服务商和数据中心运营商需要围绕持续紧张的供给和快速平台迭代进行规划。 Vera Rubin 预计将为第三季度数据中心收入贡献约 20%。约 70%的 2028 财年增长是公司预测，明确受供给限制，尚未由实际客户采用情况证实。

telegram · zaihuapd · 8月27日 08:51

**背景**: Vera Rubin 是英伟达继 Blackwell 之后的下一代 AI 数据中心平台，整合新的 GPU、CPU、网络和散热方案，将数据中心视为一个计算单元。据称 Rubin 的 FP4 稀疏算力达 50 petaflops，高于 Blackwell 的 20 petaflops，专为大规模智能体 AI 和推理模型设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Rubin_%28microarchitecture%29">Rubin (microarchitecture) - Wikipedia</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/technologies/rubin/">Infrastructure for Scalable AI Reasoning | NVIDIA Vera Rubin Platform</a></li>
<li><a href="https://developer.nvidia.com/blog/inside-the-nvidia-rubin-platform-six-new-chips-one-ai-supercomputer/">Inside the NVIDIA Vera Rubin Platform: Six New Chips, One AI Supercomputer | NVIDIA Technical Blog</a></li>

</ul>
</details>

**标签**: `#productivity\_boundaries`, `#AI infrastructure`, `#Nvidia Vera Rubin`

---

<a id="item-10"></a>
## [谷歌推广 goto 跳转，搜索结果改用服务器重定向](http://google.com/goto) ⭐️ 8.0/10

谷歌已确认在搜索结果中推广 google.com/goto 服务器端跳转链接。Nozzle 在多个住宅 IP 网络中观察到覆盖率接近 100%，用户点击结果后会先经过谷歌的重定向，再到达目标网址。 这一变化几乎影响所有谷歌搜索用户，使谷歌获得一个独立于 JavaScript 跟踪的服务器端点击观测点。同时，它也提高了依赖直接目标链接的第三方抓取工具和 SEO 工具的获取门槛，可能重塑搜索数据的采集方式。 谷歌称此举旨在应对滥用行为并保护服务和用户。该跳转属于通道式基础设施变更，并非排名或索引变更，实际覆盖范围可能因地区或查询而异。

telegram · zaihuapd · 8月27日 10:14

**背景**: 谷歌搜索长期以来使用基于 JavaScript 的点击跟踪来统计结果点击。新的 google.com/goto 机制增加了服务器端重定向，即使用户禁用 JavaScript 或使用拦截跟踪的工具，谷歌仍能收集点击数据。住宅 IP 网络常被排名跟踪和抓取服务用来模拟真实用户，因此 Nozzle 在多个此类网络中观察到接近 100% 的覆盖率具有重要意义。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://squarezix.com/google-goto-url-redirects/">Google Goto URL Redirects : Everything You Need to Know</a></li>
<li><a href="https://en.inithtml.com/resources/google-switches-to-google-com-goto-a-major-change-in-search-results-for-2026/">Google Switches to google .com/ goto : A Major Change in Search...</a></li>
<li><a href="https://www.goodfellastech.com/blog/google-com-goto-redirect-what-changed-and-what-it-means-for-your-business">Google Goto Redirect : What It Means for Your Traffic</a></li>

</ul>
</details>

**标签**: `#game\_rules`, `#google search`, `#server-side redirect`, `#anti-scraping`

---

<a id="item-11"></a>
## [美国法官叫停五角大楼对 Anthropic 的供应链风险标签](https://www.bloomberg.com/news/articles/2026-08-28/anthropic-wins-court-challenge-to-us-supply-chain-risk-label?srnd=phx-technology) ⭐️ 8.0/10

2026 年 8 月 28 日，旧金山联邦地区法院裁定，特朗普政府必须解除国防部对 Anthropic 的供应链风险认定，恢复其技术供联邦机构使用的资格。法官认为该认定缺乏充分依据，且是针对 Anthropic 批评政府的报复性举措。 该裁决推翻了一项具有约束力的采购限制——此前联邦机构和国防承包商不得使用 Anthropic 的 Claude 模型，可能重塑政府 AI 采购格局。它也为《联邦采购供应链安全法》下的供应链风险权力如何适用于美国 AI 公司确立了先例。 国防部于 2026 年 3 月 4 日将 Anthropic 列为供应链风险，此前双方军事 AI 合同谈判破裂，导致承包商在为美军工作时停止使用 Claude。该裁决可能是初步裁决或面临上诉，其在所有机构中的最终适用范围及实施时间表尚未明确。

telegram · zaihuapd · 8月28日 03:15

**背景**: 2018 年《联邦采购供应链安全法》授权行政机构在采购中缓解供应链风险，包括将供应商认定为风险来源。国防部利用这一权力将 Anthropic 列为供应链风险，Anthropic 称此举是对合同纠纷的惩罚。Anthropic 随后起诉，认为该认定缺乏法律依据且具有报复性。争议期间，Anthropic 消费者下载量激增，每天有超过一百万人注册 Claude。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.armscontrol.org/act/2026-04/news-briefs/pentagon-labels-ai-company-supply-chain-risk">Pentagon Labels AI Company Supply Chain Risk | Arms Control Association</a></li>
<li><a href="https://www.dw.com/en/us-pentagon-labels-ai-company-anthropic-a-supply-chain-risk/a-76239091">US: Pentagon labels AI company Anthropic a supply chain risk</a></li>
<li><a href="https://www.npr.org/2026/03/06/g-s1-112713/pentagon-labels-ai-company-anthropic-a-supply-chain-risk">Pentagon labels AI company Anthropic a supply chain risk &#x27;effective immediately&#x27; : NPR</a></li>

</ul>
</details>

**标签**: `#game\_rules`, `#court\_ruling`, `#federal\_AI\_procurement`, `#supply\_chain\_risk`

---