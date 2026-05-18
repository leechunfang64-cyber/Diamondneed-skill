# Diamondneed Skill：竞品需求分析与机会判断

这是一个用于 **竞品分析、需求调研、AI 产品调研、小红书选品、虚拟产品选品、SaaS 机会判断、竞品收入估算** 的 Agent Skill。

它的目标不是写漂亮报告，而是帮你判断：

```text
这个机会有没有真实需求？
有没有人已经付费？
对手强不强？
流量从哪里来？
大概能不能赚钱？
小团队能不能打？
下一步应该做什么？
```

最终必须落到一个明确决策：

```text
Go Now / Small Bet / Observe / Reject
```

## 1. 适合什么时候用？

典型问题：

```text
这个 AI 工具能不能做？
这个小红书品是不是机会？
这个关键词有没有需求？
这个竞品大概赚多少钱？
这个赛道是不是蓝海？
对手看起来很弱，我能不能降维打击？
这个产品值不值得投入时间？
```

适合分析：

```text
AI 产品
AI 工具站
小红书选品
虚拟产品
SaaS 点子
Chrome Extension
模板产品
知识付费产品
私域产品
服务产品化机会
Fiverr / Upwork 服务
SEO 工具站
内容站 / 资源站
```

## 2. 核心判断链路

```text
机会定义
→ 需求证据
→ 付费验证
→ 流量来源
→ 竞品强弱
→ 收入区间
→ 风险反证
→ Go Now / Small Bet / Observe / Reject
```

最重要的原则：

```text
不要因为点赞高就以为能赚钱。
不要因为没人做就以为是蓝海。
不要因为流量大就以为转化好。
不要因为产品能做就以为值得做。
```

## 3. 输出模式

这个 skill 现在有 3 档输出，避免所有问题都写成长报告。

### Quick Judgment

适合一句话快速判断。

包含：

```text
一句话结论
当前证据
关键判断
最大风险
最小验证动作
Final Decision
```

### Standard Report

默认模式。适合分析一个产品、一个竞品、一个关键词或一个小红书机会。

包含：

```text
一句话结论
机会定义
需求证据
付费验证
竞品强弱
流量打法
收入区间
风险与反证
推荐验证动作
Final Decision
```

### Deep Research

适合严肃下注、多竞品、收入估算或完整调研。

详细模板在：

```text
references/output-formats.md
```

## 4. 安装与使用

把整个仓库作为一个 skill 文件夹放到 Agent / 编程助手支持的 skills 目录中。

目录结构：

```text
Diamondneed-skill/
├── SKILL.md
├── README.md
├── references/
│   ├── evidence-grading.md
│   ├── output-formats.md
│   ├── research-sources.md
│   ├── paid-validation-and-xiaohongshu-framework.md
│   ├── go-no-go-checklist.md
│   ├── revenue-estimation-template.md
│   └── competitor-analysis-rubric.md
└── evals/
    └── evals.json
```

核心文件是 `SKILL.md`。真正触发 skill 的是 `SKILL.md` 里的 frontmatter `description`，不是 README。

## 5. 推荐提问模板

### 分析 AI 产品

```text
请使用 competitor-demand-research skill，帮我分析这个 AI 产品值不值得做：

产品：{产品名称或链接}
目标用户：{谁用}
解决问题：{解决什么问题}
已知竞品：{竞品链接或名称}
已知数据：{流量、价格、订单、评论、小红书笔记等}

重点判断：
1. 有没有真实需求；
2. 有没有付费验证；
3. 对手强不强；
4. 小团队能不能降维打击；
5. 大概盈利区间；
6. 最终 Go Now / Small Bet / Observe / Reject。
```

### 分析小红书选品

```text
请使用 competitor-demand-research skill，帮我分析这个小红书品能不能做：

品类：{品类名称}
相关账号：{账号名称或链接，可选}
相关笔记数据：{点赞、收藏、评论、发布时间、成交等}
评论区购买意图：{用户是否问怎么买、多少钱、链接在哪}
同行数量：{大概多少个}
同行强弱：{是否专业、是否矩阵、是否有私域}
```

### 分析关键词 / SEO 机会

```text
请使用 competitor-demand-research skill，帮我分析这个关键词有没有产品机会：

关键词：{关键词}
市场：中国 / 海外 / 都看
搜索量数据：{可选}
竞品网站：{可选}
用户意图：{可选}
```

### 估算竞品收入

```text
请使用 competitor-demand-research skill，帮我估算这个竞品大概能赚多少钱：

竞品：{名称或链接}
月访问量：{如果有 Similarweb / Semrush 数据，填这里}
定价：{价格}
订单量 / 评论数 / 用户数：{可选}
主要流量来源：{可选}
```

## 6. 参考文件说明

### `SKILL.md`

主流程文件。负责触发、任务边界、输出模式、核心流程和最终自检。

### `references/evidence-grading.md`

证据分级。用于区分：

```text
兴趣信号
需求信号
付费信号
留存信号
```

这是防止误判的核心文件。

### `references/output-formats.md`

3 档输出模板：

```text
Quick Judgment
Standard Report
Deep Research
```

### `references/research-sources.md`

调研渠道清单。用于寻找搜索需求、付费需求、痛点需求、技术突破信号。

### `references/paid-validation-and-xiaohongshu-framework.md`

小红书和付费验证判断。重点看订单速度、评论购买意图、同行弱但卖得动。

### `references/go-no-go-checklist.md`

最终下注检查表。用于避免进入伪需求、低毛利、高客服、无复利项目。

### `references/revenue-estimation-template.md`

收入估算模板。输出保守 / 中位 / 乐观区间，不输出假装精确的单一数字。

### `references/competitor-analysis-rubric.md`

竞品强弱评分。用于判断对手是否真的弱，还是只是表面粗糙。

### `evals/evals.json`

测试样例。现在覆盖 10 个关键场景，包括小红书、收入估算、无竞品误判、强竞品、法律风险、快速输出模式等。

## 7. 决策含义

### Go Now

需求清晰，已有付费验证，对手可打，流量路径清楚，MVP 能快速做，毛利健康。

### Small Bet

方向不错，但成交、流量或竞争还有不确定。先用落地页、内容、店铺页、私域人工交付或小 MVP 测试。

### Observe

方向有意思，但搜索、成交、流量或竞品信号不足。继续观察，不要投入开发。

### Reject

需求弱，没有付费信号，流量不可达，竞争过强，成本/法律/平台风险高，或者无法形成长期资产。

## 8. 最终目标

从：

```text
会做功能
```

升级到：

```text
会做让用户愿意付费的功能
```
