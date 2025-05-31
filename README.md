# Recruitment Platform Data Analysis Project

---

### Action-Based Clustering for User Segmentation & Data-Driven Personalized Marketing Strategy

As a Strategy Team Data Analyst, I developed and proposed **AARRR framework-based marketing strategies** to increase application conversion rates among existing users on the recruitment platform.

---

### 1. Data Preprocessing
- **Time Filtering**: Extracted logs from after `May 24, 2023`, following “application complete” error corrections.
- **Session Segmentation**: Split user sessions using a `30-minute inactivity threshold`.
- **Path & UTM Categorization**: Categorized user paths into `6 stages` and UTM parameters into `4 types`.
- **Noise Removal**: Removed rows with error codes and anomalous user behaviors.
- **Timestamp Feature Engineering**: Derived features such as year, month, day, and weekday from timestamps.

---

### 2. Exploratory Data Analysis (EDA)
- **User Volume & Trends**:
  - Identified a total of **11,111** unique users since May 24, 2023.
  - Monthly active users declined from `~4,700 in June` to `<3,500 by December`.
- **Job Category Distribution**:
  - All job postings: Software Development `41.7%`, PM/Planning `13.7%`, Marketing `11.3%`
  - Applications: Software Development `56.8%`, PM/Planning `11.0%`, Marketing `7.2%`
- **New vs. Existing User Behavior**:
  - Application completion rate: New users `91.6%`, Existing users `23.1%`
  - Time to application: New users average `19 days`, Existing users average `36 days`
- **Cohort Analysis (Weekly/Monthly)**:
  - Noted a `DAU/MAU drop-off trend`, `weekday activity peaks`, and `increased user influx at the start of each month`

---

### 3. Clustering Analysis

**Objective:**
- To identify and segment nuanced user behaviors beyond the AARRR funnel.

**Method:**
- Converted user URL paths into session sequences and applied **K-Means clustering** (`4 clusters`).

**Findings:**
- The **“Inactive”** and **“Job Browser”** clusters were identified as key groups requiring improvement.
  - Of these, **“Job Browsers”** were chosen as the primary focus.
    - Although application count is close to zero, this group averages `14 job-listing views` and `12 job-detail views` per user.
    - Their view count is **10 times higher** than that of inactive users.
    - Therefore, targeting job browsers is the most realistic approach for rapid performance improvement.

---

### 4. Key Insights

- **Month-Start User Spike:**
  - User activity surges at the beginning of each month.

**Cohort Criteria:**
- Session duration `≤ 3 minutes`
- Total sessions `≤ 3`
- Job-listing page views `≥ 13`

**Recommended Action Plan:**
- Send personalized push notifications at the start of each month
- Provide one-tap access to job listings
- Conduct **A/B testing** for marketing messages
- Continuously monitor key cohort metrics and funnel drop-off rates

---

