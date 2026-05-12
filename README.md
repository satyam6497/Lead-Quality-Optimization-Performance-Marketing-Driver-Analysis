# Lead Quality Optimization & Performance Marketing Analysis

## Project Overview
This project involves a comprehensive analysis of approximately 3,000 leads generated for an advertiser to identify performance drivers and optimize lead quality. The objective was to evaluate historical trends, determine the impact of creative and placement variables on conversion, and model a path to a 20% increase in Lead Quality to unlock higher Cost-Per-Lead (CPL) payouts.

## Key Objectives
The analysis addresses three primary business questions:
1. **Trend Analysis:** Identifying statistically significant trends in lead quality over time.
2. **Driver Identification:** Segmenting data by creative design, form layout, and user demographics to find quality drivers.
3. **Revenue Modeling:** Developing a strategy to improve the lead quality rate from 8.0% to 9.6% to justify a CPL increase from $30 to $33.

## Methodology & Data Logic

### 1. Defining Lead Quality
To quantify performance, I categorized every lead based on its final disposition in the CallStatus column:
* **High Quality:** Includes "Closed" (the ultimate measure of success), "EP Sent", "EP Received", and "EP Confirmed".
* **Low Quality:** Includes "Unable to Contact" (invalid numbers), "Contacted - Invalid Profile" (wrong person), and "Contacted - Doesn't Qualify" (insufficient debt/income).
* **Unknown:** Leads where the consumer was not interested after learning program details or did not return calls.

### 2. Feature Engineering: Widget & Creative Analysis
The WidgetName column was parsed to isolate variables affecting user friction and intent:
* **Form Layout:** Compared 1-Page Forms (1DC) against 2-Page Forms (2DC).
* **Creative Elements:** Analyzed specific design themes (e.g., "yellowarrow," "BlueMeter") and background colors.
* **Ad Size:** Grouped identical widgets such as the 300x250 and 302x252 formats.

### 3. Data Validation Scores
Leveraged internal scoring systems to correlate data accuracy with final conversion:
* **AddressScore:** Comparison of name and address against offline databases (5 = perfect match, 1-2 = poor match).
* **PhoneScore:** Comparison of name and phone number accuracy.

## Optimization Strategy
To achieve the target quality rate of 9.6% (a 20% improvement):
* **Segment Reallocation:** Identified high-performing segments in PublisherZoneName and Referral Domains to prioritize budget.
* **Lead Friction:** Proposed shifting traffic toward 2DC form layouts and branded-shortform creatives, which filter for higher-intent users.
* **Validation Filtering:** Recommended a threshold for AddressScore and PhoneScore to automatically prioritize leads with a score of 3 or higher.

## Tech Stack
* **Excel:** For pivot tables and initial data exploration.
* **Python (Pandas/Matplotlib):** For complex string parsing of WidgetNames and visualization of trends.
* **Statistical Analysis:** Application of significance testing to confirm the validity of quality trends over time.
