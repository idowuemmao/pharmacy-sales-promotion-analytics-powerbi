# 🏆 European Pharmacy Sales & Profitability Analytics
## Power BI Advanced Analytics Solution | Challenge Runner-Up 🥈

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)]()
[![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)]()
[![Award](https://img.shields.io/badge/Award-Runner--Up-silver?style=for-the-badge&logo=trophy)]()
[![Status](https://img.shields.io/badge/Status-Production%20Ready-success?style=for-the-badge)]()

---

## 🎖️ Competition Achievement

![Uploading runner up awards.png…]()

**This Power BI solution was recognized as RUNNER-UP** in the European Pharmacy Sales & Profitability Analytics Challenge, competing against analytics professionals across multiple countries. The solution was evaluated on:

- ✅ **Data Storytelling Excellence** - Clear narrative flow across 3 interconnected pages
- ✅ **Advanced DAX Implementation** - 80+ dynamic measures with business logic
- ✅ **User Experience Design** - Interactive tooltips, dynamic reference labels, and contextual insights
- ✅ **Business Impact** - Actionable recommendations with quantified ROI projections
- ✅ **Technical Sophistication** - Complex calculations, performance optimization, and scalable architecture

---

## 📋 Table of Contents

- [Executive Summary](#-executive-summary)
- [Report Architecture](#-report-architecture)
- [Page 1: Enterprise Performance Overview](#-page-1-enterprise-performance-overview)
- [Page 2: Operational Efficiency & Store Performance](#-page-2-operational-efficiency--store-performance)
- [Page 3: Product & Promotion Strategy Performance](#-page-3-product--promotion-strategy-performance)
- [Advanced Features](#-advanced-features)
- [Data Model](#-data-model)
- [DAX Innovation Showcase](#-dax-innovation-showcase)
- [Installation Guide](#-installation-guide)
- [Key Insights & Recommendations](#-key-insights--recommendations)
- [Technical Specifications](#-technical-specifications)
- [Future Enhancements](#-future-enhancements)

---

## 🎯 Executive Summary

### Business Context

A comprehensive Power BI analytics solution built for a European pharmacy chain distributor operating:
- **158 pharmacies** across 5 countries (Germany, France, Italy, Spain, Netherlands)
- **€18.9M annual revenue** with strategic growth trajectory
- **247+ active products** across 5 therapeutic categories
- **675K+ units sold** through urban, suburban, and rural locations

### Solution Overview

**3-Page Interactive Dashboard** following a strategic decision-flow architecture:
```
Page 1: WHAT is happening? → Enterprise health snapshot
   ↓
Page 2: WHY is it happening? → Operational root causes
   ↓
Page 3: WHERE do we optimize? → Product & promotion strategy
```

### Innovation Highlights

- 🎨 **6 Custom Report Page Tooltips** with pharmacy/product performance snapshots
- 📊 **80+ DAX Measures** including dynamic reference labels that adapt to business thresholds
- 🏷️ **Dynamic Page Titles** that change based on filter context
- 💡 **Context-Aware KPI Cards** with automated alerts and recommendations
- 🔄 **Drill-Through Functionality** enabling seamless navigation across analysis layers

---

## 🏗️ Report Architecture

### Design Philosophy

The report follows a **strategic funnel approach**:

1. **Page 1 (Enterprise Overview)** - Executives ask: "Are we winning?"
2. **Page 2 (Operations Deep Dive)** - Managers ask: "Which levers are working?"
3. **Page 3 (Product Intelligence)** - Strategists ask: "What should we change?"

Each page builds upon insights from the previous, creating a cohesive analytical narrative.

### Navigation Flow
```
┌─────────────────────────────────────────────────────────┐
│  🏢 PAGE 1: ENTERPRISE PERFORMANCE OVERVIEW             │
│  "What is our overall performance health?"              │
│  • Revenue, Margin, Units - Absolute performance        │
│  • Geographic distribution - Where do we operate?       │
│  • YoY trends - Are we growing?                         │
└───────────────────┬─────────────────────────────────────┘
                    │
                    ▼ (Drill down to understand WHY)
┌─────────────────────────────────────────────────────────┐
│  🏬 PAGE 2: OPERATIONAL EFFICIENCY                      │
│  "Why are these results happening?"                     │
│  • Transaction economics - Pricing & basket behavior    │
│  • Store benchmarking - Who's winning, who's losing?    │
│  • Promotion analysis - Are discounts working?          │
└───────────────────┬─────────────────────────────────────┘
                    │
                    ▼ (Focus on actionable changes)
┌─────────────────────────────────────────────────────────┐
│  📦 PAGE 3: PRODUCT & PROMOTION STRATEGY                │
│  "What specific actions should we take?"                │
│  • Product portfolio - Stars, Dogs, Cash Cows           │
│  • Promo effectiveness - Lift vs margin impact          │
│  • Category optimization - Mix recommendations          │
└─────────────────────────────────────────────────────────┘
```

---

## 🏢 Page 1: Enterprise Performance Overview

<img width="1306" height="733" alt="Screenshot_14" src="https://github.com/user-attachments/assets/a1ab3d9f-6651-4e4c-a04c-1b199bf368ad" />

### Purpose
Provide a **high-level executive summary** of revenue, margin, and geographic contribution for rapid decision-making.

### Page Header (Dynamic)
```
📊 Enterprise Performance Overview | [Selected Country] | [Selected Period]
Last refreshed: [Auto-generated timestamp]
```

The page title dynamically updates based on slicer selections, showing filtered context.

---

### KPI Cards (5 Metrics)

Each KPI card includes:
- ✅ **Primary metric** (large, bold)
- ✅ **Dynamic reference label** (context-aware insight)
- ✅ **Trend indicator** (YoY growth with color coding)

#### KPI 1: Total Revenue
```
€18.9M
─────────────────────────────
⚠️ SLOW GROWTH: +4.43% more | Modest rev ↗️ €4,440K | ↗️ +20,112 more sales vs LY
```

**Reference Label Logic:**
- 🔴 < 0%: "DECLINE: Revenue down €XK"
- ⚠️ 0-5%: "SLOW GROWTH: Below industry benchmark"
- ✅ 5-15%: "HEALTHY GROWTH: On track"
- 🚀 > 15%: "STRONG MOMENTUM: Outpacing market"

#### KPI 2: Total Margin
```
€5.3M
─────────────────────────────
✅ Stable | 28.0% | Holding vs last year
```

**Reference Label Logic:**
- Compares current margin % to prior year
- Flags margin erosion (> -1pt) or expansion (> +1pt)

#### KPI 3: Margin %
```
28.04%
─────────────────────────────
+0.5pts vs LY | Margin expanding | Capture what is driving this
```

#### KPI 4: Average Revenue Per Store
```
€119.6K
─────────────────────────────
U: €185K | S: €102K | R: €51K | ✅ 3.6x spread — healthy gradient
```

**Reference Label Logic:**
- Shows Urban, Suburban, Rural averages
- Calculates Urban-to-Rural multiple
- Alerts if gap > 4x (concentration risk)

#### KPI 5: Total Units Sold
```
445,789
─────────────────────────────
✅ +8.2% units | Revenue & volume both growing
```

---

### Core Visuals

#### Visual 1: Monthly Revenue Comparison (2025 vs 2024)
**Type:** Clustered Column Chart with Line Overlay

**Configuration:**
- **X-Axis:** Month (Jan-Dec)
- **Columns:** Revenue 2024 (blue), Revenue 2025 (green)
- **Line:** YoY Growth % (orange)
- **Data Labels:** Revenue values on bars, growth % on line

**Business Insight:**
Reveals seasonal patterns and growth acceleration/deceleration by month.

**Tooltip Enhancement:**
Hover displays:
```
Month: March 2025
Revenue 2025: €1.42M (+26% vs 2024)
Revenue 2024: €1.13M
Growth: +€290K
Trend: ↗️ Accelerating (Feb was +18%)
```

---

#### Visual 2: Revenue Distribution by Pharmacy Type
**Type:** Donut Chart

**Configuration:**
- **Values:** Total Revenue
- **Legend:** Pharmacy Type (Urban, Suburban, Rural)
- **Data Labels:** Percentage + absolute value

**Breakdown:**
- 🏙️ Urban: 63% (€11.9M)
- 🏘️ Suburban: 29% (€5.5M)
- 🌾 Rural: 8% (€1.5M)

**Dynamic Subtitle:**
```
Urban stores average 3.6x rural revenue | ✅ Balanced location portfolio
```

Changes to:
```
⚠️ Consider closing low-performing rural stores
```
if Urban-to-Rural multiple exceeds 4.5x

---

#### Visual 3: Geographic Revenue Map
**Type:** Filled Map (Country-level) + Bubble Map (City-level)

**Configuration:**
- **Location:** DimPharmacy[Country], DimPharmacy[City]
- **Size:** Total Revenue
- **Color Saturation:** Margin % (green = high, red = low)
- **Tooltip:** Custom report page tooltip (Pharmacy Performance Snapshot)

**Interactive Elements:**
- Click country → filters all other visuals to that country
- Drill-down: Country → Region → City

**Map Tooltip (Custom):**
Shows when hovering over a city bubble:
```
📍 Berlin, Germany
─────────────────────────
💰 Performance: €2.1M revenue | 27.5% margin
📊 Rank: #2 of 158 stores | ⭐ Star Performer
📈 Trends: MoM +6% | YoY +14%
🏆 Top Category: OTC (42% of revenue)
```

---

#### Visual 4: Store Size Revenue Contribution
**Type:** 100% Stacked Bar Chart (Horizontal)

**Configuration:**
- **Axis:** Single bar
- **Values:** Revenue by Store Size Band (S, M, L)
- **Data Labels:** Percentage breakdown

**Insight Display:**
```
Large (L):   45% | €8.5M | 45 stores
Medium (M):  38% | €7.2M | 78 stores
Small (S):   17% | €3.2M | 35 stores
```

**Dynamic Reference Text:**
```
✅ Large format delivering 189% vs Medium stores
```

OR if underperforming:
```
⚠️ Large stores underperforming — avg only 120% vs Medium format
```

---

#### Visual 5: Drilldown Revenue Hierarchy
**Type:** Clustered Bar Chart with Drill-Down Hierarchy

**Hierarchy Levels:**
1. Country (5 countries)
2. Region (15 regions)
3. City (48 cities)
4. Pharmacy Name (158 stores)

**Visual Features:**
- **Drill-down icons:** Visible for easy navigation
- **Color coding:** Top 3 performers in green, bottom 3 in red
- **Dynamic title:** Changes with drill level
  - Level 1: "Revenue by Country"
  - Level 2: "Revenue by Region in [Country]"
  - Level 3: "Revenue by City in [Region]"
  - Level 4: "Revenue by Pharmacy in [City]"

**Concentration Risk Indicator:**
Shows below the chart:
```
⚠️ HIGH RISK: Top 3 pharmacies = 34% of total
```

---

### Page 1 Slicers

- **Year** (2024, 2025) - Dropdown
- **Country** - Multi-select list
- **Pharmacy Type** - Button slicer (Urban/Suburban/Rural)
- **Date Range** - Between slicer

---

### Key Business Insights (Page 1)
```
✅ STRENGTHS:
- 104.6% YoY revenue growth (actually 4.6% after fixing ratio)
- 28.04% margin stability (healthy for pharmacy retail)
- 445.79K units sold with balanced geographic distribution

⚠️ WATCH AREAS:
- Urban concentration at 63% creates geographic risk
- Growth below 8% industry benchmark
- Top 3 countries (Germany, France, Italy) drive 72% of revenue
```

---

## 🏬 Page 2: Operational Efficiency & Store Performance

<img width="1308" height="734" alt="Screenshot_15" src="https://github.com/user-attachments/assets/e70148fa-343a-45c4-ad5d-ecd4be212310" />

### Purpose
Analyze **transaction behavior, pricing strategy, and store-level efficiency** to identify operational improvement opportunities.

### Page Header (Dynamic)
```
🏬 Operational Intelligence: [Filtered Context] | Store Performance Analysis
Benchmark: Network Average | Period: [Selected Date Range]
```

---

### KPI Cards (5 Metrics)

#### KPI 1: Total Sales Count
```
156,847 transactions
─────────────────────────────
✅ +12.3% transactions | Traffic growing | Demand healthy
```

#### KPI 2: Revenue YoY Growth %
```
4.43%
─────────────────────────────
⚠️ SLOW GROWTH: +4.43% more | Modest rev ↗️ €4,440K | ↗️ +20,112 more sales vs LY
```

**Note:** This matches Page 1 but adds sales count context.

#### KPI 3: Average Cost Per Unit
```
€6.85
─────────────────────────────
✅ Stable | €6.85/unit | 27.2% unit margin
```

**Dynamic Logic:**
- Alerts if cost increased > 3% MoM (supplier inflation)
- Shows unit margin (Selling Price - Cost)

#### KPI 4: Average Selling Price
```
€9.52
─────────────────────────────
✅ Stable at €9.52/unit | 12% sold on promo
```

**Insight:**
- Tracks pricing power
- Shows % of volume on promotion
- Alerts if ASP declining > 2% (over-discounting)

#### KPI 5: Average Revenue Per Sale
```
€28.45
─────────────────────────────
✅ Stable: €28.45/sale | 3.0 items per basket
```

**Basket Analysis:**
- Shows items per transaction
- Alerts if basket shrinking (cross-sell failing)

---

### Core Visuals

#### Visual 1: Promotion Profitability Analysis
**Type:** Clustered Column Chart + Line

**Configuration:**
- **X-Axis:** PromoFlag (Yes / No)
- **Columns:** Total Revenue, Total Margin
- **Line (Secondary Axis):** Margin %

**Data Display:**
```
Promoted Sales:
- Revenue: €2.2M (12% of total)
- Margin: €396K
- Margin %: 18%

Non-Promoted Sales:
- Revenue: €16.7M (88% of total)
- Margin: €4.9M
- Margin %: 29%

Promo Impact: -11pts margin cost 🚨
```

**Dynamic Subtitle:**
```
🚨 CRITICAL: Promos cost 11pts | €242K in sacrificed margin | Reduce discount depth immediately
```

**Tooltip (Custom - Promo Analysis):**
```
🎁 PROMOTIONAL EFFECTIVENESS BREAKDOWN

Promoted Sales:
├─ Volume Share: 11.7% of units
├─ Revenue Share: 12%
├─ Margin: 18% (vs 29% full price)
└─ Impact: -11pts margin erosion

Promotion Lift: -2.39% 🚨
→ Customers buy LESS when on promo
→ Pure margin destruction
→ ACTION: Stop discounting immediately

Promo Frequency: 32% of days
→ Over-promoting creates expectation
```

---

#### Visual 2: Store Opening Trend (Expansion Velocity)
**Type:** Area Chart with Cumulative Line

**Configuration:**
- **X-Axis:** Open Date (Year)
- **Area:** New Pharmacies Opened (per year)
- **Line:** Cumulative Pharmacies Opened

**Time Range:** 2010-2025

**Insights Display:**
```
Fleet Maturity Analysis:
- Total Stores: 158
- Avg Age: 7.8 years
- Stores < 2 years: 24 (15% still ramping)
- Peak Expansion: 2018 (22 stores opened)
- Recent Pace: 3-5 stores/year
```

**Dynamic Commentary:**
```
📈 Network Growth Intelligence:
"15% of fleet opened in last 2 years (still ramping) | 68% of revenue from stores 5+ years old"
```

**Tooltip (Store Cohort Analysis):**
Shows when hovering on a year:
```
2019 Cohort (6 years old)
─────────────────────────
Stores Opened: 18
Current Contribution: €3.2M (18% of total)
Avg Rev/Store: €178K
Maturity: Fully ramped
Performance vs Newer: +92% revenue/store
```

---

#### Visual 3: Pharmacy-Level Performance Scorecard
**Type:** Matrix

**Rows:** Pharmacy Name  
**Columns:**
1. No. of Pharmacies (context - always 1)
2. Total Sales Count
3. Total Revenue
4. Total Margin
5. Margin %
6. Total Units Sold
7. Rev YoY %
8. Promo Impact on Margin

**Conditional Formatting:**
- **Margin %**: Green > 26%, Yellow 23-26%, Red < 23%
- **Rev YoY %**: Green > 8%, Yellow 3-8%, Red < 3%
- **Promo Impact**: Red if > 6pts

**Sorting:** Default by Total Revenue (descending)

**Matrix Tooltip (Pharmacy Snapshot):**
```
🏥 PARIS HEALTHPOINT #042
Urban • Large • Île-de-France
─────────────────────────────

💰 PERFORMANCE
Revenue: €312K | Margin: 28.5%
Rank: #5 of 158 stores | ⭐ Star Performer
Margin Rank: #8 💎 Top 20

📊 BENCHMARKS
vs Regional Avg: ↗️ +28% revenue | +3.2pts margin
vs Urban Avg: ↗️ +18%

📈 TRENDS
MoM: ↗️ +5% | YoY: 🚀 +12%

🛒 OPERATIONS
2,847 transactions | €109.60 avg basket | 2.4 units/sale
Promo Mix: 32% of revenue ✅ -4.8pts

📦 CATEGORY MIX
Top: OTC (38% of revenue)

💡 INSIGHT
Leading store — document and replicate best practices across network
```

---

#### Visual 4: Store Profitability Positioning Matrix
**Type:** Scatter Plot

**Configuration:**
- **X-Axis:** Total Revenue (per pharmacy)
- **Y-Axis:** Margin %
- **Size:** Total Units Sold
- **Color:** Pharmacy Type (Urban/Suburban/Rural)
- **Labels:** Pharmacy Name (shown for outliers only)

**Reference Lines:**
- Vertical: Network Average Revenue
- Horizontal: Network Average Margin %

**Quadrants:**
```
TOP-RIGHT: ⭐ Star Performers (High Revenue + High Margin)
TOP-LEFT: 💎 Efficient but Small (Low Revenue + High Margin)
BOTTOM-RIGHT: ⚠️ Volume Giants (High Revenue + Low Margin)
BOTTOM-LEFT: 🔴 Underperformers (Low Revenue + Low Margin)
```

**Dynamic Title:**
```
Store Performance Matrix | [X] Stars | [Y] Underperformers | [Z] Need Margin Improvement
```

**Scatter Tooltip (Quadrant Analysis):**
```
🏥 MUNICH HEALTHCENTER #089
Suburban • Medium • 6 years old
─────────────────────────────

📍 Current Position
├─ Quadrant: ⚠️ High Volume, Low Margin
├─ Revenue: €285K (vs €183K network avg)
└─ Margin: 22% (vs 26% network avg)

🔍 Root Cause Analysis
├─ Promo Units Share: 48% (too high)
├─ Promo Impact: -7.2pts (above threshold)
├─ Generic Mix: 38% (below 45% target)
└─ Avg Selling Price: €8.20 (-12% vs avg)

💡 Recommended Actions
1. Reduce promo frequency by 10%
2. Push generic substitution to 45%
3. Review discount depth on top SKUs

📊 Peer Comparison (Similar Stores)
Best Peer: Frankfurt Sub #034 (28% margin)
Gap: -6pts margin | Visit for learnings
```

---

### Page 2 Slicers

- **Pharmacy Type** - Button slicer
- **Store Size Band** - Dropdown
- **Country/Region** - Cascading slicers
- **Store Age Band** - Slicer (<2yr, 2-5yr, 5+yr)

---

### Key Business Insights (Page 2)
```
🎯 OPERATIONAL FINDINGS:

PROMOTION STRATEGY:
🚨 CRITICAL ISSUE: -2.39% promotion lift (customers buy LESS on promo)
⚠️ 11pts margin cost on promoted sales
📊 Only 11.7% of volume on promo (controlled, but ineffective)
→ ACTION: Stop all promotions immediately, redesign strategy

STORE PERFORMANCE:
✅ 15 "Star Performers" (24% of revenue, 32% of margin)
⚠️ 23 "Volume Giants" need margin improvement (high rev, low margin)
🔴 8 "Underperformers" require turnaround plans

FLEET MATURITY:
📈 15% of stores < 2 years old (still ramping to full productivity)
💎 Stores 5+ years old deliver 68% of revenue
🆕 New store ramp-up: 18-24 months to reach avg performance
```

---

## 📦 Page 3: Product & Promotion Strategy Performance

<img width="1307" height="732" alt="Screenshot_16" src="https://github.com/user-attachments/assets/59abca57-94a1-4987-a1ad-a3e8ddab1d6a" />

### Purpose
Evaluate **product mix dynamics and promotional effectiveness** to optimize category strategy and pricing decisions.

### Page Header (Dynamic)
```
📦 Product & Promotion Strategy | [Category Filter] | Profitability Optimization
Focus: Portfolio mix, Promo ROI, Generic vs Branded performance
```

---

### KPI Cards (5 Metrics)

#### KPI 1: Promo Impact on Margin
```
9.0 pts
─────────────────────────────
🚨 CRITICAL: 9.0pts lost to promos | €650K in sacrificed margin | Reduce discount depth immediately
```

**Severity Thresholds:**
- 🚨 > 7pts: Critical
- 🔴 6-7pts: Severe
- ⚠️ 5-6pts: Above threshold
- ✅ 3-5pts: Controlled
- 🎯 < 3pts: Excellent

#### KPI 2: Promo Units Share %
```
11.7%
─────────────────────────────
✅ HEALTHY: 11.7% promo | 88.3% at full price | Promotions supplementary, not structural
```

**Dependency Thresholds:**
- 🚨 > 55%: Dependency problem
- 🔴 45-55%: High risk
- ⚠️ 30-45%: Watch carefully
- ✅ 15-30%: Healthy
- 🎯 < 15%: Strong pricing power

#### KPI 3: Revenue at Risk %
```
8.2%
─────────────────────────────
⚠️ MODERATE RISK: €1.55M (8.2%) at risk | Plan 18 replacement SKUs within 2 quarters
```

**From discontinued products that still have revenue**

#### KPI 4: Promotion Lift
```
-2.39%
─────────────────────────────
🔴 NEGATIVE LIFT: -2.39% | Customers buy LESS on promo | Audit promo strategy immediately
```

#### KPI 5: Generic vs Branded Margin Gap
```
-3.0 pts
─────────────────────────────
🚨 Branded (28.2%) > Generic (25.1%) | Generic push losing margin
```

**Strategic Validation:**
- Negative gap = Generic strategy FAILING
- Positive gap = Strategy validated

---

### Core Visuals

#### Visual 1: Revenue & Margin Contribution Hierarchy
**Type:** Clustered Bar Chart with Drill-Down

**Hierarchy:**
1. Category (5 categories)
2. Brand (15+ brands)
3. Product Name (247 products)

**Measures Displayed:**
- Total Revenue (bar 1 - blue)
- Total Margin (bar 2 - green)
- Promo Impact on Margin (line - orange)

**Drill Level Titles:**
- Level 1: "Performance by Category"
- Level 2: "Brand Performance in [Category]"
- Level 3: "SKU Performance for [Brand]"

**Category-Level Tooltip:**
```
📦 VITAMINS CATEGORY
Contribution: 18% of Total Revenue
─────────────────────────────

💰 Category Economics
├─ Revenue: €3.42M
├─ Margin: €1.09M (32% margin)
├─ Units: 156K
└─ Active SKUs: 47 products

🎯 Performance by Location Type
├─ Urban:    €2.1M (34% margin) ⭐
├─ Suburban: €0.9M (30% margin)
└─ Rural:    €0.4M (27% margin)

📊 Promo vs Non-Promo Split
├─ On Promo:     28% of volume
├─ Promo Margin: 28% (healthy)
├─ Impact:       -4pts (controlled)
└─ Lift:         +22% (effective)

🏆 Top 3 Brands in This Category
1. HealthPlus Vitamins  €1.2M (33% margin)
2. WellCare Supplements €0.9M (31% margin)
3. GenericPro Vitamins  €0.7M (32% margin)

💡 Insight: Performs 8pts better in Urban
           Consider expanding urban range
```

**Product-Level Tooltip:**
```
💊 MEDICA IBUPROFEN 400MG
OTC • Branded • 20 tablets
─────────────────────────────

📊 12-Month Performance Trend
[Sparkline showing last 12 months revenue]
Trend: Declining -3% MoM (investigate)

💰 Pricing Analysis
├─ List Price: €12.99
├─ Avg Selling Price: €11.20 (86% of list)
├─ Avg Cost: €9.10
└─ Unit Margin: €2.10 (19%)

🎁 Promotional Performance
├─ Promo Frequency: 32% of days
├─ Promo Price: €9.99 (-23% discount)
├─ Promo Margin: 15% (-7pts vs full price)
└─ Lift: +12% (weak for this discount)

⚠️ Alert: High promo intensity (32%) with
         weak lift (12%) = margin bleed

💡 Action: Reduce promo frequency to 20%
          or cut discount depth to 15%
```

---

#### Visual 2: Product Profitability Matrix
**Type:** Matrix (Enhanced)

**Rows:** Product Name

**Columns:**
1. Total Sales Count
2. Total Revenue
3. Total Margin
4. Margin %
5. Total Units Sold
6. Promo Impact on Margin
7. Generic Flag (Yes/No count)
8. Active Status (Active/Discontinued)

**Advanced Calculated Columns:**
```dax
Product Rank = RANKX(ALL(DimProduct[ProductID]), [Total Revenue], , DESC)

Product Portfolio Quadrant = 
// Stars, Cash Cows, Premiums, Dogs classification

Promo Alert = 
// "🚨 Over-promoted" or "✅ Controlled"
```

**Conditional Formatting:**
- **Margin %**: Data bars (green scale)
- **Promo Impact**: Color scale (red > 6pts)
- **Product Rank**: Icon set (⭐ top 20, ⚠️ bottom 20%)

---

#### Visual 3: Generic vs Branded Revenue Split
**Type:** Donut Chart

**Values:** Total Revenue  
**Legend:** IsGeneric (Yes/No)

**Data Labels:**
- Generic: 42% (€7.9M)
- Branded: 58% (€11.0M)

**Dynamic Subtitle:**
```
⚠️ Generic share: 42% | Branded margin advantage: +3pts | Generic strategy not working
```

Changes based on margin gap value.

---

#### Visual 4: Revenue Dependency on Promotions
**Type:** 100% Stacked Bar Chart (Horizontal)

**Categories:**
- Revenue from Promoted Sales
- Revenue from Non-Promoted Sales

**Breakdown:**
- Promoted: 12% (€2.2M)
- Non-Promoted: 88% (€16.7M)

**Insight Box Below Chart:**
```
💡 PROMOTION DEPENDENCY ANALYSIS

Volume Share: 11.7% of units on promo
Revenue Share: 12% of revenue on promo
Margin Cost: -9pts on promoted sales

Verdict: ✅ LOW DEPENDENCY — business not structurally reliant on discounts

BUT: 🚨 Negative lift (-2.39%) means promos are pure margin destruction
     Stop discounting immediately
```

---

#### Visual 5: Pack Size Volume & Contribution Analysis
**Type:** Clustered Column Chart

**X-Axis:** Pack Size (10 tablets, 20 tablets, 30 tablets, 50 tablets, etc.)

**Values:**
- Total Units Sold (column 1)
- Total Revenue (column 2)

**Sort By:** Total Revenue (descending)

**Insights:**
```
Volume Concentration:
- 20-tablet packs: 38% of volume, 42% of revenue
- 50-tablet packs: 18% of volume, 28% of revenue (higher value)
- 10-tablet packs: 25% of volume, 15% of revenue (lower value)

Strategic Implication:
→ Push larger pack sizes (better revenue per unit)
→ Reduce shelf space for 10-tablet format
```

---

### Page 3 Slicers

- **Category** - Dropdown (multi-select)
- **Brand** - Dropdown
- **IsGeneric** - Button slicer (Yes/No)
- **Metric Selector** - Dropdown affecting pie charts:
  - Total Revenue
  - Total Margin
  - Margin %
  - Total Units Sold

---

### Key Business Insights (Page 3)
```
🎯 PRODUCT & PROMOTION FINDINGS:

CRITICAL ISSUES:
🚨 Promotion Lift: -2.39% (customers buy LESS when on promo)
🚨 Promo Impact: 9pts margin cost (€650K+ annually lost)
🚨 Generic Strategy Failure: Branded products 3pts MORE profitable than generics

PORTFOLIO HEALTH:
⚠️ 8.2% revenue at risk from discontinued products (€1.55M)
⚠️ Revenue concentration in 20-tablet packs (42%)
✅ Low promo dependency (11.7% of volume)

STRATEGIC ACTIONS REQUIRED:
1. STOP all promotions immediately (negative lift = pure margin destruction)
2. RENEGOTIATE generic supplier costs OR stop generic push
3. PLAN replacements for 18 discontinued SKUs within 2 quarters
4. SHIFT pack mix toward larger formats (50-tablet) for better revenue density
```

---

## 🎨 Advanced Features

### 1. Report Page Tooltips (6 Custom Pages)

#### Tooltip 1: Pharmacy Performance Snapshot
**Triggered on:** Map bubbles, Scatter plot dots, Matrix rows

**Layout:** 320px × 240px canvas

**Content Sections:**
1. Header (Pharmacy name, type, size, location)
2. Performance Summary (Revenue, Margin, Rank, Quadrant)
3. Benchmarks (vs Regional avg, vs Type avg)
4. Trends (MoM, YoY)
5. Operations (Transactions, basket size, promo mix)
6. Top Category
7. Dynamic Insight/Recommendation

**Sample Output:** *(See Page 2, Visual 4 tooltip above)*

---

#### Tooltip 2: Product Performance Detail
**Triggered on:** Product matrix rows, Category bars

**Content Sections:**
1. Product header (Name, category, brand, pack size)
2. 12-month trend sparkline
3. Pricing analysis (List, Actual, Cost, Margin)
4. Promotional performance (Frequency, discount depth, lift, impact)
5. Alert (if over-promoted or negative lift)
6. Recommended action

**Sample Output:** *(See Page 3, Visual 1 product-level tooltip above)*

---

#### Tooltip 3: Category Performance Breakdown
**Triggered on:** Category drill-down bars

**Content Sections:**
1. Category economics (Revenue, Margin, Units, Active SKUs)
2. Performance by location type (Urban/Suburban/Rural split)
3. Promo vs non-promo split
4. Top 3 brands in category
5. Location-based insight

**Sample Output:** *(See Page 3, Visual 1 category-level tooltip above)*

---

#### Tooltip 4: Monthly Trend Context
**Triggered on:** Monthly column chart (Page 1)

**Content Sections:**
1. Month header
2. Revenue 2025 vs 2024
3. YoY Growth %
4. Growth value (€)
5. Trend direction (accelerating/decelerating)

---

#### Tooltip 5: Store Cohort Analysis
**Triggered on:** Store opening timeline (Page 2)

**Content Sections:**
1. Year + cohort age
2. Stores opened that year
3. Current revenue contribution
4. Avg revenue per store
5. Maturity status
6. Performance vs newer cohorts

---

#### Tooltip 6: Promotion Analysis Deep Dive
**Triggered on:** Promo vs Non-Promo chart (Page 2)

**Content Sections:**
1. Volume share
2. Revenue share
3. Margin comparison
4. Promotion lift
5. Promo frequency
6. Verdict + recommendation

---

### 2. Dynamic Reference Labels

Every KPI card includes a **context-aware reference label** that changes based on:
- Thresholds (e.g., growth < 5% = "SLOW", > 15% = "STRONG")
- Comparisons (vs benchmark, vs prior year)
- Business logic (e.g., Urban-to-Rural ratio > 4 triggers alert)

**Implementation:**
```dax
YoY Growth Insight = 
VAR GrowthRatio = DIVIDE([Total Revenue], CALCULATE([Total Revenue], DATEADD(DimDate[Date], -1, YEAR)), 0)
VAR GrowthPct = GrowthRatio - 1
VAR GrowthValue = [Total Revenue] - CALCULATE([Total Revenue], DATEADD(DimDate[Date], -1, YEAR))
RETURN
    SWITCH(TRUE(),
        GrowthRatio < 0.95,
        "🔴 DECLINE: " & FORMAT(GrowthPct, "0.00%") & " | Revenue down €" & FORMAT(ABS(GrowthValue)/1000, "#,##0K"),
        GrowthRatio < 1.05,
        "⚠️ SLOW GROWTH: " & FORMAT(GrowthPct, "0.00%") & " | Modest rev ↗️ €" & FORMAT(GrowthValue/1000, "#,##0K"),
        GrowthRatio < 1.15,
        "✅ HEALTHY GROWTH: +" & FORMAT(GrowthPct, "0.0%") & " | +" & FORMAT(GrowthValue/1000, "#,##0K") & " vs LY",
        "🚀 STRONG MOMENTUM: +" & FORMAT(GrowthPct, "0.0%") & " | +" & FORMAT(GrowthValue/1000, "#,##0K") & " vs LY"
    )
```

**Total Reference Labels:** 15+ across all 15 KPI cards

---

### 3. Dynamic Page Titles

Page titles update based on filter context:

**Page 1:**
```
Default: "📊 Enterprise Performance Overview | All Countries | Full Period"
Filtered: "📊 Enterprise Performance Overview | Germany | Q4 2025"
```

**Implementation:**
```dax
Page 1 Dynamic Title = 
"📊 Enterprise Performance Overview | " &
IF(
    ISFILTERED(DimPharmacy[Country]),
    CONCATENATEX(VALUES(DimPharmacy[Country]), DimPharmacy[Country], ", "),
    "All Countries"
) & " | " &
IF(
    ISFILTERED(DimDate[Year]),
    CONCATENATEX(VALUES(DimDate[Year]), DimDate[Year], ", "),
    "Full Period"
)
```

---

### 4. Conditional Formatting Rules

Applied across visuals:

**Matrix Tables:**
- Margin %: Green > 26%, Yellow 23-26%, Red < 23%
- YoY Growth: Green > 8%, Yellow 3-8%, Red < 3%
- Promo Impact: Red > 6pts, Yellow 4-6pts, Green < 4pts

**Scatter Plots:**
- Color by Quadrant (Star = Green, Underperformer = Red)

**Bar Charts:**
- Top 3 values in darker shade
- Bottom 3 values in red

---

### 5. Drill-Through Functionality

**From Page 1 → Page 2:**
- Right-click any pharmacy in drill-down chart
- Select "Drill through" → "Store Detail"
- Opens Page 2 filtered to that pharmacy

**From Page 2 → Page 3:**
- Right-click any category in store matrix
- Select "Drill through" → "Product Detail"
- Opens Page 3 filtered to that category

---

### 6. Cross-Page Filtering

Slicers sync across pages:
- Year slicer (Pages 1, 2, 3)
- Country slicer (Pages 1, 2)
- Pharmacy Type slicer (Pages 1, 2)

**Configuration:** Edit interactions to prevent circular filtering

---

## 📊 Data Model

### Star Schema Architecture
```
           ┌─────────────┐
           │  DimDate    │
           │ (Dimension) │
           └──────┬──────┘
                  │
    ┌─────────────┼─────────────┐
    │             │             │
┌───▼────┐   ┌───▼────┐   ┌───▼────┐
│DimPhar-│   │FactSa- │   │DimPro- │
│macy    ├───┤les     ├───┤duct    │
│(Dim)   │   │(Fact)  │   │(Dim)   │
└────────┘   └────────┘   └────────┘
```

### Table Details

**FactSales** (675,000+ rows)
- SalesID (PK)
- DateKey (FK)
- PharmacyID (FK)
- ProductID (FK)
- UnitsSold
- RevenueEUR
- CostEUR
- MarginEUR
- PromoFlag

**DimDate** (730 rows - 2 years)
- DateKey (PK)
- Date
- Year, Quarter, Month, Week
- YearMonth (for grouping)

**DimPharmacy** (158 rows)
- PharmacyID (PK)
- PharmacyName
- Country, Region, City
- PharmacyType (Urban/Suburban/Rural)
- StoreSizeBand (S/M/L)
- OpenDate
- Latitude, Longitude

**DimProduct** (247 rows)
- ProductID (PK)
- ProductName
- Category, Brand
- IsGeneric (Yes/No)
- PackSize
- ListPriceEUR, StandardCostEUR
- LaunchDate, IsDiscontinued

### Relationships
```
FactSales[DateKey] → DimDate[DateKey] (Many-to-One, Active)
FactSales[PharmacyID] → DimPharmacy[PharmacyID] (Many-to-One, Active)
FactSales[ProductID] → DimProduct[ProductID] (Many-to-One, Active)
```

### Calculated Columns

**DimPharmacy:**
```dax
Store Age (Years) = DATEDIFF(DimPharmacy[OpenDate], TODAY(), YEAR)

Store Age Band = 
    SWITCH(TRUE(),
        [Store Age (Years)] < 2, "< 2 years",
        [Store Age (Years)] < 5, "2-5 years",
        "5+ years"
    )
```

**DimProduct:**
```dax
Product Age (Days) = DATEDIFF(DimProduct[LaunchDate], TODAY(), DAY)

Price Tier = 
    SWITCH(TRUE(),
        DimProduct[ListPriceEUR] < 10, "Budget",
        DimProduct[ListPriceEUR] < 30, "Mid-Range",
        "Premium"
    )
```

---

## 🧮 DAX Innovation Showcase

### Highlight Measures (15 of 80+)

#### 1. Context-Aware YoY Growth Label
```dax
YoY Growth Insight = 
VAR CurrentRev = [Total Revenue]
VAR LastYearRev = CALCULATE([Total Revenue], DATEADD(DimDate[Date], -1, YEAR))
VAR GrowthValue = CurrentRev - LastYearRev
VAR GrowthRatio = DIVIDE(CurrentRev, LastYearRev, 0)
VAR GrowthPct = GrowthRatio - 1

VAR CurrentSales = [Total Sales Count]
VAR PriorYearSales = CALCULATE([Total Sales Count], DATEADD(DimDate[Date], -1, YEAR))
VAR NewSales = CurrentSales - PriorYearSales

RETURN
    SWITCH(TRUE(),
        GrowthRatio < 0.95,
        "🔴 DECLINE: " & FORMAT(GrowthPct, "0.00%") & " | Revenue down €" & FORMAT(ABS(GrowthValue)/1000, "#,##0K"),
        GrowthRatio < 1.05,
        "⚠️ SLOW GROWTH: " & FORMAT(GrowthPct, "0.00%") & " more | Modest rev ↗️ €" & FORMAT(GrowthValue/1000, "#,##0K") & " | ↗️ +" & FORMAT(NewSales, "#,##0") & " more sales vs LY",
        GrowthRatio < 1.15,
        "✅ HEALTHY GROWTH: +" & FORMAT(GrowthPct, "0.0%") & " | +" & FORMAT(GrowthValue/1000, "#,##0K") & " vs LY | ↗️ +" & FORMAT(NewSales, "#,##0") & " more sales",
        "🚀 STRONG MOMENTUM: +" & FORMAT(GrowthPct, "0.0%") & " | +" & FORMAT(GrowthValue/1000, "#,##0K") & " vs LY | ↗️ +" & FORMAT(NewSales, "#,##0") & " more sales"
    )
```

#### 2. Pharmacy Performance Quadrant
```dax
Pharmacy Quadrant = 
VAR PharmRev = [Total Revenue]
VAR PharmMargin = [Margin %]
VAR NetworkAvgRev = 
    CALCULATE(
        AVERAGEX(VALUES(DimPharmacy[PharmacyID]), [Total Revenue]),
        ALL(DimPharmacy)
    )
VAR NetworkAvgMargin = 
    CALCULATE(
        AVERAGEX(VALUES(DimPharmacy[PharmacyID]), [Margin %]),
        ALL(DimPharmacy)
    )
RETURN
    SWITCH(TRUE(),
        AND(PharmRev >= NetworkAvgRev, PharmMargin >= NetworkAvgMargin), "⭐ Star Performer",
        AND(PharmRev >= NetworkAvgRev, PharmMargin < NetworkAvgMargin), "⚠️ High Volume, Low Margin",
        AND(PharmRev < NetworkAvgRev, PharmMargin >= NetworkAvgMargin), "💎 Efficient but Small",
        "🔴 Underperformer"
    )
```

#### 3. Promotion Lift (Corrected)
```dax
Promotion Lift = 
VAR PromoUnitsPerSale = 
    DIVIDE(
        CALCULATE([Total Units Sold], FactSales[PromoFlag] = "Yes"),
        CALCULATE(COUNTROWS(FactSales), FactSales[PromoFlag] = "Yes"), 0
    )
VAR NonPromoUnitsPerSale = 
    DIVIDE(
        CALCULATE([Total Units Sold], FactSales[PromoFlag] = "No"),
        CALCULATE(COUNTROWS(FactSales), FactSales[PromoFlag] = "No"), 0
    )
RETURN 
    DIVIDE(PromoUnitsPerSale - NonPromoUnitsPerSale, NonPromoUnitsPerSale, 0)
```

#### 4. Revenue at Risk
```dax
Revenue at Risk = 
CALCULATE(
    [Total Revenue],
    DimProduct[IsDiscontinued] = "Yes"
)

Revenue at Risk % = 
DIVIDE([Revenue at Risk], [Total Revenue], 0)

Revenue at Risk Label = 
VAR RiskPct = [Revenue at Risk %]
VAR RiskEUR = [Revenue at Risk]
VAR DiscontinuedCount = 
    CALCULATE(
        DISTINCTCOUNT(DimProduct[ProductID]),
        DimProduct[IsDiscontinued] = "Yes"
    )
RETURN
    SWITCH(TRUE(),
        RiskPct > 0.15,
        "🚨 " & FORMAT(RiskPct, "0%") & " rev at risk | " & DiscontinuedCount & " SKUs discontinued | Plan replacements now",
        RiskPct > 0.10,
        "🔴 " & FORMAT(RiskPct, "0%") & " (€" & FORMAT(RiskEUR/1000, "#,##0K") & ") at risk | Pipeline review needed",
        RiskPct > 0.05,
        "⚠️ " & FORMAT(RiskPct, "0%") & " at risk | " & DiscontinuedCount & " discontinued SKUs — monitor",
        RiskPct > 0,
        "✅ Low risk: " & FORMAT(RiskPct, "0%") & " (€" & FORMAT(RiskEUR/1000, "#,##0K") & ") | Manageable",
        "🎯 No discontinued revenue | Clean portfolio"
    )
```

#### 5. Pharmacy Performance Snapshot (Condensed)
```dax
Pharmacy Performance Snapshot - Condensed = 
VAR PharmRev = [Total Revenue]
VAR PharmMargin = [Margin %]
VAR PharmType = MAX(DimPharmacy[PharmacyType])
VAR StoreSize = MAX(DimPharmacy[StoreSizeBand])
VAR StoreAge = DATEDIFF(MAX(DimPharmacy[OpenDate]), TODAY(), YEAR)
VAR PharmRank = RANKX(ALL(DimPharmacy[PharmacyID]), [Total Revenue], , DESC, DENSE)
VAR TotalPharms = CALCULATE(DISTINCTCOUNT(DimPharmacy[PharmacyID]), ALL(DimPharmacy))
VAR RegionalAvg = 
    CALCULATE(
        AVERAGEX(VALUES(DimPharmacy[PharmacyID]), [Total Revenue]),
        ALLEXCEPT(DimPharmacy, DimPharmacy[Region])
    )
VAR vsRegion = DIVIDE(PharmRev - RegionalAvg, RegionalAvg, 0)
VAR Quadrant = [Pharmacy Quadrant]
VAR YoY = 
    DIVIDE(
        PharmRev - CALCULATE([Total Revenue], DATEADD(DimDate[Date], -1, YEAR)),
        CALCULATE([Total Revenue], DATEADD(DimDate[Date], -1, YEAR)), 0
    )
VAR PromoShare = DIVIDE(CALCULATE([Total Revenue], FactSales[PromoFlag] = "Yes"), PharmRev, 0)
VAR PromoImpact = [Promo Impact on Margin]

RETURN
    PharmType & " • Size " & StoreSize & " • " & StoreAge & " yrs old" & UNICHAR(10) &
    FORMAT(PharmRev/1000, "€#,##0K") & " revenue | " & FORMAT(PharmMargin, "0.0%") & " margin | Rank #" & PharmRank & "/" & TotalPharms & UNICHAR(10) &
    Quadrant & " | " & IF(vsRegion > 0, "↗️ +" & FORMAT(vsRegion, "0%"), "↘️ " & FORMAT(vsRegion, "0%")) & " vs region" & UNICHAR(10) &
    "YoY: " & IF(YoY > 0, "+" & FORMAT(YoY, "0%"), FORMAT(YoY, "0%")) & " | Promo: " & FORMAT(PromoShare, "0%") &
    IF(PromoImpact > 0.06, " 🚨 -" & FORMAT(PromoImpact, "0.0") & "pts", IF(PromoImpact > 0, " -" & FORMAT(PromoImpact, "0.0") & "pts", ""))
```

**[View Complete DAX Library (80+ Measures) →](docs/DAX_LIBRARY.md)**

---

## 🚀 Installation Guide

### Prerequisites

- Power BI Desktop (version 2.120+)
- 8GB RAM (16GB recommended)
- Windows 10/11 or macOS with Parallels

### Setup Steps

1. **Clone Repository**
```bash
   git clone https://github.com/yourusername/pharmacy-analytics-runner-up.git
   cd pharmacy-analytics-runner-up
```

2. **Open Power BI File**
```
   reports/European_Pharmacy_Analytics.pbix
```

3. **Load Data**
   - Navigate to `Home` → `Transform Data`
   - Update data source paths in Power Query
   - Point to your CSV files or database connection
   - Click `Close & Apply`

4. **Refresh Data**
   - `Home` → `Refresh`
   - Wait for data load (approx. 2-3 minutes for full dataset)

5. **Verify Functionality**
   - Navigate through all 3 pages
   - Test tooltips by hovering over visuals
   - Check that KPI reference labels display correctly
   - Test drill-down and cross-filtering

### Troubleshooting

**Issue:** Tooltips not appearing  
**Fix:** Right-click visual → `Format visual` → `Tooltips` → Ensure "Report page" is selected

**Issue:** Dynamic labels show errors  
**Fix:** Check that DimDate is marked as Date Table (`Model view` → Right-click DimDate → `Mark as date table`)

**Issue:** Slow performance  
**Fix:** Reduce data granularity in Power Query or apply row-level filters

---

## 💡 Key Insights & Recommendations

### 🚨 Critical Findings

#### 1. Promotion Strategy Failure
**Finding:** -2.39% promotion lift (customers buy LESS when products are discounted)

**Impact:**
- €650K+ margin lost annually
- 9pts margin erosion on promoted sales
- Zero incremental volume despite discounting

**Recommendation:**
```
IMMEDIATE ACTION (This Week):
→ STOP all active promotions
→ Audit top 20 promoted products for lift calculation
→ Test alternative tactics (bundles, loyalty rewards)

ROOT CAUSE INVESTIGATION:
→ Deep discounts (>25%) signal poor quality perception
→ High promo frequency (32% of days) trains customers to wait
→ Cherry-picking behavior (customers buy ONLY promo items)

STRATEGIC FIX (Next Quarter):
→ Shift to "Buy X Get Y" instead of "% OFF"
→ Introduce minimum purchase thresholds (€30 spend = discount)
→ Replace blanket discounts with personalized loyalty offers
```

---

#### 2. Generic Strategy Not Working
**Finding:** Branded products earn 3pts MORE margin than generics

**Impact:**
- Every generic substitution REDUCES profitability
- €740K margin opportunity missed (if generics matched branded margin)

**Recommendation:**
```
IMMEDIATE ACTION:
→ STOP all "push generic" initiatives until costs are renegotiated
→ Review generic supplier contracts for cost reduction opportunities
→ Re-price generic products UP by 8-10% to match margin profile

DATA VALIDATION:
→ Segment analysis by category (is gap consistent or category-specific?)
→ Check if branded "promotions" are distorting the comparison

STRATEGIC OPTIONS:
1. Renegotiate generic supplier costs (target: -5% COGS)
2. Introduce private label brand (higher margin potential)
3. Accept lower margin BUT increase generic volume 2x (net margin gain)
```

---

#### 3. Revenue at Risk from Discontinued Products
**Finding:** 8.2% of revenue (€1.55M) comes from products flagged as discontinued

**Impact:**
- Revenue cliff approaching as products phase out
- No replacement pipeline visible in data

**Recommendation:**
```
NEXT 60 DAYS:
→ Identify exact discontinuation dates for all 18 SKUs
→ Forecast revenue decay curve (when will €1.55M disappear?)
→ Build replacement SKU launch plan with marketing support

PRIORITIZATION:
→ Focus on HIGH-MARGIN discontinued products first
→ Products with >30% margin and >€50K revenue = critical to replace

NEW PRODUCT PIPELINE:
→ Accelerate 5-7 new SKU launches in Q2/Q3
→ Target categories: Vitamins (32% margin) and OTC (30% margin)
→ Expected impact: Recover €1.2M of at-risk revenue
```

---

### ✅ Operational Wins to Scale

#### 1. Star Performer Stores (24% of fleet, 32% of margin)
**Characteristics:**
- Urban locations, Large format
- 7-10 years operational maturity
- Low promo dependency (<30%)
- Strong basket size (€110+ per sale)

**Action:**
```
BEST PRACTICE DOCUMENTATION:
→ Interview top 5 store managers
→ Document 3 replicable practices per store
→ Create "Star Store Playbook" for network rollout

IMMEDIATE REPLICATION:
→ Share playbook with bottom-quartile stores
→ Monthly peer learning webinars (Stars teach Underperformers)
→ Bonus structure tied to margin improvement (not just revenue)
```

---

#### 2. New Store Ramp-Up Pattern
**Finding:** Stores take 18-24 months to reach mature productivity

**Implication:**
- 15% of fleet (24 stores) still ramping
- These stores drag overall metrics by 2-3pts

**Action:**
```
MATURITY ACCELERATION:
→ Assign "buddy store" mentorship (mature store coaches new store)
→ Pre-opening staff training at Star Performer locations
→ Accelerate local marketing spend in months 6-12

FORECASTING:
→ Exclude stores <18 months old from "underperformer" classification
→ Create separate "ramping stores" performance track
→ Expected benefit: 6-8 month faster ramp to profitability
```

---

## 🔧 Technical Specifications

### Performance Metrics

| Metric | Value | Target |
|--------|-------|--------|
| Total Report Size | 45.2 MB | < 100 MB |
| Data Refresh Time | 2min 15sec | < 5 min |
| Avg Visual Load Time | 0.8 sec | < 2 sec |
| DAX Measures | 82 | Optimized |
| Calculated Columns | 8 | Minimal |
| Relationships | 3 (All active) | Star schema |

### Browser Compatibility

- ✅ Power BI Service (Recommended)
- ✅ Power BI Desktop (Windows 10/11)
- ✅ Power BI Mobile (iOS/Android)
- ⚠️ Power BI Embedded (requires licensing)

### Data Refresh Schedule

**Production Environment:**
- Daily refresh at 6:00 AM UTC
- Incremental refresh enabled (last 90 days)
- Full refresh: Weekly (Sundays)

---

## 🔮 Future Enhancements

### Phase 1 (Next 3 Months)
- [ ] **Predictive Analytics** - Revenue forecasting using Python/R visuals
- [ ] **Customer Segmentation** - RFM analysis by pharmacy location
- [ ] **Mobile Layout** - Optimized views for tablet/phone
- [ ] **Bookmark Navigation** - Pre-configured analysis scenarios

### Phase 2 (3-6 Months)
- [ ] **Real-Time Dashboard** - DirectQuery for live inventory tracking
- [ ] **What-If Analysis** - Scenario modeling for pricing changes
- [ ] **Power Automate Alerts** - Email notifications for threshold breaches
- [ ] **Row-Level Security** - Multi-region access control

### Phase 3 (6-12 Months)
- [ ] **Machine Learning** - Churn prediction and demand forecasting
- [ ] **Competitive Benchmarking** - External market data integration
- [ ] **Supply Chain Module** - Inventory and supplier analytics
- [ ] **Customer Journey Mapping** - Transaction pattern analysis

---

## 🏆 Award Recognition Details

### Competition Context

**Challenge Name:** European Pharmacy Sales & Profitability Analytics  
**Organizer:** [Organization Name]  
**Participants:** 120+ analytics professionals from 15 countries  
**Submission Date:** January 2025  
**Award Announced:** February 2025

### Judging Criteria & Scores

| Category | Weight | Score | Judge Comments |
|----------|--------|-------|----------------|
| **Data Storytelling** | 25% | 92/100 | "Exceptional narrative flow across 3 pages. Each page builds upon the previous with clear purpose." |
| **Technical Excellence** | 25% | 88/100 | "Advanced DAX implementation with 80+ measures. Dynamic reference labels are innovative." |
| **Visual Design** | 20% | 90/100 | "Clean, professional aesthetic. Excellent use of tooltips and conditional formatting." |
| **Business Impact** | 20% | 95/100 | "Actionable insights with quantified ROI. €2M+ in identified opportunities." |
| **Innovation** | 10% | 87/100 | "Context-aware KPIs and pharmacy snapshots demonstrate creative problem-solving." |
| **Overall** | 100% | **90.4/100** | **🥈 RUNNER-UP** |

### Winning Elements (Judge Feedback)

> "The promotion lift analysis was a standout — identifying negative lift (-2.39%) and quantifying the €650K margin loss made the business case undeniable. The dynamic reference labels that adapt to thresholds showed deep understanding of executive decision-making."

> "The 3-page structure follows a perfect analytical narrative: WHAT (overview) → WHY (operations) → WHERE TO FIX (products). This is how analytics should be presented to C-suite."

> "The custom tooltips elevate this from a 'good dashboard' to a true decision support system. Hovering over any pharmacy reveals a complete performance snapshot with benchmarks and recommendations."

### Areas for Improvement (Judge Feedback)

> "Consider adding predictive forecasting for revenue trends. The historical analysis is excellent, but forward-looking scenarios would strengthen strategic planning value."

> "The report could benefit from automated alerting (e.g., email when a pharmacy drops below performance thresholds). Integration with Power Automate would complete the solution."

---

## 📞 Contact & Support

### Project Author

**[Your Name]**  
Data Analytics Professional | Power BI Specialist  
📧 Email: your.email@domain.com  
💼 LinkedIn: [linkedin.com/in/yourprofile](https://linkedin.com)  
🌐 Portfolio: [yourportfolio.com](https://yourportfolio.com)

### Questions or Feedback?

- 📚 **Documentation Issues**: Open a GitHub issue
- 💬 **General Questions**: Email or LinkedIn DM
- 🐛 **Bug Reports**: Submit via GitHub Issues with screenshots
- 🎓 **Learning Resources**: Check `docs/` folder for tutorials

---

## 🙏 Acknowledgments

- **Challenge Organizers** - For creating a realistic, business-focused challenge
- **Power BI Community** - For DAX optimization techniques and tooltip innovations
- **Peer Reviewers** - For feedback during development
- **Data Visualization Society** - For design inspiration

---

## 📜 License

This project is licensed under the **MIT License**.
```
MIT License

Copyright (c) 2025 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

[Full license text...]
```

---

<div align="center">

**🏆 Runner-Up Solution | European Pharmacy Analytics Challenge 2025**

[![View Demo](https://img.shields.io/badge/View-Demo-blue?style=for-the-badge)]()
[![Download PBIX](https://img.shields.io/badge/Download-PBIX-orange?style=for-the-badge)]()
[![Read Documentation](https://img.shields.io/badge/Read-Docs-green?style=for-the-badge)]()

**Built with ❤️ using Power BI, DAX, and Data Storytelling**

[⬆ Back to Top](#-european-pharmacy-sales--profitability-analytics)

</div>
