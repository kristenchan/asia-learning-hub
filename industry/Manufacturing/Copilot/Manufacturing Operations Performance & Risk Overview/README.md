# Manufacturing Operations Performance & Risk Overview

This package is a complete, lightweight, English-only demo for:

- **Copilot in Excel** (analysis)
- **Copilot in Word** (report creation)
- **Copilot in Outlook** (leadership communication)

## Scenario

You are a **Manufacturing Operations Performance Manager** preparing a weekly leadership review for:

- Plant Head
- Operations Director
- Quality Lead
- Supply Chain Lead

Your goal is to convert operational data into clear decisions on throughput, quality, delivery risk, and next actions.

## Files Included

1. `Operations_Data.csv`  
   Core operational metrics (throughput, downtime, OEE, delivery, and financial impact)
2. `Quality_and_Supplier_Risk.csv`  
   Combined quality and supplier risk signals
3. `Action_Register.csv`  
   Action owners, due dates, status, and expected impact
4. `Email_Distribution.csv`  
   Recipients for Outlook communication
5. `Weekly_Operations_Report_Template.docx`  
   Word template to generate the leadership report

## Complete Demo Steps

1. Create a new Excel workbook.
2. Import the four CSV files as worksheets:
   - `Operations_Data`
   - `Quality_and_Supplier_Risk`
   - `Action_Register`
   - `Email_Distribution`
3. Run the Excel prompts below to generate findings and dashboard outputs.
4. Open `Weekly_Operations_Report_Template.docx` in Word.
5. Use the Word prompts below to produce the weekly leadership report and save it.
6. In Outlook, attach the saved Word report and use the Outlook prompts below.

## Data Notes

- All records are **synthetic** and for demonstration only.
- Currency is **USD**.
- The data intentionally includes:
  - naming inconsistencies (`Plant A` vs `Plant-A`, `Drive Train` vs `Drivetrain`)
  - one duplicate row
  - one risk-spike week followed by recovery

## Copilot in Excel

### Workbook orientation

```text
Summarize this workbook in 30 seconds for senior operations leadership.
```

```text
Which worksheets are most important for throughput, quality risk, and delivery reliability? Explain in one short paragraph.
```

```text
List the top columns leadership should monitor every week and why.
```

### Data cleanup and validation

```text
Normalize similar values for Plant and Product Family naming (for example: Plant A vs Plant-A, Drive Train vs Drivetrain), and create a cleaned output table.
```

```text
Identify duplicate records in Operations_Data and list row references plus recommended correction.
```

```text
Find outliers in Downtime Minutes, Scrap Units, OEE, Defect PPM, and On-Time Delivery %. Rank the top 5 highest-risk records.
```

### Calculated fields

```text
Create a new column in Operations_Data called Operational Risk Category using these rules:
- Critical: Downtime Minutes > 180 OR On-Time Delivery % < 0.90
- High: Downtime Minutes between 140 and 180 OR Scrap Units > 45
- Medium: Downtime Minutes between 100 and 139 OR Scrap Units between 30 and 45
- Low: all other rows
```

```text
Create a formula in Quality_and_Supplier_Risk to flag records where First Pass Yield Actual < 0.96 AND Scrap Rate > 0.035. Return values: Watch, Stable.
```

### Trend and risk analysis

```text
Analyze week-over-week trends by Plant and Line for Completed Units, Downtime Minutes, and OEE. Highlight where performance worsened in W42 and where recovery happened in W43.
```

```text
Correlate Operations_Data and Quality_and_Supplier_Risk to identify lines that are weak on FPY, scrap, and OEE at the same time.
```

```text
Create a pivot table by Plant and Product Family showing Completed Units, Scrap Units, Downtime Minutes, and Estimated Margin Impact USD.
```

```text
Identify supplier-driven operational risk by combining Late PO Lines, Expedite Cost USD, and Production Impact Hours.
```

### Executive dashboard challenge

```text
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
```

---

## Copilot in Word

```text
Using Weekly_Operations_Report_Template.docx and the Excel workbook, draft a leadership-ready weekly manufacturing operations report.

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
```

```text
Write a 150-word executive risk summary for this week, including what improved, what remains at risk, and what leadership approval is needed.
```

---

## Copilot in Outlook

```text
Draft an email to primary recipients listed in Email_Distribution and CC the functional leads.
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
```

```text
Create a follow-up Teams-ready summary message (under 80 words) with:
- one line on current status
- one line on top risk
- one line on immediate next action
```
