---
layout: default
title: "Horizon Summary: 2026-09-01 (EN)"
date: 2026-09-01
lang: en
---

> From 196 items, 5 important content pieces were selected

---

1. [Google Removes Manifest V2 Extensions, Including uBlock Origin, from Chrome Web Store](#item-1) ⭐️ 8.0/10
2. [California Passes Age-Verification Bill Exempting Linux and BSD](#item-2) ⭐️ 8.0/10
3. [Google Revamps Search Results: Hidden URLs and 10-Result Page Cap](#item-3) ⭐️ 8.0/10
4. [iQiyi Ends Pay-Per-View Coupons, Moves Exclusive Films to VIP Library](#item-4) ⭐️ 8.0/10
5. [EU labels ChatGPT, Reddit, Roblox as very large services under DSA](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Google Removes Manifest V2 Extensions, Including uBlock Origin, from Chrome Web Store](https://webiterate.dev/google-removed-extensions-ublock-origin-108/) ⭐️ 8.0/10

Google has removed Manifest V2 \(MV2\) extensions from the Chrome Web Store, including the popular ad blocker uBlock Origin, as it enforces the transition to Manifest V3. This removal marks a definitive platform-rule change that affects how Chrome extensions can operate. This matters because MV2-based ad blockers, especially uBlock Origin, rely on the blocking webRequest API that Chrome&\#x27;s new MV3 framework restricts. Chrome users will lose the most powerful ad-blocking option, while developers must rewrite extensions under stricter rules; many users may also migrate to Firefox. uBlock Origin remains available for Firefox, where it is actively maintained and can still be installed from addons.mozilla.org. The exact scope of the removal, including possible enterprise or managed-device exemptions, remains uncertain.

hackernews · twapi · Aug 31, 21:10 · [Discussion](https://news.ycombinator.com/item?id=49514878)

**Background**: Manifest V2 \(MV2\) is the older extension specification for Chrome, while Manifest V3 \(MV3\) is the new platform introduced for better security, privacy, and performance. MV3 restricts some powerful APIs, particularly the blocking webRequest API used by ad blockers to filter network requests before they load. Google&\#x27;s removal of MV2 extensions from the Chrome Web Store is the final enforcement of this long-announced transition, forcing extensions like uBlock Origin either to adapt to MV3 limitations or to be replaced by less powerful versions.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/UBlock_Origin">uBlock Origin - Wikipedia</a></li>
<li><a href="https://ublockorigin.com/">uBlock Origin - Free, open-source ad blocker extension</a></li>
<li><a href="https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/">uBlock Origin – Get this Extension for 🦊 Firefox (en-US)</a></li>

</ul>
</details>

**Discussion**: Commenters largely express frustration with Google and urge users to switch to Firefox, noting that ad blocking has become a safety issue for less tech-savvy users. Some recall Chrome&\#x27;s early popularity and contrast it with today&\#x27;s concern about a single company having unilateral control over the web. Several point out that uBlock Origin always worked best in Firefox anyway.

**Tags**: `#game\_rules`, `#Chrome Web Store`, `#Manifest V2 removal`, `#ad blocking`

---

<a id="item-2"></a>
## [California Passes Age-Verification Bill Exempting Linux and BSD](https://www.solidot.org/story?sid=85245) ⭐️ 8.0/10

The California Assembly and Senate passed Assembly Bill 1856, which requires consumer operating systems to collect age or birth date at account setup and share a digital age signal through an API. The bill exempts Linux and BSD and is expected to take effect January 1, 2027, after the governor&\#x27;s action. If signed, this law would directly affect commercial operating system providers such as Apple, Google, and Microsoft, as well as app stores and developers doing business in California. It could set a precedent for state-level age-verification mandates and renew debates over privacy, data minimization, and open-source software exemptions. The age signal does not reveal an exact birth date; instead it reports one of four brackets: under 13, 13–15, 16–17, or 18 and older. For devices sold before January 1, 2027, providers must offer an interface for account holders to supply age information by July 1, 2027.

rss · Solidot · Aug 31, 15:47

**Background**: Assembly Bill 1856 amends California&\#x27;s Digital Age Assurance Act \(DAAA\), a law that, beginning January 1, 2027, requires operating system providers to offer accessible account-setup interfaces for age indication. It also imposes obligations on covered application stores and prohibits requesting an age signal beyond what the law requires. The bill intentionally exempts open-source operating systems like Linux and BSD, which typically do not have centralized account or app-store ecosystems. This exemption reflects the law&\#x27;s focus on large commercial platforms rather than community-maintained systems.

<details><summary>References</summary>
<ul>
<li><a href="https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202520260AB1856">Bill Text - AB-1856 Age verification signals: software applications.</a></li>
<li><a href="https://legiscan.com/CA/text/AB1856/id/3456513">Bill Text: CA AB1856 | 2025-2026 | Regular Session | Amended | LegiScan</a></li>
<li><a href="https://calmatters.digitaldemocracy.org/bills/ca_202520260ab1856">AB 1856: Age verification signals: software applications.</a></li>

</ul>
</details>

**Tags**: `#game\_rules`, `#age verification`, `#California law`, `#operating systems`, `#privacy regulation`

---

<a id="item-3"></a>
## [Google Revamps Search Results: Hidden URLs and 10-Result Page Cap](https://www.solidot.org/story?sid=85242) ⭐️ 8.0/10

Google has changed how search results links are displayed, replacing direct destination URLs with google.com/goto redirect links. It also removed the &amp;num=100 parameter, limiting results to 10 per page. These changes affect all Google Search users, website owners, SEO professionals, and heavy search users by reducing link transparency and user control. The obscured redirect links also impact AI Overview citations, making it harder to verify sources. The google.com/goto redirect also appears in AI Overview citations. The removed &amp;num=100 parameter previously allowed up to 100 results per page; now users must click through 10 pages for the same results, and the change has been confirmed by third-party reports but not officially announced.

rss · Solidot · Aug 31, 11:35

**Background**: In a typical search engine, results appear as direct hyperlinks to websites, and hovering over a result shows the destination URL in the browser&\#x27;s status bar. Google&\#x27;s new redirect URLs route users through google.com first, obscuring the actual destination, possibly for tracking or security purposes. AI Overviews are AI-generated summaries at the top of search results that include linked sources. The &amp;num parameter was an undocumented but widely used query trick to control how many results appear per page.

<details><summary>References</summary>
<ul>
<li><a href="https://serpapi.com/blog/googles-new-goto-redirect-urls-resolution-in-progress/">Google ’s New /goto Redirect URLs : Resolution in Progress</a></li>
<li><a href="https://search.google/ways-to-search/ai-overviews/">Google AI Overviews - Search anything, effortlessly</a></li>

</ul>
</details>

**Tags**: `#game\_rules`, `#google search`, `#search interface policy`, `#dominant platform`

---

<a id="item-4"></a>
## [iQiyi Ends Pay-Per-View Coupons, Moves Exclusive Films to VIP Library](https://www.ithome.com/0/996/261.htm) ⭐️ 8.0/10

Starting September 1, 2026, iQiyi will stop issuing pay-per-view coupons \(点播券\). Exclusive films previously requiring coupons will be fully incorporated into the VIP membership library, so VIP members can watch them directly at no extra cost. This simplifies iQiyi&\#x27;s membership model and removes a source of confusion for subscribers. It also signals a broader industry shift toward consolidating premium content within subscription tiers rather than à la carte rental. Existing coupon holders can still view their coupons under &\#x27;My Member Assets—点播券&\#x27; until the asset list is taken offline on October 8, 2026. The official announcement does not specify how unused coupons will be compensated or whether regional exceptions apply.

telegram · zaihuapd · Aug 31, 02:41

**Background**: 点播券 \(pay-per-view coupons\) are iQiyi vouchers that let users watch Hollywood on-demand premium movies without paying extra, with a validity period of about one month. They have been issued since at least 2015 as part of promotions or membership perks, and are redeemed within the iQiyi app to unlock specific pay-per-view titles. The change means these titles will now be part of the standard VIP subscription.

<details><summary>References</summary>
<ul>
<li><a href="https://m.300.cn/itzspd/445761.html">爱奇艺点播券是做什么用 - IT知识教程 - 中企动力</a></li>
<li><a href="https://zhidao.baidu.com/question/520535736813267525">爱奇艺的点播券是做什么用的？_百度知道</a></li>

</ul>
</details>

**Discussion**: No community comments were provided for this news item.

**Tags**: `#game\_rules`, `#iQiyi`, `#streaming`, `#video subscription`

---

<a id="item-5"></a>
## [EU labels ChatGPT, Reddit, Roblox as very large services under DSA](https://www.euronews.com/next/2026/08/31/eu-places-chatgpt-reddit-and-roblox-under-strictest-digital-safety-rules) ⭐️ 8.0/10

On August 31, the European Commission designated ChatGPT as a very large online search engine and Reddit and Roblox as very large online platforms under the Digital Services Act, because each has over 45 million monthly active users in the EU. The designation subjects these services to the DSA&\#x27;s strictest obligations, including annual systemic risk assessments, independent audits, and data sharing with regulators and researchers. This sets a precedent for how generative AI and gaming platforms are regulated in the EU. The companies have a four-month transition period to comply. Obligations focus on illegal content, minor protection, and user wellbeing, and include data sharing with vetted researchers.

telegram · zaihuapd · Aug 31, 14:39

**Background**: The EU Digital Services Act \(DSA\) imposes extra obligations on very large online platforms \(VLOPs\) and very large online search engines \(VLOSEs\) once they are designated. Under Article 34, these services must conduct annual systemic risk assessments covering issues such as addictive design and recommender-system harms. The Commission has designated these services due to their scale in the EU.

<details><summary>References</summary>
<ul>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/dsa-vlops">DSA : Very large online platforms and search engines</a></li>
<li><a href="https://zertia.ai/resources/regulatory-frameworks/references/eu-dsa-algorithmic-transparency/">EU DSA Algorithmic Transparency - Zertia</a></li>
<li><a href="https://dsa-observatory.eu/2026/03/09/how-have-platforms-addressed-addictive-design-under-dsa/">How Have Platforms Addressed Addictive Design Under DSA</a></li>

</ul>
</details>

**Tags**: `#game\_rules`, `#DSA`, `#VLOP`, `#VLOSE`, `#digital regulation`

---