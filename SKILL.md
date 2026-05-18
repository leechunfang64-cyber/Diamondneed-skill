---
name: competitor-demand-research
description: Use this skill when the user wants to judge whether a product, AI tool, niche, keyword, Xiaohongshu item, virtual product, SaaS idea, marketplace service, competitor, or business opportunity has real demand and is worth betting on. It must produce evidence-backed demand judgment, paid validation level, competitor strength, traffic path, revenue range, risk signals, and a direct Go Now / Small Bet / Observe / Reject decision. Trigger on requests such as 竞品分析, 需求调研, 选品, 蓝海判断, 小红书选品, AI产品调研, 付费验证, 订单量, 爆款笔记, 同行竞争, 对手弱, 降维打击, 产品机会, 这个项目能不能做, 这个产品值不值得做, and 估算竞品收入.
---

# Competitor Demand Research

## Mission

Turn a product idea, competitor, keyword, AI tool, Xiaohongshu item, virtual product, SaaS idea, or business opportunity into a practical go/no-go decision.

The goal is not a generic market report. The goal is to answer:

```text
有没有真实需求？
有没有人已经付费？
对手强不强？
流量从哪里来？
大概能赚多少钱？
小团队能不能打？
下一步应该做什么？
```

## Non-Negotiable Rules

- Always end with exactly one decision: `Go Now`, `Small Bet`, `Observe`, or `Reject`.
- Do not treat likes, saves, views, comments, or hype as paid validation.
- Do not assume "no competitors" means blue ocean. It may mean weak demand, hard traffic, legal risk, or low willingness to pay.
- Separate `事实`, `假设`, and `推断`. If evidence is missing, mark it as `待验证假设`.
- Prefer precise traffic over broad traffic. Big traffic with weak purchase intent is usually a trap.
- Always look for negative evidence before recommending entry.
- Never output a single exact revenue number. Use conservative / middle / optimistic ranges with assumptions.
- If the user asks for current market facts, live competitor data, prices, search results, order signals, or latest trends, gather fresh evidence and cite sources when tools allow it.
- If fresh evidence cannot be gathered, say so directly and lower confidence.

## Input Handling

Collect or infer these fields:

- Product, competitor URL, keyword, niche, or rough idea
- Target market: China, global, or both
- Target users and core scenario
- Current substitute solution
- Known competitors
- Possible pricing
- Expected traffic channel
- Build and delivery difficulty
- Whether the user can personally experience the pain
- Product type: AI tool, SaaS, virtual product, service, content product, marketplace opportunity, or tool site

Ask a clarifying question only when the missing information blocks a useful decision. Otherwise continue with assumptions and label them.

## Output Mode Selector

Choose the smallest output that still supports a useful decision.

### Quick Judgment

Use when the user asks a rough question, gives little evidence, or wants fast direction.

Must include:

1. 一句话结论
2. 当前证据强弱
3. 最大风险
4. 最小验证动作
5. 不建议先做什么
6. Final decision

### Standard Report

Default mode for one product, one keyword, one competitor, or one Xiaohongshu opportunity.

Must include:

1. 一句话结论
2. 机会定义
3. 需求证据
4. 付费验证
5. 竞品强弱
6. 流量打法
7. 收入区间
8. 风险与反证
9. 推荐验证动作
10. Final decision

### Deep Research

Use when the user asks for serious investment judgment, multiple competitors, revenue estimation, or "完整调研".

Load `references/output-formats.md` and use the deep report template.

## Core Workflow

### 1. Define the Opportunity

State:

- What the product/opportunity is
- Who needs it
- In what scenario they need it
- What painful job it solves
- What users currently use instead
- Whether the need is frequent, urgent, paid, emotional, productivity-driven, compliance-driven, or entertainment-driven

### 2. Collect and Grade Evidence

Grade every signal as one of:

- Interest signal: attention only
- Demand signal: repeated need or pain
- Payment signal: money changed hands
- Retention signal: repeat purchase, subscription, renewal, or habit

Use `references/evidence-grading.md` when signal quality matters.
Use `references/research-sources.md` when choosing where to gather evidence.

### 3. Check Paid Validation

Paid behavior is the strongest validation.

Look for:

- Real purchases
- Order count and order velocity
- Pricing and margin
- Paid reviews or user feedback
- Subscription, renewal, or repeat purchase
- Store sales, marketplace traces, or service orders
- Comments that move beyond curiosity into buying intent

Classify paid validation:

- Weak: interest only, no clear purchase
- Medium: some purchase evidence or early paid feedback
- Strong: stable weekly or monthly orders
- Very Strong: large order-level signal plus repeatable traffic and acceptable margin

Use `references/paid-validation-and-xiaohongshu-framework.md` for Xiaohongshu and order-speed judgment.

### 4. Validate the Traffic Channel

Do not recommend building before naming where users come from.

Check:

- Search traffic: Baidu, Google, 5118, Google Suggest, long-tail keywords, SEO difficulty
- Social traffic: Xiaohongshu, Douyin, Bilibili, YouTube, TikTok, X, Reddit, Zhihu
- Marketplace traffic: Taobao, Xianyu, Pinduoduo, Fiverr, Upwork, app stores, plugin stores
- Private-domain traffic: WeChat, groups, newsletters, communities, repeat purchase
- Partner traffic: creators, affiliates, agents, resellers

If traffic is broad but purchase intent is weak, say so directly.

### 5. Analyze Competitors

Include direct competitors, indirect competitors, manual substitutes, platform substitutes, and informal sellers.

Judge:

- Competitor quantity
- Competitor quality
- Traffic moat
- Product moat
- Brand/trust moat
- User complaints
- Whether weak competitors are still selling
- Whether small-team 降维打击 is realistic

Use `references/competitor-analysis-rubric.md` when competitor strength is central to the decision.

### 6. Estimate Revenue Range

Estimate only with assumptions.

Common formulas:

```text
Tool site revenue = monthly visitors x paid conversion rate x ARPPU
Private-domain revenue = leads x add-WeChat rate x payment conversion x average order value
Marketplace revenue = monthly orders x unit price x gross margin
SaaS MRR = paying users x monthly price
Competitor estimate = estimated monthly visits x estimated conversion rate x ARPPU
```

Use `references/revenue-estimation-template.md` for formulas, conversion assumptions, and estimate quality levels.

### 7. Look for Risks and False Demand

Always check:

- Users only want free solutions
- Competitors look weak but have hidden traffic or private-domain assets
- Product is easy to copy
- API or delivery cost destroys margin
- Support burden is high
- Legal, copyright, compliance, or platform risk is high
- Demand is seasonal or one-time
- Users are hard to reach
- Product requires trust a new brand cannot quickly build
- The user cannot personally understand the pain
- The project does not create compounding assets

Use `references/go-no-go-checklist.md` before recommending `Go Now`.

### 8. Decide the Next Action

Map the evidence to one decision:

- `Go Now`: demand clear, payment exists, competition beatable, traffic reachable, build/delivery cost controlled.
- `Small Bet`: promising but uncertain; run a landing page, content test, manual delivery, marketplace listing, or small MVP first.
- `Observe`: interesting but evidence is not enough; keep tracking specific signals.
- `Reject`: weak demand, no payment path, poor traffic, strong moat, bad margin, high legal/platform risk, or bad strategic fit.

The recommendation must include the first verification action and what not to build yet.

## Reference Map

Load only the files needed for the request:

- `references/evidence-grading.md`: how to grade likes, comments, orders, reviews, renewal, and revenue signals.
- `references/output-formats.md`: quick, standard, and deep output templates.
- `references/research-sources.md`: where to collect China/global demand, payment, pain, and traffic evidence.
- `references/paid-validation-and-xiaohongshu-framework.md`: paid validation levels, Xiaohongshu note/order timing, and content-to-payment signal quality.
- `references/competitor-analysis-rubric.md`: competitor types, strength scoring, and beatability judgment.
- `references/revenue-estimation-template.md`: revenue formulas, assumptions, and estimate quality levels.
- `references/go-no-go-checklist.md`: final entry/avoid checklist.

## Quality Rules

- Be direct and practical.
- Avoid empty business jargon.
- Do not pretend estimates are exact.
- Show assumptions clearly.
- Compare demand and competition together.
- Distinguish broad traffic from precise traffic.
- Identify whether competitors are truly weak or only look weak.
- Include risks and negative evidence.
- Favor the smallest useful validation over building a full product.
- Prefer opportunities that create compounding assets: content, SEO pages, private-domain users, product data, templates, workflows, brand trust, or operational SOPs.

## Bad Output Pattern

Do not say:

```text
这个市场很有潜力，建议可以尝试。
```

Say:

```text
建议 Small Bet。现在有兴趣信号，但付费信号不足。先不要开发完整产品，建议用一个落地页 + 3 篇精准内容 + 人工交付测试，验证是否有人愿意付费。验证通过后再做 MVP。
```

## Final Self-Check

Before final output, check:

- Did I separate facts, assumptions, and inference?
- Did I check paid validation instead of only popularity?
- Did I name the traffic path?
- Did I include risk and negative evidence?
- Did I give revenue as a range with assumptions?
- Did I choose exactly one of `Go Now / Small Bet / Observe / Reject`?
- Did I recommend the smallest next validation action?
