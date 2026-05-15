---
name: competitor-demand-research
description: Use this skill when the user wants to judge whether a product, AI tool, niche, keyword, Xiaohongshu item, virtual product, SaaS idea, marketplace service, or business opportunity has real demand and is worth betting on. This skill focuses on practical opportunity research for small teams: whether users are already paying, how fast orders appear within 24 hours, 48 hours, one week, or one month, whether Xiaohongshu notes are going viral, whether competitors are few or weak, whether current sellers are unprofessional but still making sales, whether traffic is precise and reachable, and whether the user can achieve 降维打击. It should output demand evidence, paid validation level, Xiaohongshu validation, competitor map, revenue range, risk signals, and a direct Go / Small Bet / Observe / Reject decision. Trigger when the user mentions 竞品分析, 需求调研, 选品, 蓝海, 小红书选品, AI产品调研, 付费验证, 订单量, 爆款笔记, 同行竞争, 对手弱, 降维打击, 产品机会, 这个项目能不能做, or 这个产品值不值得做.
---

# Competitor Demand Research Skill

## Mission

This skill turns a product idea, competitor, keyword, AI tool, Xiaohongshu item, virtual product, SaaS idea, or business opportunity into a practical go/no-go business decision.

The goal is not to produce a generic market research report. The goal is to answer:

> Is there real demand, are users already paying, how strong are the competitors, where will traffic come from, how much money can it roughly make, and can a small team beat the current players?

## Core Philosophy

1. Search behavior equals demand, but search volume alone does not prove payment willingness.
2. Complaints reveal pain. Repeated complaints usually mean current solutions are weak.
3. Paid behavior is the strongest validation. Real purchases beat likes, saves, comments, and hype.
4. A market with no competitors is not automatically a blue ocean. It may hide weak demand, low payment willingness, legal risk, bad retention, or difficult traffic.
5. For small teams, “打得过” can be treated as practical blue ocean.
6. The best opportunities often look like: clear demand, weak or few competitors, reachable traffic, high-margin delivery, and room for 降维打击.
7. Prefer precise traffic over broad traffic. Broad traffic may look large but often converts poorly.
8. Do not build just because a trend is hot. Validate demand, payment, traffic, competition, and build cost first.
9. Do not invest heavily in products whose user pain cannot be personally experienced or understood.
10. Favor opportunities where time creates compounding assets: content, SEO pages, private-domain users, product data, templates, workflows, brand trust, or operational SOPs.

## Required Inputs

When possible, collect:

- Product name, competitor URL, keyword, niche, or rough idea
- Target market: China, global, or both
- Target users
- Core use case
- Known competitors
- Possible pricing
- Expected traffic channel
- Build difficulty
- Whether the user can personally experience the pain
- Whether this is an AI product, virtual product, SaaS, tool site, service, content product, or marketplace opportunity

If information is missing, continue with reasonable assumptions and mark them as `待验证假设`.

## Workflow

### Step 1: Define the Opportunity

Clarify:

- Product / niche name
- One-sentence description
- Target users
- Core problem
- Core usage scenario
- Current substitute solution
- Why now
- China / global market distinction

Ask:

- Who needs this?
- In what scenario do they need it?
- Is this frequent or occasional?
- Is the pain strong enough to pay for?
- Is the need productivity, emotional, compliance, education, entertainment, or business-driven?

### Step 2: Find Demand Evidence

Evaluate four demand sources:

1. Search demand
   - Baidu Index, WeChat Index, 5118, Zhihu views, Google Trends, Google Suggest, Similarweb, Semrush, AITDK, allintitle, KGR.
2. Pain demand
   - Reddit, Twitter/X, Zhihu, Xiaohongshu, Bilibili, YouTube comments, app reviews, Chrome extension reviews, Discord, forums, private-domain feedback.
3. Market demand
   - SaaS tools, AI tool directories, Product Hunt, AppSumo, Gumroad, Fiverr, Upwork, Chrome Web Store, WordPress plugins, Xiaohongshu shops, Douyin shops, Taobao, Xianyu, Pinduoduo.
4. Technology breakthrough demand
   - New AI models, GitHub open-source projects, Hugging Face models, new API capabilities, platform changes, migration from old platform demand to new platform demand.

Always distinguish:

- Interest signal: likes, saves, views, comments, wishful thinking.
- Demand signal: search, complaints, repeated questions, user workarounds.
- Payment signal: purchases, orders, reviews, renewals, subscriptions, repeat purchases.

### Step 3: Check Paid Validation

Before judging an opportunity as attractive, check whether real paid behavior exists.

Do not treat likes, views, bookmarks, or discussion as paid validation.

Look for:

- Real purchases
- Order count
- Sales velocity
- Paid user feedback
- Repeat purchase
- Subscription or renewal
- Review screenshots
- Store sales
- Comments asking how to buy
- Marketplace transaction traces
- Paid tool usage
- Paid service demand

Classify paid validation:

- Weak: interest only, no clear purchase.
- Medium: some purchases and early user feedback.
- Strong: stable weekly or monthly orders.
- Very Strong: 1000+ or 10000+ order-level signal, depending on timeframe, category, price, and product type.

Evaluate order quality by:

- Timeframe
- Price
- Margin
- Refund risk
- Support burden
- Repeat purchase
- Whether demand comes from precise traffic or broad traffic

### Step 4: Xiaohongshu Product Validation

When analyzing Xiaohongshu opportunities, evaluate:

1. Does the related account's content explode?
2. Is the product selling within 24 hours, 48 hours, one week, and one month?
3. How many similar competitors exist?
4. How strong are those competitors?
5. Are competitors professional or amateur?
6. Is demand strong even when competitors promote poorly?

Check:

- Note volume
- Recent note performance
- Number of viral notes
- Viral rate
- Comment purchase intent
- Store sales
- Account professionalism
- Competitor count
- Competitor quality
- Private-domain conversion
- Whether multiple accounts can sell the same product

Strongest signal:

> Competitors are unprofessional, traffic work is poor, but users still buy.

This usually means demand may be strong and current supply may be weak.

### Step 5: Analyze Competitors

Include direct competitors, indirect competitors, manual substitutes, platform substitutes, and informal sellers.

For each competitor, analyze:

- Product name
- Platform / URL
- Target users
- Core features
- Pricing
- Traffic source
- Estimated traffic
- Estimated revenue
- UX quality
- Product maturity
- Brand strength
- SEO strength
- Social presence
- User complaints
- Weaknesses
- Whether we can beat them

Use this table:

| Competitor | Type | Strength | Weakness | Pricing | Traffic | Can Beat? | How to Beat |
|---|---|---|---|---|---|---|---|

### Step 6: Judge Competition Strength

Rate:

- Competitor quantity: 0-5
- Competitor quality: 0-5
- Traffic moat: 0-5
- Product moat: 0-5
- Small-seller opportunity: 0-5

Do not assume zero competitors means good opportunity. Weak competitors plus clear demand is usually better.

### Step 7: Estimate Revenue Range

Revenue estimates must be shown as assumptions, not truth.

Use low / middle / high estimates.

Common formulas:

```text
Tool site revenue = monthly visitors × paid conversion rate × ARPPU
Private-domain revenue = leads × add-WeChat rate × payment conversion × average order value
Marketplace revenue = monthly orders × unit price × gross margin
SaaS MRR = paying users × monthly price
Competitor estimate = estimated monthly visits × estimated conversion rate × estimated ARPPU
```

Always include:

- Key assumptions
- Conservative estimate
- Middle estimate
- Optimistic estimate
- Major risks to the estimate

### Step 8: Analyze Traffic Strategy

Do not build before knowing where users come from.

Evaluate:

- Search traffic: keywords, KGR, SEO difficulty, landing pages, programmatic SEO
- Social traffic: Xiaohongshu, Douyin, Bilibili, YouTube, TikTok, X, Reddit, Zhihu
- Marketplace traffic: Xianyu, Pinduoduo, Taobao, Fiverr, Upwork, app stores, plugin marketplaces
- Private-domain traffic: WeChat, communities, newsletters, customer service, repeat purchase
- Partner traffic: affiliates, agents, resellers, creators

Principle:

> Precise small traffic can be more valuable than broad large traffic.

### Step 9: Product Entry Point

Define the smallest product that solves the core pain.

Ask:

- What is the MVP?
- What 20% of a large product creates 80% of the value?
- What proven competitor interaction can be reused?
- What can be improved immediately?
- What feature do users want but large products ignore?
- What can be automated by AI?
- What can be delivered faster, cheaper, or with better UX?

Use “暗影复刻” carefully:

> Replicate 20% of the core value of a large product, then add one or two features that users want but the large product has not prioritized.

Do not blindly clone. Clone validated workflows, then differentiate.

### Step 10: Risks and False Demand

Always look for反证.

Potential risks:

- Users only want free solutions.
- Competitors look weak but have hidden private-domain traffic.
- Product is easy to copy and has no moat.
- API cost destroys margin.
- Customer support is too heavy.
- Legal / copyright / platform risk is high.
- Demand is seasonal.
- Users are not reachable.
- Product requires trust that a new brand cannot easily build.
- Idea is interesting but not painful.
- The user cannot personally understand the scenario.
- The project consumes time but does not create compounding assets.

### Step 11: Score the Opportunity

Use this model:

```text
Demand Clarity: 15
Paid Validation Strength: 20
Xiaohongshu / Content Traffic Validation: 15
Market Size: 10
Competitor Weakness: 15
Traffic Reachability: 10
Build Feasibility: 10
Compounding Potential: 5
Total: 100
```

Risk penalties:

```text
Legal risk: -10 to -30
High support burden: -5 to -15
No personal experience: -10
No clear traffic path: -15
No paid signal: -15
Strong incumbents: -10 to -30
```

Interpretation:

```text
85-100: Strong opportunity. Worth entering quickly.
70-84: Good opportunity. Build MVP or run a small test.
55-69: Unclear opportunity. Continue research or test cheaply.
40-54: Weak opportunity. Watch only.
Below 40: Avoid.
```

### Step 12: Make Decision

Final decision must be one of:

- Go Now: demand clear, competition beatable, traffic path clear, monetization realistic.
- Small Bet: promising but uncertain; test with landing page, content, manual delivery, or MVP first.
- Observe: interesting but not enough evidence.
- Reject: weak demand, strong competition, poor monetization, or bad strategic fit.

Do not give vague conclusions.

## Output Format

```markdown
# 竞品需求分析报告：{产品/赛道/关键词}

## 1. 一句话结论

Go Now / Small Bet / Observe / Reject。直接说原因。

## 2. 机会定义

- 产品/赛道：
- 目标用户：
- 使用场景：
- 解决的问题：
- 中国市场 / 海外市场：
- 当前用户替代方案：

## 3. 需求证据

| 证据类型 | 来源 | 信号 | 强度 | 备注 |
|---|---|---|---|---|

## 4. 付费验证判断

- 是否已有真实购买：
- 订单规模：
- 成交周期：
- 客单价：
- 复购/续费迹象：
- 用户反馈：
- 订单含金量：
- 付费验证等级：弱 / 中 / 强 / 极强

## 5. 小红书验证

- 相关账号数量：
- 相关笔记数量：
- 24 小时表现：
- 48 小时表现：
- 一周表现：
- 一个月表现：
- 爆款率：
- 评论区购买意图：
- 同行数量：
- 同行专业度：
- 是否存在“对手弱但卖得动”：
- 小红书机会判断：A / B / C / D

## 6. 需求量级判断

- 搜索需求：
- 痛点需求：
- 付费需求：
- 趋势需求：
- 综合判断：

## 7. 竞品地图

| 竞品 | 类型 | 功能 | 定价 | 流量来源 | 强点 | 弱点 | 是否打得过 |
|---|---|---|---|---|---|---|---|

## 8. 竞争强度判断

- 对手数量：
- 对手质量：
- 流量壁垒：
- 产品壁垒：
- 小团队是否有机会降维打击：

## 9. 蓝海判断

- 是否需求明确：
- 是否对手少：
- 是否对手弱：
- 是否有可触达流量：
- 是否能做出差异化：
- 结论：

## 10. 盈利区间估算

### 保守估算
- 假设：
- 月收入：
- 年收入：

### 中位估算
- 假设：
- 月收入：
- 年收入：

### 乐观估算
- 假设：
- 月收入：
- 年收入：

## 11. 流量打法

- 精准关键词：
- 泛关键词：
- SEO机会：
- 社交媒体机会：
- 平台/市场机会：
- 私域机会：
- 推荐优先级：

## 12. 产品切入点

- MVP核心功能：
- 可以复刻的竞品流程：
- 可以超越竞品的地方：
- 用户愿意付费的点：
- 需要砍掉的非核心功能：

## 13. 时间成本与复利判断

- 开发成本：
- 运营成本：
- 客服成本：
- 是否可自动化：
- 是否可复购：
- 是否能积累内容/数据/用户/品牌：
- 是否值得长期做：

## 14. 风险与反证

- 最大风险：
- 伪需求可能性：
- 法律/平台风险：
- 成本风险：
- 流量风险：
- 竞争风险：

## 15. 评分

| 维度 | 分数 |
|---|---|
| 需求清晰度 | /15 |
| 付费验证强度 | /20 |
| 小红书/内容流量验证 | /15 |
| 市场量级 | /10 |
| 对手弱度 | /15 |
| 流量可达性 | /10 |
| 建设可行性 | /10 |
| 复利潜力 | /5 |
| 风险扣分 |  |
| 总分 | /100 |

## 16. 最终建议

- Go Now / Small Bet / Observe / Reject
- 推荐验证动作
- 第一阶段应该做什么
- 不应该做什么
```

## Quality Rules

The answer must:

- Avoid empty business jargon.
- Avoid pretending estimates are exact.
- Always show assumptions.
- Compare demand and competition together.
- Distinguish broad traffic from precise traffic.
- Identify whether competitors are truly weak.
- Include revenue range, not a single number.
- Include go/no-go decision.
- Include risks and反证.
- Favor practical small-team execution.
- Respect the principle: do not build what cannot be personally understood or experienced.

## Bad Output Examples

Do not say:

```text
这个市场很有潜力，建议可以尝试。
```

Instead say:

```text
这个项目建议 Small Bet。需求有一定证据，但付费信号不足。先不要开发完整产品，建议用一个落地页 + 3篇精准SEO文章 + 小红书/私域人工交付测试，验证是否有人愿意付费。验证通过后再做MVP。
```

## Final Principle

The purpose of this skill is to help the user move from:

```text
会做功能
```

to:

```text
会做让用户愿意付费的功能
```

The best opportunities are often:

```text
需求明确
用户已经付费
对手不强
流量可达
成本可控
时间投入后能沉淀资产
```
