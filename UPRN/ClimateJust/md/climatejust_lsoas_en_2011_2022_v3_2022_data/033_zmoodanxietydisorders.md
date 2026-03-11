### Mood and Anxiety Disorder Indicator (Z-Score)

**Description:**
This field (referred to as `ZMoodAnxietyDisorders` in the spatial dataset) represents the standardized Z-score for the prevalence of mood and anxiety disorders within a given Lower Super Output Area (LSOA). It measures how the local rate of these mental health conditions in a specific neighbourhood compares to the national average across England. 

**Vulnerability Rationale:**
This metric is a supporting indicator within the "Health" domain, which is used to calculate a community's overall "Sensitivity" (or biophysical susceptibility) to climate hazards like floods and heatwaves. 

Higher proportions of people with pre-existing mental health conditions indicate a higher level of social vulnerability. Extreme weather events, such as flooding, are highly stressful and can cause serious mental health impacts, including post-traumatic stress disorder, depression, and anxiety. While the post-event stress of a severe climate shock is likely to affect everyone, individuals with existing mental health conditions are typically the most susceptible to suffering the most severe and prolonged psychological impacts.

**Interpretation:**
Standardizing this metric as a Z-score allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher prevalence of mood and anxiety disorders than the national average, indicating higher relative vulnerability.
*   **Values around 0** indicate that the prevalence is approximately average for England.
*   **Negative values** signify a lower prevalence than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying data for this indicator is derived from the 2019 English Indices of Deprivation (IMD). Specifically, it utilizes the "Mood and Anxiety Disorders Indicator" from the Health Deprivation and Disability Domain, which is sourced from the Office for National Statistics. It carries a 0.143 weighting within the broader Health domain.