# Recruitment-Platform-Analysis
- Action-based clustering for user segmentation and integration of key cohorts into personalized product marketing
- Proposed AARRR-based marketing strategies as a Strategy Team Data Analyst to increase application rates of existing users on the recruitment platform.

---
## 1. Preprocessing  
- **Time Filtering**  
  - Extracted logs from May 24, 2023 onward (to account for “application complete” error corrections)  
- **Session Segmentation**  
  - Split sessions using a 30-minute inactivity threshold  
- **Path & UTM Categorization**  
  - Categorized user paths into 6 stages; UTM parameters into 4 types  
- **Noise Removal**  
  - Removed error-code responses and anomalous user rows  
- **Timestamp Feature Engineering**  
  - Derived `year`, `month`, `day`, `weekday`, etc.  

---

## 2. Exploratory Data Analysis (EDA)  
- **User Volume & Trends**  
  - 11,111 unique users since May 24  
  - Decline from ~4,700 in June to <3,500 by December  
- **Job Category Distribution**  
  - All listings: 41.7% SW Dev, 13.7% PM/Planning, 11.3% Marketing  
  - Applications: 56.8% SW Dev, 11.0% PM/Planning, 7.2% Marketing  
- **New vs. Existing User Behavior**  
  - Application completion: 91.6% (new) vs. 23.1% (Existing)  
  - Time to apply: 19 days (new) vs. 36 days (Existing)  
- **Cohort Analysis (Weekly/Monthly)**  
  - Noted stickiness (DAU/MAU drop-off), weekday activity peaks, and month-start influx  

---

## 3. Clustering Analysis  
**Objective:**  
Finesse behavioral distinctions beyond AARRR funnel using sequence-based patterns  

**Method:**  
1. Converted URL paths into session sequences  
2. Applied K-Means (4 clusters)

---

## 4. Final Insights
- **Month-Start Peak:** User activity spikes at each month’s start.  
- **Cohort Conditions:**  
  - ≤3 min sessions  
  - ≤3 sessions  
  - ≥13 job-listing page visits  
- **Actions:**  
  - Send personalized month-start push alerts  
  - Provide one-tap job-listing access  
  - A/B test messaging  
  - Track cohort metrics & funnel drop-offs  

