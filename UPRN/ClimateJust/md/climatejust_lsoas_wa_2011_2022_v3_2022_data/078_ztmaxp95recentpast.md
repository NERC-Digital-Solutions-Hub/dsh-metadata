The field **'Average temperature of top 5% hottest days, recent past 30 year mean 1990 - 2019 (Score)'** (internal name `ztmaxp95recentpast`) represents the relative heat hazard score for the baseline period.

### **Description**
This metric converts the raw baseline temperature into a relative score. A higher score indicates that the neighbourhood was historically exposed to higher heat hazards compared to the average across the entire dataset (including all years and scenarios).

*   **Assumption:** Positive scores denote neighbourhoods that have historically experienced higher extreme heat hazards than the baseline average, providing a starting point for assessing heat disadvantage.
*   **Vulnerability Dimension:** This is the standardized input for the **Hazard Exposure** component.
*   **Caveat:** This is a relative score based on a specific z-score classification (e.g., >2.5 is "Acute").
*   **Data Source:** Standardized from **UKCP18** baseline climate data.
