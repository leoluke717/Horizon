---
layout: default
title: "Horizon Summary: 2026-09-01 (ZH)"
date: 2026-09-01
lang: zh
---

> 从 196 条内容中筛选出 5 条重要资讯。

---

1. [谷歌从 Chrome 应用商店移除 Manifest V2 扩展，包括 uBlock Origin](#item-1) ⭐️ 8.0/10
2. [加州通过年龄验证法案，Linux/BSD 获豁免](#item-2) ⭐️ 8.0/10
3. [谷歌变革搜索结果：隐藏目标 URL 并设每页 10 条上限](#item-3) ⭐️ 8.0/10
4. [爱奇艺停发点播券，专享影片并入 VIP 片库](#item-4) ⭐️ 8.0/10
5. [欧盟认定 ChatGPT、Reddit、Roblox 为超大型服务，面临更严监管](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [谷歌从 Chrome 应用商店移除 Manifest V2 扩展，包括 uBlock Origin](https://webiterate.dev/google-removed-extensions-ublock-origin-108/) ⭐️ 8.0/10

谷歌已从 Chrome 应用商店移除 Manifest V2 \(MV2\) 扩展，包括流行的广告拦截工具 uBlock Origin，以此强制执行向 Manifest V3 的过渡。这一移除标志着影响 Chrome 扩展工作方式的平台规则发生了决定性改变。 此事意义重大，因为基于 MV2 的广告拦截工具（尤其是 uBlock Origin）依赖 Chrome 新 MV3 框架所限制的 blocking webRequest API。Chrome 用户将失去最强大的广告拦截选择，扩展开发者必须按更严格的规则重写扩展；许多用户也可能会转向 Firefox。 uBlock Origin 仍可在 Firefox 上使用，它仍在积极维护，并可从 addons.mozilla.org 安装。移除的确切范围，包括企业或托管设备是否豁免，仍存在不确定性。

hackernews · twapi · 8月31日 21:10 · [社区讨论](https://news.ycombinator.com/item?id=49514878)

**背景**: Manifest V2 \(MV2\) 是 Chrome 较旧的扩展规范，而 Manifest V3 \(MV3\) 是为了更好安全性、隐私和性能而引入的新平台。MV3 限制了一些强大的 API，特别是广告拦截器用来在请求加载前过滤网络请求的 blocking webRequest API。谷歌从 Chrome 应用商店移除 MV2 扩展，是这一早就宣布的过渡的最终执行，迫使 uBlock Origin 等扩展要么适应 MV3 的限制，要么被功能较弱的版本取代。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/UBlock_Origin">uBlock Origin - Wikipedia</a></li>
<li><a href="https://ublockorigin.com/">uBlock Origin - Free, open-source ad blocker extension</a></li>
<li><a href="https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/">uBlock Origin – Get this Extension for 🦊 Firefox (en-US)</a></li>

</ul>
</details>

**社区讨论**: 评论者大多对谷歌表示不满，并敦促用户改用 Firefox；他们指出广告拦截已成为不太懂技术的用户的安全问题。一些人回忆 Chrome 早期的受欢迎程度，并对比今天对单一公司单方面控制网络的担忧。还有人指出 uBlock Origin 在 Firefox 上本来就表现最好。

**标签**: `#game\_rules`, `#Chrome Web Store`, `#Manifest V2 removal`, `#ad blocking`

---

<a id="item-2"></a>
## [加州通过年龄验证法案，Linux/BSD 获豁免](https://www.solidot.org/story?sid=85245) ⭐️ 8.0/10

加州参众两院通过了第 1856 号议会法案，要求消费级操作系统在账户设置时收集出生日期或年龄，并通过 API 提供数字年龄信号。该法案豁免 Linux 和 BSD，预计在州长签署后于 2027 年 1 月 1 日生效。 若该法案签署成法，将直接影响 Apple、Google、Microsoft 等商业操作系统提供商，以及在加州运营的应用商店和开发者。它可能为各州层面的年龄验证要求开创先例，并重新引发关于隐私、数据最小化和开源软件豁免的讨论。 该年龄信号不会显示精确出生日期，而是提供四个年龄段之一：13 岁以下、13–15 岁、16–17 岁或 18 岁及以上。对于 2027 年 1 月 1 日之前售出的设备，提供商必须在 2027 年 7 月 1 日前提供界面，让账户持有人补充年龄信息。

rss · Solidot · 8月31日 15:47

**背景**: 第 1856 号议会法案修订了加州《数字年龄保证法案》（DAAA）。从 2027 年 1 月 1 日起，DAAA 要求操作系统提供商在账户设置时提供可访问的年龄标示界面，并对受监管的应用商店施加义务，同时禁止超出法律要求索取年龄信号。该法案特意豁免 Linux、BSD 等开源操作系统，这类系统通常没有集中的账户或应用商店生态。这一豁免体现了法案针对大型商业平台，而非社区维护的系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202520260AB1856">Bill Text - AB-1856 Age verification signals: software applications.</a></li>
<li><a href="https://legiscan.com/CA/text/AB1856/id/3456513">Bill Text: CA AB1856 | 2025-2026 | Regular Session | Amended | LegiScan</a></li>
<li><a href="https://calmatters.digitaldemocracy.org/bills/ca_202520260ab1856">AB 1856: Age verification signals: software applications.</a></li>

</ul>
</details>

**标签**: `#game\_rules`, `#age verification`, `#California law`, `#operating systems`, `#privacy regulation`

---

<a id="item-3"></a>
## [谷歌变革搜索结果：隐藏目标 URL 并设每页 10 条上限](https://www.solidot.org/story?sid=85242) ⭐️ 8.0/10

谷歌改变了搜索结果链接的显示方式，用 google.com/goto 重定向链接取代了直接的目标 URL。它还取消了 &amp;num=100 参数，将每页结果限制为 10 条。 这些变化通过降低链接透明度和用户可控性，影响了所有谷歌搜索用户、网站所有者、SEO 从业者及重度搜索用户。被隐藏的重定向链接也影响了 AI Overview 的引用来源，使验证来源更加困难。 google.com/goto 重定向也出现在 AI Overview 的引用链接中。被取消的 &amp;num=100 参数此前可支持每页最多 100 条结果，如今用户需要翻页 10 次才能看到同样数量的结果；该变化已获第三方报道确认，但谷歌尚未正式公布。

rss · Solidot · 8月31日 11:35

**背景**: 在典型的搜索引擎中，搜索结果是以指向网站的直接超链接形式出现，悬停在结果上时浏览器的状态栏会显示目标 URL。谷歌的新重定向 URL 会让用户先经过 google.com 再跳转，从而隐藏真实地址，这可能是出于追踪或安全考虑。AI Overview 是搜索结果顶部的 AI 生成摘要，其中包含带链接的来源。&amp;num 参数是一种非官方但被广泛使用的查询技巧，用来控制每页显示的结果数量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://serpapi.com/blog/googles-new-goto-redirect-urls-resolution-in-progress/">Google ’s New /goto Redirect URLs : Resolution in Progress</a></li>
<li><a href="https://search.google/ways-to-search/ai-overviews/">Google AI Overviews - Search anything, effortlessly</a></li>

</ul>
</details>

**标签**: `#game\_rules`, `#google search`, `#search interface policy`, `#dominant platform`

---

<a id="item-4"></a>
## [爱奇艺停发点播券，专享影片并入 VIP 片库](https://www.ithome.com/0/996/261.htm) ⭐️ 8.0/10

自 2026 年 9 月 1 日起，爱奇艺将不再发放点播券。原先需要使用点播券的专享影片将全面纳入 VIP 会员片库，VIP 会员可直接免费观看。 这一举措简化了爱奇艺的会员体系，消除了用户对额外付费的困惑。这也反映出行业正趋向于将会员专享优质内容整合进订阅服务，而不是采用单片租借等额外付费模式。 已领取的点播券近期仍可在会员中心“我的会员资产—点播券”列表中查看，该资产列表将于 2026 年 10 月 8 日下线。官方公告未说明未使用点播券的具体补偿方式，也未提及是否存在地区性例外。

telegram · zaihuapd · 8月31日 02:41

**背景**: 点播券是爱奇艺推出的一种观影券，用户可在观看好莱坞点播付费影片时使用，无需额外付费，有效期通常为一个月。点播券至少从 2015 年起通过活动或会员权益发放，用户可在爱奇艺 App 内兑换观看特定付费影片。此次调整后，这些影片将纳入标准的 VIP 会员订阅范围。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://m.300.cn/itzspd/445761.html">爱奇艺点播券是做什么用 - IT知识教程 - 中企动力</a></li>
<li><a href="https://zhidao.baidu.com/question/520535736813267525">爱奇艺的点播券是做什么用的？_百度知道</a></li>

</ul>
</details>

**社区讨论**: 该新闻没有提供社区评论。

**标签**: `#game\_rules`, `#iQiyi`, `#streaming`, `#video subscription`

---

<a id="item-5"></a>
## [欧盟认定 ChatGPT、Reddit、Roblox 为超大型服务，面临更严监管](https://www.euronews.com/next/2026/08/31/eu-places-chatgpt-reddit-and-roblox-under-strictest-digital-safety-rules) ⭐️ 8.0/10

8 月 31 日，欧盟委员会依据《数字服务法》将 ChatGPT 认定为超大型在线搜索引擎，将 Reddit 和 Roblox 认定为超大型在线平台，因这三项服务在欧盟的月均活跃用户均超过 4500 万。 这一认定使这三项服务承担《数字服务法》下最严格的义务，包括年度系统性风险评估、独立审计以及与监管机构和研究人员共享数据。这为生成式 AI 和游戏平台在欧盟的监管开创了先例。 这些公司有四个月的过渡期来合规。义务重点涉及非法内容、未成年人保护和用户身心健康，包括与经审核的研究人员共享数据。

telegram · zaihuapd · 8月31日 14:39

**背景**: 欧盟《数字服务法》（DSA）对超大型在线平台（VLOP）和超大型在线搜索引擎（VLOSE）在被认定后施加额外义务。根据第 34 条，这些服务必须开展年度系统性风险评估，涵盖成瘾性设计、推荐系统危害等问题。欧盟委员会基于这些服务在欧盟的规模作出了认定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/dsa-vlops">DSA : Very large online platforms and search engines</a></li>
<li><a href="https://zertia.ai/resources/regulatory-frameworks/references/eu-dsa-algorithmic-transparency/">EU DSA Algorithmic Transparency - Zertia</a></li>
<li><a href="https://dsa-observatory.eu/2026/03/09/how-have-platforms-addressed-addictive-design-under-dsa/">How Have Platforms Addressed Addictive Design Under DSA</a></li>

</ul>
</details>

**标签**: `#game\_rules`, `#DSA`, `#VLOP`, `#VLOSE`, `#digital regulation`

---