# Social Media Usage vs. Academic Deadlines: An Analysis

## Overview
This project investigates the relationship between social media usage (Instagram and YouTube) and academic deadlines. The goal was to determine whether proximity to deadlines significantly affects daily social media usage.

## Hypothesis
**"I tend to use social media more when I am under the inluence of academic stress."**

## Methodology

### Data Collection
- **Instagram Usage**:
  - Extracted using the **"Saved" data** from Instagram.
  - Instagram doesn't provide direct time-spent statistics; thus, usage time was **estimated** based on timestamps of "Saved" actions:
    - Usage starts at the first "Saved" action of the day.
    - Pauses if no actions occur within a 30-minute window.
    - The total active time per day was calculated by summing the durations of active intervals.
- **YouTube Usage**:
  - Extracted using watch history and YouTube API.
  - Daily usage time was calculated based on video durations and timestamps.

- **Academic Deadlines**:
  - Manually documented as a JSON file (can be found inside the project documents), including all key academic events like exams, project deadlines, and homework due dates. 

### Data Preprocessing
- **Daily Aggregation**:
  - Social media usage data was aggregated daily for both platforms.
  - Academic deadlines were aligned with daily social media usage data.

- **Normalization**:
  - Data was normalized (scaled between 0 and 1) to facilitate comparison and prepare for statistical tests.

### Analysis
#### Regression Analysis
- **Linear Regression**:
  - Examined the relationship between daily social media usage and days relative to deadlines.
  - Key Findings:
    - Weak relationships were observed:
      - Instagram Usage: **Weak positive trend** (r ≈ 0.26).
      - YouTube Usage: **Weak negative trend** (r ≈ -0.25).
      - Total Usage: **Weak negative trend** (r ≈ -0.22).
    - Regression results:
      - **Intercept**: Average usage on the deadline day ≈ 188 minutes.
      - **Slope**: Social media usage decreases by ≈ 2.48 minutes per day as deadlines move further away.

- **Polynomial Regression**:
  - Explored non-linear relationships to capture more subtle trends.
  - Results showed no strong patterns, confirming weak overall influence of deadlines.

#### Statistical Significance
- **Chi-Square Test**:
  - The data was normalized and subjected to a Chi-Square test to assess the statistical significance of deviations from expected usage patterns.
  - Results:
    - **Chi-Square Statistic**: 2.19
    - **Critical Value (0.05 significance)**: 23.68
    - **p-value**: 0.9999
    - **Conclusion**: Failed to reject \( H_0 \), indicating **no statistically significant relationship** between social media usage and deadlines.

## Results
- **Regression Analysis**:
  - Usage trends relative to deadlines were weak and not statistically significant.
  - Regression lines suggested minor trends but high variability in data.

- **Statistical Significance**:
  - The Chi-Square test confirmed no significant deviation from expected usage patterns.
