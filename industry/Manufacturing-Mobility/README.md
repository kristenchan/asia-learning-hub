# Manufacturing Operations Performance & Risk Demo

This demo shows how a **Manufacturing Operations Performance Manager** uses Copilot in Excel, Word, and Outlook to go from four weeks of raw plant data to a leadership report and an approval email, in one connected workflow.


---

## Scenario

You are a **Manufacturing Operations Performance Manager at Contoso Manufacturing**, a company with two plants (Plant A and Plant B) producing Power Modules, Control Boards, Drive Trains and Sensor Packs.

It is **Monday morning, the start of week W44**. The **weekly performance and risk review** with leadership is this afternoon. Attendees:

- **Plant Head**, Morgan Hayes 
- **Operations Director**, Avery Brooks, 
- **Quality Lead**, Riley Chen, 
- **Supply Chain Lead**, Taylor Singh, 

You have received one workbook from the plants with information about:

- Weekly throughput, scrap and downtime by plant and line
- Equipment effectiveness (OEE, availability, performance, quality)
- On-time delivery to customers
- First pass yield, defect rates and customer complaints
- Supplier delivery performance and expedite costs
- Open management actions and their owners
- The leadership distribution list

Two weeks ago (W42) the plants had a **bad week**: lines stopped, scrap went up, customers complained. Last week (W43) the numbers look better. Leadership wants to understand:

- Which plants and lines are improving or declining?
- Where is throughput, OEE, or delivery reliability under pressure?
- What caused the W42 drop, and is the W43 recovery real?
- Which quality and supplier signals could impact next week's output?
- What actions need approval now?

**The challenge is not data availability. The challenge is turning many operational records into clear priorities and decisions before 2 p.m.**

The manager needs to move from **raw operations data to a decision leadership can approve**.

---

## Business Pain Points

The Operations Performance Manager faces several challenges during a typical weekly review.

### 1. Understanding a Multi-Sheet Workbook Quickly

Operations workbooks are often compiled by plant teams, quality and procurement, each with their own sheets and column names. Before analysis, the manager needs to know what is available, which sheets matter and which columns to watch.

**How Copilot helps:** Copilot summarizes the workbook structure and explains the key fields in natural language.

**Business benefit:** Faster orientation, less setup time and earlier focus on decisions.

---

### 2. Cleaning Data Before Analysis

Plant data is typed in by different shifts and systems. Inconsistent names (`Plant A` vs `Plant-A`), duplicate rows and unusual values can distort trends and lead to wrong conclusions.

**How Copilot helps:** Copilot helps normalize labels, detect duplicates and flag outliers.

**Business benefit:** More reliable analysis and fewer false conclusions in front of leadership.

---

### 3. Converting Raw Metrics into Risk Signals

Leaders do not make decisions from 19 raw columns. They need interpreted indicators: red, amber, green. The business rules exist, but writing nested formulas takes time and is error-prone.

**How Copilot helps:** Copilot creates calculated columns and formulas from plain-English business rules, and explains formulas it or others created.

**Business benefit:** Data becomes understandable, repeatable risk and performance signals.

---

### 4. Identifying Performance Drivers Across Plants, Lines and Suppliers

Row-level review cannot easily reveal what is driving week-over-week movement, or whether quality, equipment or supplier problems are behind it.

**How Copilot helps:** Copilot supports trend summaries, pivots, cross-sheet analysis and an executive dashboard.

**Business benefit:** A clear understanding of what is changing, why, and who owns the fix.

---

### 5. Turning Analysis into Leadership Communication

Even strong analysis loses value if it is not translated into a concise report and a clear request for decision. Rewriting the same facts for Word and Outlook is slow and introduces copy-paste errors.

**How Copilot helps:** Copilot drafts a structured Word report grounded in the workbook and an executive-ready Outlook email from the same facts.

**Business benefit:** Faster handoff from analysis to aligned action, with consistent numbers across every document.

---

## Demo Setup

### Files

| File | Purpose |
|---|---|
| `Manufacturing_Operations_Performance_and_Risk.xlsx` | One workbook, four sheets: `Operations_Data`, `Quality_and_Supplier_Risk`, `Action_Register`, `Email_Distribution` |
| `DATA_DICTIONARY.md` | Trainer reference: column definitions and manufacturing glossary (not used in prompts) |
| `Weekly_Operations_Report_Template.docx` | Word template for the weekly leadership report |

> **Note:** This workbook contains **synthetic sample data** created solely for training and demonstration purposes. It does not represent any real company, plant, supplier or person. All email addresses are fictional (`contoso.com`).

---

---

# Copilot Demo Journey

The demonstration follows the natural workflow of the Operations Performance Manager on review day:

**Understand → Prepare → Calculate → Analyze → Report → Communicate**

| Step | Time in scenario | App | Copilot capability | Leadership question it answers |
|---|---|---|---|---|
| 1. Understand | 8:30 a.m. | Excel | Summarize and explain | *What data do I have, and what matters?* |
| 2. Prepare | 8:45 a.m. | Excel | Clean and validate data | *Can I trust this data?* |
| 3. Calculate | 9:15 a.m. | Excel | Natural language → formulas | *How do raw numbers become risk signals?* |
| 4. Analyze | 10:00 a.m. | Excel | Trends, pivots, dashboard | *What is driving performance and risk?* |
| 5. Report | 11:30 a.m. | Word | Grounded drafting across files | *What does leadership need to read?* |
| 6. Communicate | 12:30 p.m. | Outlook | Audience-aware writing | *What should leadership approve now?* |

---

# 1. Understand the Operations Dataset (Excel)

## Business Challenge

> **Scenario moment, 8:30 a.m.** The workbook arrived overnight from the plant teams. You did not build it, and the review is at 2 p.m.

Before deeper analysis, the manager needs to understand what information is available, which sheets are relevant and which columns matter most.

## How Copilot Helps

Use natural-language questions to explore the workbook and quickly establish what is available and where to focus.

### 📋 Before you run
- Open the workbook and select any cell on `Operations_Data`.
- Tell the audience: *"Imagine this workbook just landed in your inbox. You have a few hours before the review."*

## Workbook Orientation

**Worksheet: Any**

```text
Summarize this workbook in 30 seconds for an operations leadership audience.
```

**Worksheet: Any**

```text
Explain this workbook as if I am a plant head preparing for a weekly performance review.
```

**Worksheet: Any**

```text
Which sheets are most important for throughput, quality risk, supplier risk, and leadership communication? List the most important columns to monitor weekly and explain why each matters.
```

### ✅ What to look for
- Copilot identifies the **four data sheets** and their purpose (operations KPIs, quality and supplier risk, action list, recipients).
- Key columns mentioned: **OEE, Downtime Minutes, On-Time Delivery %, First Pass Yield, Defect PPM, Late PO Lines**.
- Bonus: Copilot may already notice that **W42 looks worse** than the other weeks.

### 🗣️ Say this
> *"Copilot didn't just list the sheets. It explained why each one matters to an operations leader. That's the difference between reading data and understanding it."*

### Business Outcome

The manager quickly establishes what information is available and where to focus the weekly review.

---

# 2. Prepare and Validate Data (Excel)

## Business Challenge

> **Scenario moment, 8:45 a.m.** Last month a pivot table showed "Plant A" and "Plant-A" as two different plants, and leadership questioned every number in the deck. You do not want that again.

Before trusting the analysis, the manager needs to check data consistency. Potential issues:

- The same plant or product written two different ways
- Duplicate records
- Unusual downtime, scrap, OEE or defect values

## How Copilot Helps

Copilot identifies data-quality issues that should be reviewed before deeper analysis.

### 📋 Before you run
- The dataset contains **three intentional data-quality traps**. Do **not** reveal them first; let Copilot find them.
- No domain knowledge is needed: "the same thing written two ways" is the whole concept.

## Data Cleanup

**Worksheet: Operations_Data**

```text
Across Operations_Data and Quality_and_Supplier_Risk, normalize similar Plant and Product Family names (for example: Plant A vs Plant-A, Drive Train vs Drivetrain) and create a cleaned output table.
```

**Worksheet: Operations_Data**

```text
In Operations_Data, identify duplicate records and show row references with recommended correction.
```

**Worksheet: Operations_Data**

```text
Across Operations_Data and Quality_and_Supplier_Risk, find outliers in Downtime Minutes, Scrap Units, OEE, Defect PPM, and On-Time Delivery %. Rank the top 5 highest-risk records.
```

### ✅ What to look for (answer key)

| Trap | Where | Expected fix |
|---|---|---|
| Inconsistent plant name | `Plant-A`: W41, Line 2, on **both** sheets | → `Plant A` |
| Inconsistent product name | `Drivetrain`: W41, Plant B Line 1, on **both** sheets | → `Drive Train` |
| Duplicate record | `Operations_Data` **rows 17 and 18**: W43 Plant B Line 2 Sensor Pack, identical values | Remove one row |

- Outliers should cluster in **W42**. The worst record is **Plant A Line 2** (245 downtime minutes, 48.6% OEE, 87% on-time delivery, 2,890 defect PPM).

### 🗣️ Say this
> *"Without this step, W43 Sensor Pack output is counted twice, so the recovery looks better than it really is. That's how bad data turns into a bad decision."*

> **Tip:** Delete the duplicate row before continuing so totals in Step 4 are correct.

### Business Outcome

The manager has more confidence that the analysis is based on a consistent, trusted dataset.

---

# 3. Create Calculated Signals (Excel)

## Business Challenge

> **Scenario moment, 9:15 a.m.** The Plant Head told you on the phone: *"Anything with more than 3 hours of downtime, or that ships late on more than 10% of orders, is Critical."* You need that rule applied to every line, every week, and it must still work next week.

Raw values need business classifications before they can support management decisions. The manager may also need to explain the logic to someone who did not write it.

## How Copilot Helps

Copilot creates calculated columns from plain-English rules and explains formulas in plain language.

### 📋 Before you run
- Point out: *"These thresholds are business rules a plant manager would give you verbally. Watch Copilot turn them into a formula."*
- Percentages are stored as decimals (90% = 0.90), which is why the rules use decimals.

## Calculated Columns

**Worksheet: Operations_Data**

```text
Create a new column in Operations_Data called Operational Risk Category using these rules:
- Critical: Downtime Minutes > 180 OR On-Time Delivery % < 0.90
- High: Downtime Minutes between 140 and 180 OR Scrap Units > 45
- Medium: Downtime Minutes between 100 and 139 OR Scrap Units between 30 and 45
- Low: all other rows
```

**Worksheet: Quality_and_Supplier_Risk**

```text
Create a formula in Quality_and_Supplier_Risk to flag records where First Pass Yield Actual < 0.96 AND Scrap Rate > 0.035. Return values: Watch, Stable.
```

**Worksheet: Operations_Data**

```text
Explain the formula in the Operational Risk Category column in plain language, as if to a new team member who will maintain this workbook.
```

### ✅ What to look for (answer key)

**Operational Risk Category** (16 rows after the duplicate is removed):

| Week | Plant A Line 1 | Plant A Line 2 | Plant B Line 1 | Plant B Line 2 |
|---|---|---|---|---|
| W40 | Low | Medium | Medium | Low |
| W41 | Medium | Medium | High | Medium |
| W42 | **Critical** | **Critical** | **Critical** | High |
| W43 | Low | Low | Low | Low |

**Watch flag:** **7 Watch** (W41 Plant A Line 2, Plant B Lines 1 and 2, plus all four W42 lines), **9 Stable**.

- Check that Copilot inserts a **formula**, not typed values (click a cell and show the formula bar).
- **Edge case if asked:** W42 Plant B Line 1 has on-time delivery of exactly **90%**, which does *not* meet "< 0.90". It is still Critical because its downtime (198 min) is above 180.

### 🗣️ Say this
> *"The rule came from a phone call; the formula came from Copilot. Because it's a real formula, next week's data is categorized automatically, and anyone can ask Copilot to explain it."*

### Business Outcome

Raw data is transformed into understandable, repeatable risk categories.

---

# 4. Identify Performance and Risk Drivers (Excel)

## Business Challenge

> **Scenario moment, 10:00 a.m.** The Operations Director messages you: *"Was W42 a one-off or a pattern? Which line and which supplier? I need one page, not 16 rows."*

Now that the data is understood and prepared, the manager needs to answer the more important question:

> **What is actually driving performance and risk?**

## How Copilot Helps

Copilot summarizes patterns, analyzes trends across sheets, creates pivots and builds an executive dashboard.

### 📋 Before you run
- Make sure the duplicate row from Step 2 is removed; otherwise totals are inflated.
- Short on time? Run only the **dashboard** prompt (last one).

## Trend and Driver Analysis

**Worksheet: Operations_Data**

```text
Analyze week-over-week trends by Plant and Line for Completed Units, Downtime Minutes, and OEE. Highlight where performance worsened in W42 and where recovery happened in W43.
```

**Worksheet: Quality_and_Supplier_Risk**

```text
Correlate Operations_Data and Quality_and_Supplier_Risk to identify lines that are weak on FPY, scrap, and OEE at the same time.
```

**Worksheet: Operations_Data**

```text
Create a pivot table by Plant and Product Family showing Completed Units, Scrap Units, Downtime Minutes, and Estimated Gross Margin USD.
```

**Worksheet: Quality_and_Supplier_Risk**

```text
Identify supplier-driven operational risk by combining Late PO Lines, Expedite Cost USD, and Production Impact Hours across all four weeks. Rank suppliers from highest to lowest risk.
```

## Executive Dashboard Challenge

**Worksheet: Any**

```text
Create an Executive Manufacturing Operations Dashboard from this workbook.

Include:
- Total Completed Units (W40–W43)
- Average OEE by week
- Average Scrap Rate
- Total Downtime Minutes
- On-Time Delivery trend by week
- Top 3 high-risk lines based on the peak week (W42)
- Top 2 supplier risks across all four weeks
- Three recommended actions with owner names from Action_Register

Use an executive-friendly layout with red, amber, and green indicators.
```

### ✅ What to look for (answer key, after the duplicate is removed)

| Metric | Expected value |
|---|---|
| Total Completed Units | **15,190** (16,020 if the duplicate was *not* removed) |
| Average OEE by week | W40 78.3% → W41 70.2% → **W42 54.4%** → W43 81.3% |
| Total Downtime Minutes | **2,021** |
| Average Scrap Rate | **3.7%** |
| On-Time Delivery by week | 96.5% → 94.0% → **89.3%** → 97.0% |
| Weekly Gross Margin | $545.5K → $522K → **$448K** → $567.5K |
| Top 3 high-risk lines (W42) | **Plant A Line 2**, Plant A Line 1, Plant B Line 1 |
| Lines weak on FPY + scrap + OEE together | **Plant A Line 2** and **Plant B Line 1** (W41–W42) |
| Top 2 supplier risks | **Supplier Nova** and **Supplier Apex** |
| Recommended actions | A-001 Alex Morgan · A-002 Riley Chen · A-003 Taylor Singh |

### 🗣️ Say this
> *"Look at the top risks Copilot found: Plant A Line 2, Drive Train, Nova and Apex. Now look at the Action Register: the same names. The data and the plan agree, and that's what gives leadership the confidence to approve."*

### Business Outcome

The manager can identify:

- Where performance dropped and where it recovered
- Which lines, products and suppliers drove the W42 crisis
- The financial impact (weekly gross margin fell $97.5K from W40 to W42)
- Which actions and owners address each risk

This shifts the conversation from **"What data do we have?"** to **"What is driving the business, and who fixes it?"**

---

# 5. Create the Weekly Leadership Report (Word)

## Business Challenge

> **Scenario moment, 11:30 a.m.** Leadership expects the weekly report in the standard template **one hour before** the review, so they can read it in advance.

Excel findings must be converted into a concise narrative. The report must use only workbook data and make the decision needed this week obvious.

## How Copilot Helps

Copilot drafts a structured report grounded in two files (the template and the workbook), so the manager edits instead of writing from scratch.

### 📋 Before you run
- Open a **new blank Word document** (or the template) and open Copilot.
- Use `/` in the prompt box to reference **both files**. If they don't appear, they are not in OneDrive/SharePoint (see Pre-Flight).
- Remind the audience: the report must use **only workbook data**, so check the numbers against Step 4.

## Word Prompts

**App: Word**

```text
Using /Weekly_Operations_Report_Template and /Manufacturing_Operations_Performance_and_Risk, draft a leadership-ready weekly manufacturing operations report for week 2026-W43.

Follow the template sections:
1. Executive Summary
2. Throughput and OEE Movements
3. Quality and Supplier Risk Watchlist
4. Top Root-Cause Hypotheses
5. Top 3 Management Actions (with owner and due date from Action_Register)
6. Leadership Approval Needed

Guidelines:
- Keep the report concise and insight-driven.
- Use clear headings and bullet points.
- Compare W43 against the W42 low point and the W40 baseline.
- Focus on business impact and decisions needed this week.
- Use only data from the workbook.
```

**App: Word**

```text
Write a 150-word executive risk summary for this week. Include what improved, whether the recovery is sustainable given that some actions in the Action_Register are still only Planned, and what leadership approval is needed.
```

### ✅ What to look for
- All **six template sections** are filled, including *Leadership Approval Needed*.
- Numbers match Step 4 (e.g., OEE recovered from 54.4% in W42 to 81.3% in W43).
- **Root-cause hypotheses** reflect the data: equipment downtime (Plant A Line 2), incoming material quality (Drive Train), supplier delivery (Nova, Apex).
- Management actions list **Alex Morgan (Oct 29), Riley Chen (Oct 30), Taylor Singh (Oct 30)**.
- The summary flags that **A-002 and A-003 are still Planned**: the recovery is real but not yet secured.

### 🗣️ Say this
> *"W43 looks great, and a less careful report would stop there. Copilot surfaces the risk that remains: the fixes that prevent another W42 haven't started yet. That's the decision leadership needs to make."*

> **Why this prompt:** asking "what remains at risk?" can lead Copilot to answer "nothing" (all W43 indicators are Low) or to invent a risk. Asking whether the recovery is *sustainable* points Copilot at the real remaining risk in the data.

> **Before Step 6:** save the report to OneDrive as `Weekly_Operations_Report_W43.docx`.

### Business Outcome

Insights are translated into a management-ready weekly report that leadership can read before the meeting.

---

# 6. Send Leadership Communication (Outlook)

## Business Challenge

> **Scenario moment, 12:30 p.m.** The Plant Head will not open a six-section report on their phone between meetings. They need a short email that says what is urgent and what they must approve, and the approval is needed **before the first action is due on Oct 29**.

Leaders need a concise message that separates urgent risks from normal follow-ups and ends with a clear request.

## How Copilot Helps

Copilot rewrites the same facts for a different audience and format: shorter, urgent items first, explicit owners and dates.

### 📋 Before you run
- Open a **new email** in Outlook and use **Draft with Copilot**. Use `/` to reference the workbook and the saved report.
- ⚠️ **Create a draft only. Do not send.** The recipients are fictional `contoso.com` addresses.
- Copilot does **not attach files automatically**. After the draft is generated, attach the Word report manually (or insert it as a link).

## Outlook Prompt

**App: Outlook**

```text
Draft an email to the Primary recipients listed in the Email_Distribution sheet of /Manufacturing_Operations_Performance_and_Risk and CC the recipients marked CC.
Reference the weekly report /Weekly_Operations_Report_W43.

Include:
- Key operational highlights
- Major quality and delivery risks
- Three recommended actions with owner names and target dates from Action_Register

Requirements:
- Keep the email under 200 words
- Use a professional executive tone
- Separate urgent risks from improvement opportunities
- End with a clear approval request and deadline
```

### ✅ What to look for
- **To:** Morgan Hayes (Plant Head), Avery Brooks (Operations Director).
- **CC:** Riley Chen, Taylor Singh, Alex Morgan, Cameron Patel. (If Copilot doesn't fill the address fields, copy them from the sheet; the content is the point of the demo.)
- Under 200 words, a clear **Urgent** vs **Opportunities** split, and an **approval request with a date**. A natural deadline is **Oct 29**, the first action due date.

### 🗣️ Say this
> *"Same facts, third format. Excel found the patterns, Word explained them, and Outlook asks for a decision in under 200 words."*

### ➕ Optional extension: Teams follow-up

> **Scenario moment, after the review.** Leadership approved the actions. The plant floor supervisors need a three-line update in the operations Teams channel.

Run in **Microsoft 365 Copilot Chat** or a Teams chat with yourself:

```text
Create a follow-up Teams-ready summary message (under 80 words) with:
- one line on current status
- one line on top risk
- one line on immediate next action
```

**Look for:** three short lines covering recovery to about 81% OEE, sustainability depending on A-002 and A-003, and the approval or next action by Oct 29.

### Business Outcome

Leadership receives clear, action-oriented communication with explicit next decisions, owners and deadlines.

---

# Advanced Extension: Copilot Analyst

> **Scenario moment, after the review.** The Operations Director asks: *"W42 surprised us. Could we have seen it coming, and what should we watch in W44?"*

Once the manager understands historical performance, the next question becomes:

> **Are there early-warning patterns we should watch, and what might happen next?**

For a more advanced analytical experience, use **Copilot Analyst** (Microsoft 365 Copilot) with the workbook.

```text
Using Python, analyze /Manufacturing_Operations_Performance_and_Risk to identify which indicators moved first before the W42 drop in OEE (for example: downtime, defect PPM, late PO lines, changeover minutes).

Then project a simple W44 outlook for OEE and on-time delivery by line, and recommend 3 early-warning thresholds leadership should monitor weekly.

Show the trend charts and explain the results in plain business language, including the limitations of having only four weeks of data.
```

### ✅ What to look for
- **W41 is the early-warning week.** Downtime, defect PPM, late PO lines and changeover minutes all rose in W41, **before** the W42 OEE drop.
- Copilot should **state the limitation**: with only four weeks of data, any projection is indicative, not a forecast to plan production on.

### Business Value

This extends the weekly review from looking back to looking ahead:

- Leading indicators that signal a crisis one week early
- Early-warning thresholds leadership can monitor
- A more proactive operating rhythm

---