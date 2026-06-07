# The Indian Union Budget Analysis — 2017 to 2027
### *A Data-Driven Policy Examination of a Decade of Fiscal Priorities*

---

> **"A government's budget is not merely an accounting document. It is a statement of values — a declaration of what the state believes matters, what it is willing to sacrifice, and what kind of future it is betting on."**

---

## 📊 Live Interactive Dashboard

**[→ Open the Dashboard](https://Debajyoty-Sen.github.io/india-budget-analysis/)**

Built with Chart.js and vanilla HTML/CSS. No installation required — runs entirely in the browser.

| | |
|---|---|
| **Data Source** | Ministry of Finance, Government of India — indiabudget.gov.in |
| **Document Type** | Ministry-wise Summary of Budget Estimates (BE) |
| **Coverage** | 57 Ministries · 10 Fiscal Years · 2017-18 to 2026-27 |
| **Total Records** | 570+ ministry-year data points |
| **Figures** | All values in ₹ crore (Budget Estimates) |

---

## 🗺️ What This Project Is

This is not a dashboard project. It is a **policy investigation** that uses data as evidence.

India's Union Budget is the single most consequential annual document produced by the Indian state. It determines how ₹53 lakh crore — roughly $640 billion — is distributed across defence, healthcare, education, infrastructure, subsidies, and dozens of other priorities. Every rupee allocated is a political and philosophical choice. Every trend, every crossover, every acceleration in the numbers reflects a worldview about how economies grow and how governments should govern.

This project collects, cleans, and analyses 10 years of ministry-level budget data to answer a deceptively simple question:

> **Where does India's money actually go — and is that changing?**

The analysis is structured around five specific investigative questions, each rooted in live debates in Indian economic policy, public administration, and development studies.

---

## ❓ The Five Questions — And Why They Matter

### Question 1 — Is the *quality* of India's spending improving?
Spending more money is not the same as spending it well. The distinction between **Revenue Expenditure** (salaries, subsidies, pensions — money that is consumed) and **Capital Expenditure** (roads, railways, hospitals — money that creates assets) is one of the most fundamental measures of a government's economic philosophy. A government that spends 90% on salaries and 10% on infrastructure is structurally different from one that spends 75% on salaries and 25% on infrastructure — even if the total budget is identical. Has India's spending quality improved over the decade?

### Question 2 — Is the advertised "Capex push" real, and is it broad-based?
Since 2020, every Union Budget speech has prominently featured the government's commitment to **capital expenditure** as an engine of growth. The claim is that government infrastructure spending will "crowd in" private investment and trigger a manufacturing revival. But rhetoric and reality can diverge. Is the Capex surge genuine? And if so, is it distributed across the government — or concentrated in two or three mega-ministries?

### Question 3 — Is India choosing infrastructure over human welfare?
This is the central tension in Indian development economics, and it has no easy answer. A rupee spent on building a highway cannot simultaneously be spent on a school. The question is whether India's budget reflects a deliberate trade-off — prioritising physical capital (roads, ports, railways) over human capital (health, education, rural development) — and whether that trade-off is widening or narrowing over time.

### Question 4 — Does the money match the government's stated ambitions?
The Indian government has, in recent years, made sweeping commitments: net-zero emissions by 2070, a $1 trillion digital economy, universal piped water access under Jal Jeevan Mission, semiconductor self-sufficiency under the PLI scheme. These are not small ambitions. The question is whether the budgetary allocations — the actual rupees — are proportional to the stated urgency. CAGR analysis of strategic sectors against the overall budget baseline reveals which commitments are real and which are rhetorical.

### Question 5 — Are India's largest ministries trapped by their own history?
Even as the macro budget shifts toward capital spending, individual ministries may be structurally unable to follow. Ministries with large workforces (Defence, Home Affairs) or massive subsidy obligations (Agriculture, Food & Public Distribution) may find that committed liabilities — pensions, salaries, fertiliser subsidies — consume so much of their budget that modernisation becomes impossible regardless of political will. Is operational bloat worsening or improving at the ministry level?

---

## 📐 Methodology

**Data Collection:** Ministry-wise Summary of Budget Estimates downloaded directly from indiabudget.gov.in for each fiscal year from 2017-18 through 2026-27. These are Budget Estimate (BE) figures — announced allocations, not revised or actual expenditures.

**Data Cleaning:** All 10 PDFs were parsed and consolidated into a single master dataset (`india_budget_master.csv`) using Python and Pandas. Ministry names were standardised across years to account for renaming and restructuring (e.g., Ministry of HRD → Ministry of Education; Ministry of Drinking Water & Sanitation + Water Resources → Ministry of Jal Shakti).

**Analytical Approach:**
- Absolute figures used for trend analysis
- Percentage share of total budget used for priority analysis (removes the effect of overall budget growth)
- CAGR calculated as: `(Final Value / Initial Value)^(1/n) - 1` over 9 years
- Revenue:Capital ratio calculated per ministry per year as a measure of spending quality
- Sector groupings: Infrastructure = Roads + Railways + Ports; Social Sector = Health + Education + Rural Development + Women & Child Development

**Limitation:** Budget Estimates represent intent, not outcome. Revised Estimates and Actuals may differ — particularly in years with economic shocks (2020-21). This analysis reads the government's stated priorities, not necessarily its achieved allocations.

---

## 📋 Finding 1 — The Quality of Spending: A Genuine Structural Shift

**The Macro Picture**

In 2017-18, India's total budget was ₹21.5 lakh crore. Of this, a staggering **85.6% was Revenue Expenditure** — salaries, interest payments, subsidies, pensions, and operational costs. Only **14.4% was Capital Expenditure** — money that creates lasting assets.

By 2026-27, with the budget having grown to ₹53.5 lakh crore, this composition has materially shifted: **Revenue Expenditure has fallen to 77.1%** of the total, while **Capital Expenditure has risen to 22.9%**. In absolute terms, Capex grew from ₹3.1 lakh crore to ₹12.2 lakh crore — a **294% increase** over the decade, significantly outpacing the 149% growth in the overall budget.

**What This Means**

This is a textbook improvement in the "quality of expenditure." The government has explicitly — and measurably — traded short-term consumption boosts for long-term asset creation. The policy logic is grounded in economics: capital spending has a higher fiscal multiplier than revenue spending, meaning each rupee spent on infrastructure generates more secondary economic activity than each rupee spent on salaries or subsidies.

This shift also has implications for India's manufacturing competitiveness. India's logistics cost as a percentage of GDP currently stands at approximately **14%** — roughly double that of advanced economies. Sustained capital investment in roads, railways, and ports is directly aimed at closing this gap and making Indian-manufactured goods price-competitive in global markets.

**The Caveat**

Improvement in the aggregate Capex share does not guarantee efficient capital allocation. As explored in Finding 2, the distribution of this Capex across ministries is highly uneven — which significantly qualifies the headline narrative.

---

## 📋 Finding 2 — The Capex Concentration Problem

**The Headline That Needs Qualification**

The government's Capex push is real. The numbers confirm it unambiguously. But the claim that this push represents a "broad-based" stimulus to private investment — the crowding-in hypothesis — requires serious qualification.

**The Finding**

Across every single year in the 10-year dataset, **just three ministries account for 64% to 72% of all government capital expenditure**: Road Transport & Highways, Railways, and Defence. In 2026-27 specifically, these three ministries alone consumed approximately **66% of the entire capital budget** — with Roads at 24.1%, Railways at 22.7%, and Defence at 18.9%.

**The Internal Shift Within Capex**

There is a notable structural change within this concentration. In the early years of the dataset (2017-18 to 2020-21), **Defence was the dominant Capex driver**, reflecting spending on military modernisation and equipment procurement. Post-2022, this changed decisively: **Road Transport and Railways overtook Defence** as the primary consumers of capital expenditure, as the government accelerated the National Infrastructure Pipeline and National Monetisation Pipeline.

**The Policy Implication**

The "crowding in" hypothesis is therefore a more targeted claim than it appears. The state is building India's **physical connectivity infrastructure** — the highway network, freight corridors, high-speed rail — betting that private manufacturers will establish supply chains and factories along these arteries. This is a coherent industrial strategy. But it means that the Capex push is concentrated in the logistics and transport sector, not distributed across healthcare infrastructure, education institutions, agricultural processing facilities, or industrial clusters. The factory still has to be built by someone else.

---

## 📋 Finding 3 — Welfare vs. Infrastructure: The Crossover

**The Framing**

For decades, the central normative debate in Indian public finance has been between two schools of thought. The first argues that direct investment in human capital — health, education, nutrition, rural safety nets — is the most reliable path to poverty reduction and inclusive growth. The second argues that infrastructure-led growth creates jobs, reduces costs, and generates multiplier effects that ultimately reach the poor more durably than direct transfers.

The budget data allows us to see which school of thought has been winning.

**The Finding**

In 2017-18, the **Social Sector** (Health, Education, Rural Development, Women & Child Development) commanded **11.2% of the total budget**. Infrastructure (Roads, Railways, Ports) commanded **6.9%**. The social sector led by over 4 percentage points.

By 2026-27, these trajectories have **completely crossed**. Infrastructure now commands **12.1%** of the budget, while the Social Sector has contracted to **8.5%**. The crossover occurred in **2022-23** — the year the government's post-COVID infrastructure acceleration went into full effect.

Critically, this is not an absolute decline in social spending. Both sectors grew significantly in rupee terms. But as a **share of the total budget** — which is the correct metric for measuring priority — infrastructure has been gaining ground steadily while social sector allocation has been gradually compressed.

**The Policy Verdict**

The data confirms a **philosophical pivot** in Indian fiscal policy. The state is explicitly prioritising physical capital formation over direct human capital transfers. Whether this bet pays off — whether infrastructure-led job creation ultimately reaches the rural poor more effectively than health and education spending — is a question the data cannot yet answer. But the direction of the wager is now unambiguous.

---

## 📋 Finding 4 — Viksit Bharat: Where the Strategic Money Is Going

**The Methodology**

To assess whether the government's stated strategic priorities are backed by actual rupees, CAGR was calculated for each key ministry over the 9-year period from 2017-18 to 2026-27. The overall budget CAGR of **10.68%** serves as the baseline — any sector growing faster than this rate is being genuinely prioritised relative to the rest of government spending.

**The Winners — Rhetoric Backed by Rupees**

| Sector | 2017-18 (₹ Cr) | 2026-27 (₹ Cr) | CAGR | vs Baseline |
|---|---|---|---|---|
| Jal Shakti | 6,887 | 94,808 | **33.8%** | +23.1pp |
| Housing & Urban Affairs | 6,406 | 85,522 | **33.3%** | +22.6pp |
| New & Renewable Energy | 5,473 | 32,915 | **22.1%** | +11.4pp |
| Electronics & IT (MeitY) | 4,039 | 21,633 | **20.4%** | +9.7pp |
| Railways | 55,000 | 2,81,377 | **19.8%** | +9.1pp |

**Jal Shakti** is the single most dramatic story in the dataset — a 33.8% CAGR representing the government's near-complete transformation of rural water infrastructure under the Jal Jeevan Mission (Har Ghar Jal). **Renewable Energy** grew at 22.1% — but the acceleration is concentrated post-2022, tracking India's COP26 Panchamrit commitments almost precisely. **Electronics & IT** at 20.4% CAGR represents genuine financial validation of the PLI schemes, semiconductor missions, and Digital India programmes.

**The Counterintuitive Finding — Space**

Despite the extraordinary public visibility of ISRO's recent missions — Chandrayaan-3's historic lunar south pole landing, the Aditya-L1 solar observatory, and the Gaganyaan human spaceflight programme — the **Department of Space grew at only 4.6% CAGR** over the decade. This is less than half the overall budget growth rate, and represents one of the largest gaps between public profile and fiscal reality in the entire dataset.

This is not neglect. It is strategy. The government has been deliberately transitioning space from a purely state-led enterprise to a **public-private model** through IN-SPACe (Indian National Space Promotion and Authorisation Centre). The intent is to use ISRO as a technology anchor while private companies like Agnikul Cosmos, Skyroot Aerospace, and Pixxel build the commercial space economy. The budget numbers reflect this architectural decision.

**The Concerning Finding — Education**

Education grew at only **6.4% CAGR** — well below the budget baseline. Given that the demographic dividend window — the period during which India's working-age population is at its peak — closes over the next two decades, underinvestment in education is the variable most likely to compromise long-run growth. The data suggests this risk is not yet being priced into fiscal priorities.

---

## 📋 Finding 5 — Operational Bloat in Legacy Ministries

**The Question Within the Question**

The macro story of rising Capex is real and important. But it raises a ministry-level question: even if the government wants to spend more on assets rather than operations, can it? Are certain ministries structurally trapped by committed liabilities — pension obligations, salary rolls, and subsidy mandates — that consume their budgets before capital spending becomes possible?

To investigate this, a **Revenue-to-Capital ratio** was calculated for each major ministry in each year. A ratio of 3:1 means ₹3 is spent on operations for every ₹1 spent on asset creation. Lower is better.

**Defence — Slow but Real Improvement**

In 2017-18, Defence spent **₹2.93 in Revenue for every ₹1 in Capital**. By 2026-27, this ratio had improved to **2.40:1** — a meaningful shift driven by sustained increases in capital outlay for military modernisation, equipment procurement, and infrastructure along border areas. This is genuine — if gradual — progress in improving the quality of defence spending.

**Home Affairs — A Worsening Crisis**

Home Affairs tells the opposite story. In 2017-18, its Revenue:Capital ratio stood at **6.34:1** — already indicating that paramilitary salaries and operational costs dominated the ministry's budget. By 2024-25, this ratio had worsened to a peak of **10.30:1**, before marginal improvement in 2025-26 and 2026-27. This means that for every ₹1 spent on police infrastructure, modernisation, and equipment, ₹10 was consumed by salaries and operational costs. Police modernisation — a stated priority in multiple government documents — is being financially strangled by committed personnel liabilities.

**Agriculture — Revenue by Design**

Agriculture's Revenue:Capital ratio is so extreme — running into the hundreds — that it requires contextual explanation rather than criticism. The ministry's budget is dominated by PM-KISAN direct income transfers, fertiliser subsidies, and Minimum Support Price operations. These are not inefficiencies — they are deliberate policy instruments. But they mean that almost no budgetary headroom exists for capital investment in cold chain infrastructure, agricultural research, or irrigation modernisation within the ministry's own allocation. What capital investment in agriculture exists is largely routed through Jal Shakti and Rural Development.

**The Systemic Implication**

The operational bloat finding reveals a structural constraint on India's Capex ambitions at the ministry level. The aggregate Capex numbers look healthy because Roads and Railways — both capital-intensive by nature — are pulling the average up. Below the headline, many legacy ministries remain deeply constrained by committed revenue liabilities, limiting their ability to participate in the modernisation story.

---

## 🔍 Conclusion — What the Numbers Tell Us

Ten years of Union Budget data, across 57 ministries and ₹420 lakh crore in cumulative expenditure, yields five conclusions that complicate both the government's narrative and its critics':

1. **The quality of spending is genuinely improving** at the macro level. The Capex-to-Revenue shift is real, sustained, and statistically significant. This is not spin.

2. **The Capex push is concentrated, not broad-based.** Three ministries dominate capital expenditure every single year. The crowding-in argument applies specifically to transport connectivity infrastructure — not to the wider economy.

3. **India has made a deliberate philosophical choice** to prioritise physical capital over human capital in its fiscal allocations. Infrastructure's share of the budget now exceeds the social sector's share for the first time in the dataset. Whether this bet pays off remains to be seen.

4. **Several strategic commitments are financially genuine** — Jal Shakti, Renewable Energy, and Digital India are backed by above-average CAGR. Education and Space are not — for different but defensible reasons.

5. **Operational bloat is a ministry-level problem** that the macro Capex narrative conceals. Home Affairs, Agriculture, and Health face structural Revenue:Capital constraints that limit their modernisation capacity regardless of political will.

The most important question the data cannot answer is also the most important question in Indian public finance: will infrastructure-led growth be inclusive enough, fast enough, to absorb the 7-10 million young Indians entering the labour market every year? The budget bets it will. The next decade will deliver the verdict.

---

## 🛠️ Technical Stack

```
Data Extraction    Python (pdfplumber, Pandas)
Data Storage       CSV (india_budget_master.csv)
Analysis           Python (Pandas, NumPy)
Visualisation      Chart.js 4.4.1
Dashboard          Vanilla HTML5 / CSS3 / JavaScript
Fonts              Playfair Display · DM Sans · DM Mono (Google Fonts)
Hosting            GitHub Pages
```

---

## 📁 Repository Structure

```
india-budget-analysis/
│
├── index.html                    # Interactive dashboard (open in browser)
├── india_budget_master.csv       # Clean master dataset — 570+ rows
├── README.md                     # This policy brief
└── extract_budget.py             # Python script used for data extraction
```

---

## 👤 About the Author

**Debajyoty Sen** — Economics & Political Science graduate (University of Calcutta, Gold Medal, 2023). Three years of structured preparation for the UPSC Civil Services Examination, covering Indian Polity, Macroeconomics, Public Policy, Ethics, and Governance across 500+ analytical essays and policy summaries.

This project sits at the intersection of those two worlds: quantitative data analysis applied to policy questions that matter.

**Skills demonstrated in this project:** Python · Pandas · Data cleaning · Exploratory data analysis · Chart.js · HTML/CSS · Policy writing · Economic interpretation · Public finance

📧 sendebajyoty@gmail.com

---

*All figures are Budget Estimates (BE) as published by the Ministry of Finance, Government of India. This analysis is independent and not affiliated with any government body or political organisation.*
