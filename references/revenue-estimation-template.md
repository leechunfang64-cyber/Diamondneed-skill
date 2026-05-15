# Revenue Estimation Template

Use this reference to estimate the possible revenue range of a product, AI tool, virtual product, SaaS, Xiaohongshu item, marketplace service, or content-driven opportunity.

The purpose is not to produce exact financial truth. The purpose is to create a decision-grade estimate with clear assumptions.

## 1. Core Rule

Never output one single revenue number as if it is certain.

Always output:

- Conservative estimate
- Middle estimate
- Optimistic estimate
- Key assumptions
- Biggest variables
- Reasons the estimate may be wrong

## 2. Estimate Quality Levels

### Weak Estimate

Only has rough market feeling, no traffic or order data.

Use language like:

```text
目前只能做方向性判断，不能做严肃收入估算。
```

### Medium Estimate

Has some visible evidence:

- competitor traffic
- order count
- pricing
- review count
- Xiaohongshu content performance
- keyword demand
- store sales signal

Can estimate a rough revenue range.

### Strong Estimate

Has multiple evidence sources:

- stable order velocity
- known pricing
- competitor traffic estimate
- visible paid conversion path
- repeated user feedback
- clear sales funnel
- multiple competitors with similar data

Can produce a more useful low / middle / high range.

## 3. Website / AI Tool Site Revenue

Formula:

```text
Monthly revenue = monthly visitors × paid conversion rate × ARPPU
```

Where:

- monthly visitors = estimated monthly website visits
- paid conversion rate = percentage of visitors who pay
- ARPPU = average revenue per paying user

Suggested conversion assumptions:

```text
Broad traffic: 0.1% - 0.5%
Normal intent traffic: 0.5% - 1.5%
Precise intent traffic: 1% - 3%
Very high-intent traffic: 3% - 8%
```

Example:

```text
Monthly visits: 30,000
Price: $9.9/month

Conservative: 30,000 × 0.3% × $9.9 = $891/month
Middle: 30,000 × 1% × $9.9 = $2,970/month
Optimistic: 30,000 × 3% × $9.9 = $8,910/month
```

Always check:

- Is the traffic broad or precise?
- Is the product paid or freemium?
- Is pricing monthly, yearly, credit-based, or one-time?
- Is API cost high?
- Is refund risk high?
- Is payment friction high?

## 4. SaaS Subscription Revenue

Formula:

```text
MRR = paying users × monthly price
```

Expanded formula:

```text
MRR = monthly visitors × signup rate × free-to-paid conversion rate × monthly price
```

Estimate:

- visitor to signup rate
- signup to paid conversion
- churn
- monthly price
- yearly plan adoption
- API / infrastructure cost
- support cost

Simple scenarios:

```text
Conservative: low traffic × low conversion × low price
Middle: realistic traffic × normal conversion × standard price
Optimistic: high-intent traffic × strong conversion × annual plan or higher price
```

## 5. Xiaohongshu / Private-Domain Revenue

Formula:

```text
Monthly revenue = content exposure × profile/store click rate × consultation/add-WeChat rate × payment conversion × average order value
```

Alternative formula:

```text
Monthly revenue = leads × payment conversion × average order value
```

Track:

- note views
- saves
- comments with buying intent
- profile clicks
- store clicks
- private messages
- WeChat adds
- consultations
- payments
- refunds
- repeat purchases

Suggested assumptions:

```text
Weak buying intent: 0.5% - 2% of leads pay
Normal buying intent: 2% - 8% of leads pay
Strong buying intent: 8% - 20%+ of leads pay
```

Be careful:

- Views are not leads.
- Likes are not buying intent.
- Saves are stronger than likes but still not payment.
- Comments asking “怎么买 / 多少钱 / 链接在哪” are stronger.
- Real orders are strongest.

## 6. Marketplace Revenue

Formula:

```text
Monthly revenue = monthly orders × unit price × gross margin
```

If only review count is visible, use review-to-order assumptions carefully.

Possible rough assumption:

```text
Orders may be 5x - 30x visible reviews depending on category, platform, and user behavior.
```

But never treat this as certain.

Evaluate:

- order count
- review count
- unit price
- refund rate
- platform fee
- delivery cost
- customer support cost
- repeat purchase
- whether orders are recent or accumulated over years

## 7. Service-to-Product Revenue

Use when a manual service on Fiverr, Upwork, Xiaohongshu, Xianyu, or private domain may be productized by AI.

Formula:

```text
Revenue = number of service orders × service price × gross margin
```

Productization question:

```text
Can AI reduce delivery cost while preserving enough value for the user to pay?
```

Check:

- Is the service repetitive?
- Is the output standardized?
- Can the workflow be automated?
- Is human review still needed?
- Can the final product be self-serve?
- Can the product be sold repeatedly without proportional labor?

## 8. Competitor Traffic-Based Estimate

Formula:

```text
Estimated competitor revenue = estimated monthly visits × estimated conversion rate × estimated ARPPU
```

Use traffic tools only as directional indicators:

- Similarweb
- Semrush
- Ahrefs
- AITDK
- SEO keyword rankings
- app store ranking
- Chrome extension users
- Product Hunt / AppSumo signals

Always state:

```text
该估算基于第三方流量和转化率假设，不代表竞品真实财务数据。
```

## 9. Gross Profit Estimate

Revenue is not profit.

Formula:

```text
Gross profit = revenue - variable costs
```

Variable costs may include:

- AI API cost
- image/video generation cost
- storage
- bandwidth
- payment fee
- platform commission
- refund loss
- manual delivery cost
- customer support cost
- affiliate commission

For AI tools, always check whether API cost destroys margin.

## 10. Revenue Output Format

Use this format:

```markdown
## 盈利区间估算

### 估算前提

- 流量来源：
- 月访问 / 线索 / 订单假设：
- 转化率假设：
- 客单价假设：
- 毛利假设：
- 主要成本：

### 保守估算

- 假设：
- 月收入：
- 月毛利：
- 年收入：

### 中位估算

- 假设：
- 月收入：
- 月毛利：
- 年收入：

### 乐观估算

- 假设：
- 月收入：
- 月毛利：
- 年收入：

### 估算可信度

弱 / 中 / 强

### 最大变量

- 流量是否真实可达：
- 转化率是否成立：
- 客单价是否能维持：
- 复购是否存在：
- 成本是否可控：
```

## 11. Practical Warning

A project with high revenue but high support burden may be worse than a smaller project with automatic delivery and repeat purchase.

For small teams, prioritize:

```text
healthy gross margin
low support burden
automated delivery
precise traffic
repeat purchase
compounding assets
```
