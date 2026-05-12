# Lead Quality Optimization & Performance Marketing Analysis

## 📌 Project Overview
[cite_start]This project involves a comprehensive analysis of approximately 3,000 leads generated for an advertiser to identify performance drivers and optimize lead quality[cite: 1, 2]. [cite_start]The objective was to evaluate historical trends, determine the impact of creative and placement variables on conversion, and model a path to a 20% increase in Lead Quality to unlock higher Cost-Per-Lead (CPL) payouts[cite: 5, 8].

## 🎯 Key Objectives
The analysis addresses three primary business questions:
1. [cite_start]**Trend Analysis:** Identifying statistically significant trends in lead quality over time[cite: 4, 5].
2. [cite_start]**Driver Identification:** Segmenting data by creative design, form layout, and user demographics to find quality drivers[cite: 6, 7].
3. [cite_start]**Revenue Modeling:** Developing a strategy to improve the lead quality rate from 8.0% to 9.6% to justify a CPL increase from $30 to $33[cite: 8].

## 🛠 Methodology & Data Logic

### 1. Defining Lead Quality
[cite_start]To quantify performance, I categorized every lead based on its final disposition in the CallStatus column[cite: 3, 14, 15]:
* [cite_start]**High Quality:** Includes "Closed" (the ultimate measure of success), "EP Sent", "EP Received", and "EP Confirmed"[cite: 16, 17, 21, 22, 24, 25].
* [cite_start]**Low Quality:** Includes "Unable to Contact" (invalid numbers), "Contacted - Invalid Profile" (wrong person), and "Contacted - Doesn't Qualify" (insufficient debt/income)[cite: 18, 26, 27, 28].
* [cite_start]**Unknown:** Leads where the consumer was not interested after learning program details or did not return calls[cite: 20, 30].

### 2. Feature Engineering: Widget & Creative Analysis
[cite_start]The WidgetName column was parsed to isolate variables affecting user friction and intent[cite: 31, 62]:
* [cite_start]**Form Layout:** Compared 1-Page Forms (1DC) against 2-Page Forms (2DC)[cite: 32, 33].
* [cite_start]**Creative Elements:** Analyzed specific design themes (e.g., "yellowarrow," "BlueMeter") and background colors[cite: 33, 34, 58].
* [cite_start]**Ad Size:** Grouped identical widgets such as the 300x250 and 302x252 formats[cite: 35, 36].

### 3. Data Validation Scores
[cite_start]Leveraged internal scoring systems to correlate data accuracy with final conversion[cite: 66, 69]:
* [cite_start]**AddressScore:** Comparison of name and address against offline databases (5 = perfect match, 1-2 = poor match)[cite: 67, 68].
* [cite_start]**PhoneScore:** Comparison of name and phone number accuracy[cite: 70, 71].

## 📈 Optimization Strategy
[cite_start]To achieve the target quality rate of 9.6% (a 20% improvement)[cite: 8]:
* [cite_start]**Segment Reallocation:** Identified high-performing segments in PublisherZoneName and Referral Domains to prioritize budget[cite: 63, 78].
* [cite_start]**Lead Friction:** Proposed shifting traffic toward 2DC form layouts and branded-shortform creatives, which filter for higher-intent users[cite: 32, 72].
* [cite_start]**Validation Filtering:** Recommended a threshold for AddressScore and PhoneScore to automatically prioritize leads with a score of 3 or higher[cite: 67, 70].

## 💻 Tech Stack
* **Excel:** For pivot tables and initial data exploration.
* **Python (Pandas/Matplotlib):** For complex string parsing of WidgetNames and visualization of trends.
* **Statistical Analysis:** Application of significance testing to confirm the validity of quality trends over time.
