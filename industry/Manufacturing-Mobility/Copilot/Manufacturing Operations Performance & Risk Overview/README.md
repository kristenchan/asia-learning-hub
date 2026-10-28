# Manufacturing Operations Performance & Risk Demo

This demo showcases how a **Manufacturing Operations Performance Manager** can use **Copilot in Excel, Word, and Outlook** to move from raw operations data to decision-ready leadership communication.

---

## Scenario

You are a **Manufacturing Operations Performance Manager** preparing a weekly performance and risk review for:

- Plant Head
- Operations Director
- Quality Lead
- Supply Chain Lead

You have one workbook with operations, quality, supplier risk, action owners, and email distribution details. Leadership wants to quickly understand:

- Which plants and lines are improving or declining
- Where throughput, OEE, or delivery reliability is under pressure
- Which quality and supplier signals could impact next week output
- What actions need approval now

The challenge is not data availability. The challenge is turning many operational records into clear priorities and decisions.

---

## Business Pain Points

### 1. Understanding a Multi-Sheet Workbook Quickly

Operations reviews are often time-sensitive. Analysts need to quickly identify which sheets and columns matter most.

**How Copilot helps:** Copilot summarizes workbook structure and highlights key fields.

**Business benefit:** Faster orientation, less setup time, earlier focus on decisions.

---

### 2. Cleaning Data Before Analysis

Manufacturing data often contains naming inconsistencies, duplicate records, and outliers that can mislead trends.

**How Copilot helps:** Copilot helps normalize labels, detect duplicates, and flag unusual values.

**Business benefit:** More reliable analysis and fewer false conclusions.

---

### 3. Converting Raw Metrics into Risk Signals

Leaders do not make decisions from raw columns alone. They need interpreted indicators.

**How Copilot helps:** Copilot assists with calculated categories and business-rule-based flags.

**Business benefit:** Data becomes understandable risk and performance signals.

---

### 4. Identifying Performance Drivers Across Plants and Lines

Row-level review cannot easily reveal what is driving week-over-week movement.

**How Copilot helps:** Copilot supports trend summaries, pivots, and correlation-style analysis.

**Business benefit:** Clear understanding of what is changing and why.

---

### 5. Turning Analysis into Leadership Communication

Even strong analysis loses value if it is not translated into concise, actionable communication.

**How Copilot helps:** Copilot drafts a structured Word report and an executive-ready Outlook message.

**Business benefit:** Faster handoff from analysis to aligned action.

---

# Copilot Demo Journey

The demonstration follows a practical operations workflow:

**Understand -> Prepare -> Calculate -> Analyze -> Report -> Communicate**

---

## Demo Setup

### Files

1. `Manufacturing_Operations_Performance_and_Risk_Demo.xlsx`
   - Single workbook with these sheets:
   - `Operations_Data`
   - `Quality_and_Supplier_Risk`
   - `Action_Register`
   - `Email_Distribution`

2. `Weekly_Operations_Report_Template.docx`
   - Word template for the weekly leadership report.

> **Note:** All records are synthetic sample data created for training and demo use only.

---

# 1. Understand the Operations Dataset (Excel)

## Business Challenge

Before deeper analysis, the manager needs to quickly understand workbook structure and key business fields.

## Workbook Orientation Prompts

~~~text
Summarize this workbook in 30 seconds for an operations leadership audience.
~~~

~~~text
Which sheets are most important for throughput, quality risk, supplier risk, and leadership communication? Explain in one short paragraph.
~~~

~~~text
List the most important columns to monitor weekly and explain why each matters.
~~~

### Business Outcome

The manager quickly identifies what matters and where to focus.

---

# 2. Prepare and Validate Data (Excel)

## Business Challenge

Inconsistent labels and unusual records can distort operational conclusions.

## Data Preparation Prompts

~~~text
Across Operations_Data and Quality_and_Supplier_Risk, normalize similar Plant and Product Family names (for example: Plant A vs Plant-A, Drive Train vs Drivetrain) and create a cleaned output table.
~~~

~~~text
In Operations_Data, identify duplicate records and show row references with recommended correction.
~~~

~~~text
Across Operations_Data and Quality_and_Supplier_Risk, find outliers in Downtime Minutes, Scrap Units, OEE, Defect PPM, and On-Time Delivery %. Rank the top 5 highest-risk records.
~~~

### Business Outcome

The dataset is more consistent and better prepared for trusted analysis.

---

# 3. Create Calculated Signals (Excel)

## Business Challenge

Leadership needs interpreted risk signals, not just raw values.

## Calculation Prompts

~~~text
Create a new column in Operations_Data called Operational Risk Category using these rules:
- Critical: Downtime Minutes > 180 OR On-Time Delivery % < 0.90
- High: Downtime Minutes between 140 and 180 OR Scrap Units > 45
- Medium: Downtime Minutes between 100 and 139 OR Scrap Units between 30 and 45
- Low: all other rows
~~~

~~~text
Create a formula in Quality_and_Supplier_Risk to flag records where First Pass Yield Actual < 0.96 AND Scrap Rate > 0.035. Return values: Watch, Stable.
~~~

### Business Outcome

Raw data is transformed into decision-ready categories.

---

# 4. Identify Performance and Risk Drivers (Excel)

## Business Challenge

Management needs to know where performance is worsening, where recovery is happening, and which risks may impact next week output.

## Analysis Prompts

~~~text
Analyze week-over-week trends by Plant and Line for Completed Units, Downtime Minutes, and OEE. Highlight where performance worsened in W42 and where recovery happened in W43.
~~~

~~~text
Correlate Operations_Data and Quality_and_Supplier_Risk to identify lines that are weak on FPY, scrap, and OEE at the same time.
~~~

~~~text
Create a pivot table by Plant and Product Family showing Completed Units, Scrap Units, Downtime Minutes, and Estimated Margin Impact USD.
~~~

~~~text
Identify supplier-driven operational risk by combining Late PO Lines, Expedite Cost USD, and Production Impact Hours.
~~~

~~~text
Create an Executive Manufacturing Operations Dashboard from this workbook.

Include:
- Total Completed Units
- Average OEE
- Average Scrap Rate
- Total Downtime Minutes
- On-Time Delivery trend
- Top 3 high-risk lines
- Top 2 supplier risks
- Three recommended actions with owner names from Action_Register

Use an executive-friendly layout with red, amber, and green indicators.
~~~

### Business Outcome

Performance and risk drivers are consolidated into a leadership view.

---

# 5. Create the Weekly Leadership Report (Word)

## Business Challenge

Excel findings must be converted into a concise narrative for leadership decisions.

## Word Prompt

~~~text
Using Weekly_Operations_Report_Template.docx and Manufacturing_Operations_Performance_and_Risk_Demo.xlsx, draft a leadership-ready weekly manufacturing operations report.

Required sections:
1. Executive Summary
2. Throughput and OEE Movements
3. Quality and Supplier Risk Watchlist
4. Top Root-Cause Hypotheses
5. Top 3 Management Actions (with owner and due date from Action_Register)

Guidelines:
- Keep the report concise and insight-driven.
- Use clear headings and bullet points.
- Focus on business impact and decisions needed this week.
- Use only data from the workbook.
~~~

~~~text
Write a 150-word executive risk summary for this week, including what improved, what remains at risk, and what leadership approval is needed.
~~~

### Business Outcome

Insights are translated into a management-ready weekly report.

---

# 6. Send Leadership Communication (Outlook)

## Business Challenge

Leaders need a concise message that separates urgent risks from normal follow-ups.

## Outlook Prompts

~~~text
Draft an email to primary recipients listed in the Email_Distribution sheet and CC the functional leads.
Reference and attach the saved weekly Word report.

Include:
- Key operational highlights
- Major quality and delivery risks
- Three recommended actions with owner names and target dates from Action_Register

Requirements:
- Keep the email under 200 words
- Use a professional executive tone
- Separate urgent risks from improvement opportunities
- End with a clear approval request and deadline
~~~

~~~text
Create a follow-up Teams-ready summary message (under 80 words) with:
- one line on current status
- one line on top risk
- one line on immediate next action
~~~

### Business Outcome

Leadership receives clear, action-oriented communication with explicit next decisions.

---

# End-to-End Demo Story

## Step 1: Understand

**Question:** What data do I have and what matters most?

**Outcome:** Fast orientation of workbook structure and key KPIs.

## Step 2: Prepare

**Question:** Is this data consistent enough for reliable analysis?

**Outcome:** Cleaner dataset with key quality issues identified.

## Step 3: Calculate

**Question:** How do we convert raw columns into operational signals?

**Outcome:** Risk categories and watch flags are created.

## Step 4: Analyze

**Question:** What is driving performance and risk this week?

**Outcome:** Trends, pivots, and risk concentrations are surfaced.

## Step 5: Report

**Question:** What does leadership need to read before review?

**Outcome:** A concise, decision-focused weekly Word report.

## Step 6: Communicate

**Question:** What action should leaders approve now?

**Outcome:** A focused Outlook communication aligned to ownership and deadlines.

---

# Demo Takeaway

This is not just a feature demo of individual Copilot prompts.

It demonstrates a complete manufacturing operations workflow:

**Data -> Insight -> Report -> Decision Communication**

The value is helping operations leaders spend less time assembling updates and more time driving corrective action.
